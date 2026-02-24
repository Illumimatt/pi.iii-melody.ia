<h3 align="center">projeto.integrador.iii</h3>
<p align="center"> Este projeto integrador está sendo desenvolvido como parte do curso de Ciência da Computação da Universidade CEUB e tem como objetivo o desenvolvimento de uma plataforma de karaoke impulsionada por IA, do conceito ao lançamento. </p>

<p align="center">
  <img src="https://img.shields.io/badge/status-Em%20Desenvolvimento-yellow" alt="Status do Projeto: Em Desenvolvimento">
  <img src="https://img.shields.io/badge/framework-Flutter-blue?logo=flutter" alt="Framework: Flutter">
  <img src="https://img.shields.io/badge/tech-Python_IA-black?logo=python" alt="Tech: Python">
</p>

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

O projeto será desenvolvido e acompanhado com as seguintes ferramentas:

- **Gestão e Código-fonte:** GitHub
- - **Planejamento e tarefas:** [`Google Drive`](https://drive.google.com/drive/folders/1mQ2Xc6IGdEpPH0ltttwKjIytdraUunCP?usp=sharing)
- **Framework Client:** Flutter (Dart)
- **APIs e Serviços Externos:** Genius API e music.ai
- **Processamento de Áudio Visual:** Algoritmo audiowaveform (BBC)
- **IA e NLP:** Modelos GPT (Correção de letras)

### Justificativa das Escolhas

- **Flutter (Client):** Escolhido pela sua capacidade de compilar nativamente para múltiplas plataformas (Mobile e Web) a partir de um único código-base, essencial para alcançar o maior número de usuários no aplicativo `melody.io`.
- **Arquitetura de Microsserviços:** A divisão em repositórios (`.ai`, `.api`, `.ly`, `.io`) permite que a equipe de IA trabalhe de forma isolada nos modelos em Python/PyTorch, enquanto a interface consome os dados via requisições assíncronas, garantindo escalabilidade.

## ⚡ AI Pipeline Implementado

O motor do sistema conta com uma **Pipeline de Inteligência Artificial** robusta para processamento de áudio! 🎉

- ✅ **Separação de Stems:** Isola vocais principais, backing vocals e instrumentais.
- ✅ **Transcrição Automática:** Gera letras a partir da trilha de voz isolada.
- ✅ **Refinamento com GPT:** Corrige e ajusta a confiabilidade das letras extraídas.
- ✅ **Reconhecimento de Voz:** Associa segmentos específicos da música a diferentes cantores originais.

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

### 2. Camada de API e Orquestração (`melody.api`)
O servidor central (Backend). Atua como intermediário, gerenciando contas de usuário, salvando projetos (clips e presets) e roteando as requisições de processamento de áudio para os módulos corretos.

### 3. Camada de Inteligência Artificial (`melody.ai`)
O núcleo científico do projeto. Contém os scripts e modelos de machine learning que recebem o áudio bruto e devolvem as trilhas separadas (stems) e os metadados de tempo de voz.

### 4. Camada de Provedor de Letras (`melody.ly`)
Microsserviço focado em consumir dados da Genius API, processar as letras brutas, romanizá-las e refiná-las via modelos de linguagem (GPT).

## Cronograma e Fluxo de Desenvolvimento

### Metodologia

O projeto segue uma metodologia ágil, baseada no framework **Scrum**, conduzida pela Scrum Master (Julia). O desenvolvimento será dividido em **Sprints** quinzenais, com as seguintes etapas:

1.  **Planning:** Definição das metas da Sprint e priorização do Product Backlog pelo PO (Matheus).
2.  **Daily/Sync:** Comunicação contínua da equipe para remover impedimentos.
3.  **Review:** Apresentação das funcionalidades concluídas (como a nova Singing View) para a equipe.
4.  **Retrospectiva:** Reunião para identificar o que funcionou e o que melhorar na próxima iteração de desenvolvimento.

<div align="center">
    <p>Feito com ❤️ pela equipe do Projeto Integrador</p>
</div>
