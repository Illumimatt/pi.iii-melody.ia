<h3 align="center">Projeot Integrador III Melody AI</h3>
<div align="center">
  <img src="melody_logo.png" width="500" height="600" alt="Logo do projeto">
</div>
<p align="center"> Este projeto integrador está sendo desenvolvido como parte do curso de Ciência da Computação da Universidade CEUB e tem como objetivo o desenvolvimento de uma plataforma de karaoke impulsionada por IA, do conceito ao lançamento. </p>

<p align="center">
  <img src="https://img.shields.io/badge/status-Em%20Desenvolvimento-yellow" alt="Status do Projeto: Em Desenvolvimento">
  <img src="https://img.shields.io/badge/framework-Flutter-blue?logo=flutter" alt="Framework: Flutter">
  <img src="https://img.shields.io/badge/tech-Python_IA-black?logo=python" alt="Tech: Python">
</p>

## 🏆 Status Atual: MVP Validado em Campo (ConectaCEUB)

O **melody.ai** ultrapassou a fase de prova de conceito. Nosso Produto Mínimo Viável (MVP) foi submetido a testes de estresse com usuários reais durante o evento de tecnologia **ConectaCEUB**. 

A plataforma operou continuamente, processando sob demanda dezenas de músicas em tempo real sem degradação do servidor. Com base nos dados coletados com os participantes, alcançamos notas de aprovação quase unânimes (entre 9 e 10) em **usabilidade do aplicativo**, **qualidade do isolamento instrumental** e **democratização do catálogo musical**.

## Sobre o Projeto: "melody.ai / melody.io"

### Objetivo

O objetivo é desenvolver um ecossistema completo de software (aplicativo cliente e microsserviços de IA) capaz de gerar uma **Karaoke Experience (KE)** autêntica a partir de qualquer música, separando faixas de áudio e sincronizando letras automaticamente.

### Contexto e Público-Alvo

O "melody.io" é uma **plataforma interativa musical**. O foco é proporcionar diversão e aprimoramento vocal, onde o jogador pode cantar suas músicas favoritas com instrumentais isolados, letras perfeitamente sincronizadas e feedback de performance.

O **público-alvo** são entusiastas de música, grupos de amigos buscando entretenimento (karaoke) e cantores amadores que desejam praticar com faixas instrumentais limpas e avaliação em tempo real.

O projeto abrange todas as fases do desenvolvimento, incluindo:

- Arquitetura de microsserviços e integração de APIs.
- Pipeline de Inteligência Artificial para processamento e separação de áudio.
- Programação de interface fluida (UI/UX) e processamento de microfone em tempo real.
- Correção de linguagem natural via modelos GPT e romanização de letras.

## Por que este projeto é importante?

Este projeto representa a ponte entre o conhecimento acadêmico e a experiência prática do mercado tecnológico. Nossa motivação é criar um produto inovador e tangível. Os pilares da nossa motivação são:

- **Aprender:** Aplicar teorias complexas de processamento de sinais de áudio, machine learning e arquitetura front/back em um desafio real.
- **Nos Desafiar:** Superar os limites técnicos de sincronização em tempo real (baixa latência) e geração de waveforms no lado do cliente.
- **Inovar:** Entregar uma solução automatizada que elimina a necessidade de catálogos manuais de karaoke, transformando qualquer música em uma experiência interativa.

## Quem está envolvido e é responsável pelo sucesso do projeto?

A equipe é formada por um grupo com habilidades complementares, adotando práticas do framework Scrum:

| Nome                                                   | Funções                                          |
| :----------------------------------------------------  | :----------------------------------------------- |
| **Matheus Kollmann Deters** | Product Owner (PO) e Dev Team (Front/Back)       |
| **Julia Costa Carvalho** | Scrum Master (SM) e Dev Team (Front/Back)        |
| **Bruno D’Luka Antunes V. Oliveira** | Arquiteto de Softwares e Dev Team (Front/Back)   |
| **Caroline Machado de Oliveira** | Analista de IA e Dev Team (Front/Back)           |
| **Celeste Laura Salvioni** | Desenvolvedora (Dev Team)                        |

## Ferramentas e Tecnologias

O ecossistema é sustentado por uma infraestrutura própria e tecnologias de ponta para garantir baixa latência e escalabilidade:

- **Framework Client (Frontend):** Flutter (Dart)
- **Motor de Inteligência Artificial (The Engine):** FastAPI (Python) orquestrando modelos avançados de Machine Learning (Demucs para separação de áudio, Whisper Turbo + MMS_FA para transcrição e alinhamento *word-level*).
- **Backend e Infraestrutura de Dados:** Supabase (PostgreSQL, Auth e Storage) e Dart (Server-side).
- **Gestão e DevOps:** GitHub Actions (CI/CD) e Docker.
- **Planejamento e tarefas:** [`Google Drive`](https://drive.google.com/drive/folders/1mQ2Xc6IGdEpPH0ltttwKjIytdraUunCP?usp=sharing)

### Justificativa das Escolhas

- **Flutter (Client):** Escolhido pela capacidade de compilação nativa e alta performance na renderização fluida de ondas sonoras (waveforms) e letras sincronizadas em tempo real.
- **FastAPI + Modelos Locais:** Abandonamos APIs genéricas (como music.ai) para criar nosso próprio pipeline de inferência. Isso garante controle absoluto sobre a qualidade da separação de *stems* e sobre o tempo de resposta.
- **Supabase:** Atua como nossa fonte única de verdade (Single Source of Truth) e infraestrutura de persistência, suportando o cache de dados e o armazenamento dos áudios processados.

## ⚡ AI Pipeline Implementado

O motor do sistema conta com uma **Pipeline de Inteligência Artificial** robusta para processamento de áudio! 🎉

- ✅ **Separação de Stems:** Isola vocais principais, backing vocals e instrumentais.
- ✅ **Transcrição Automática:** Gera letras a partir da trilha de voz isolada.
- ✅ **Refinamento com GPT:** Corrige e ajusta a confiabilidade das letras extraídas.
- ✅ **Reconhecimento de Voz:** Associa segmentos específicos da música a diferentes cantores originais.

## 🚀 Performance e Otimização

A arquitetura do motor de IA foi rigorosamente otimizada para entregar resultados em tempo recorde e poupar recursos do usuário final:

- **Processamento Ultra-Rápido:** A pipeline completa processa uma música padrão (~3 minutos) em cerca de **30 segundos**, executando simultaneamente o download, a separação de faixas (stems) e o alinhamento de letras.
- **Eficiência de Dados (Compressão de 90%):** Implementamos uma estratégia de codificação avançada que reduz o tamanho dos arquivos finais de áudio de cerca de 30MB para apenas **3MB**. Isso garante downloads instantâneos no aplicativo móvel e economia drástica nos custos de armazenamento em nuvem.

## 🎤 Singing View & Feedback System

O aplicativo cliente (`melody.io`) possui uma interface de canto rica e interativa:

- ✅ **Letras Sincronizadas:** Estilo clássico de karaoke com destaque visual no tempo exato.
- ✅ **Romanização Global:** Suporte automático para Hangul, Kanji, Hanzi, Cirílico e Árabe.
- ✅ **Track Mixer:** Controle de volume e *mute* individual para cada trilha gerada.
- ⏳ **Real-Time Feedback (Planejado):** Leitura de microfone para avaliar Pitch (afinação), Tempo (ritmo) e Volume do usuário.

## Arquitetura da Aplicação

A arquitetura do "melody" é modularizada e separada por responsabilidades, facilitando a manutenção e a integração entre a inteligência artificial e a interface do usuário.

A estrutura se divide nas seguintes áreas de responsabilidade:

### 1. Camada de Interface (`melody.io`)
O aplicativo cliente (Frontend). Responsável por toda a interação do usuário, pesquisa de músicas, reprodução sincronizada de áudio e letras, geração de waveforms e captura de microfone.

### 2. Camada de API, Orquestração e Cache Persistente (`melody.api`)
O servidor central (Backend) atua não apenas como roteador, mas com uma arquitetura de resiliência ativa. Implementamos um sistema de **cache inteligente** no banco de dados (Supabase). Quando uma música é pesquisada, o sistema verifica o cache local; se existir, os metadados são servidos em menos de 1 segundo. Isso elimina a dependência contínua de provedores externos (evitando bloqueios por *rate limiting* do YouTube) e permite que nosso catálogo cresça organicamente de forma segura.

### 3. Camada de Inteligência Artificial (`melody.ai`)
O núcleo científico do projeto. Contém os scripts e modelos de machine learning que recebem o áudio bruto e devolvem as trilhas separadas (stems) e os metadados de tempo de voz.

### 4. Camada de Provedor de Letras (`melody.ly`)
Microsserviço focado em consumir dados, processar as letras brutas, romanizá-las e refiná-las via modelos de linguagem (GPT).

## Cronograma e Fluxo de Desenvolvimento

### Metodologia

O projeto segue uma metodologia ágil, baseada no framework **Scrum**, conduzida pela Scrum Master (Julia). O desenvolvimento será dividido em **Sprints** quinzenais, com as seguintes etapas:

1.  **Planning:** Definição das metas da Sprint e priorização do Product Backlog pelo PO (Matheus).
2.  **Daily/Sync:** Comunicação contínua da equipe para remover impedimentos.
3.  **Review:** Apresentação das funcionalidades concluídas (como a nova Singing View) para a equipe.
4.  **Retrospectiva:** Reunião para identificar o que funcionou e o que melhorar na próxima iteração de desenvolvimento.

### Documentos

* [Termo de Anuência e Compromisso](https://drive.google.com/file/d/1poLwJX28kVavbTtrcfOr9UHBIrV2zQ25/view?usp=share_link)
* [Documento de Backlog do Produto](https://docs.google.com/document/d/1rOwaxlCfRx9e7oK1dGxd9jt7IT2nbJqfZnb2JKFftK4/edit?usp=share_link)
* [Documento de Planejamento 5W2H](https://docs.google.com/document/d/1cOORKcFZy7MSWDR6SRHwSRMdExmfk4IE8dLYdFu9t5U/edit?usp=share_link)
* [Documento de Plano de Trabalho](https://docs.google.com/document/d/19oqwRuF4SfFkLfUYvrnpepyW21FMppC7yJldUuXTdSQ/edit?usp=share_link)
* [Documento de Histórias de Usuário](https://docs.google.com/document/d/1hvNNnHw9IfnI7sjtTSZsVLjz_mYy9H8d4uIkwzAWWOs/edit?usp=share_link)
* [Documento de Visão](https://docs.google.com/document/d/1AKVcCaHcKl29DUaBqxhA-aPOu1jEFb3AxIE1TYiy22Q/edit?usp=share_link)
* [Documento de Requisitos Funcionais, Não funcionais e Escopo](https://docs.google.com/document/d/136x0oBskko3ewS85kFORf9tAF8z2Qy4vGA1VrqMsO7o/edit?usp=share_link)
* [Documento Proposta de Atividade: ConectaCEUB](https://docs.google.com/document/d/1_nmvFE5YzxxitjNvV4ASwGye5Fp-NsGvNGMFDp0NpH0/edit?usp=share_link)
* [Documento Validação de Campo e Testes de Usabilidade](https://docs.google.com/document/d/1KfEorBiuho7ekO23GrjNGJ4iI36rGXelXAAD4L4iAB0/edit?usp=share_link)
* [Relatório de Evolução Técnica](https://docs.google.com/document/d/1a2jEWa9p_wYsiZVq64iy7Kj82OqPRe89-kv3mtaf89I/edit?usp=share_link)
* [Documento de Retrospectiva](https://docs.google.com/document/d/1x7cy0_jj7ztzeuVHgw9SjfMnE9qD4ppWTBAznQTviZA/edit?usp=share_link)
* [Evidências](https://drive.google.com/drive/folders/1IfNl9kdiFpBMxaB4_vzvmAwixT7AhgEo?usp=share_link) 

<div align="center">
    <p>Feito com ❤️ pela equipe Melody AI</p>
</div>
