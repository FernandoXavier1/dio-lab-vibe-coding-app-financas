
# 🎮 **FinQuest — Seu RPG de Educação Financeira**

Projeto desenvolvido no **Desafio Vibe Coding da DIO**, utilizando **Lovable** e **Copilot Web** para criar um app de **diagnóstico financeiro gamificado**.
A proposta é simples: transformar sua vida financeira em um **jogo** com níveis, missões e evolução guiada por IA.

---

## 🧠 **Visão Geral**

O FinQuest é um app onde o usuário conversa com uma IA que:

* analisa sua situação financeira
* define seu nível (Sobrevivente → Investidor)
* libera missões
* explica conceitos de forma simples
* ajuda a montar uma estratégia de evolução

Tudo em um fluxo leve, divertido e sem burocracia.

---

## 🎯 **Funcionalidades Principais**

* 💬 **Chat com IA** para diagnóstico
* 🏅 **Níveis financeiros** para acompanhar evolução
* 🗺️ **Missões práticas** (corte rápido, cartão único, reserva)
* 📊 **Pizza de Investimentos** explicada de forma simples
* 🔍 **Perfil de investidor** (Conservador / Moderado / Arrojado)
* 📈 **Score FinQuest (0–1000)**
* 🎓 **Trilhas educativas** curtas e diretas

---

## 💬 **Como usei o Lovable**

Usei prompts refinados no **Copilot Web** e enviei para o **Lovable**, que gerou:

* telas do fluxo completo
* chat funcional
* painel de evolução
* pizza de investimentos
* lógica básica de níveis, missões e score

FINQUEST (MVP GAMIFICADO)

Quero gerar um MVP chamado FinQuest, um aplicativo mobile com foco em jovens (16–30 anos) que transforma um diagnóstico financeiro em uma jornada gamificada baseada em níveis, missões e educação financeira guiada por IA.

Arquitetura Geral do MVP

Front-end: fluxo conversacional + telas de progresso.

Lógica local: classificação financeira, score, níveis, missões e exibição das trilhas.

Sem backend complexo: apenas persistência local/estados mockados.

Componentes essenciais:

Chat com IA

Tela de Missões

Dashboard (nível, score, progresso)

Tela de Bens/Objetivos

Perfil de investidor

“Pizza de Investimentos” (gráfico de composição)

Fluxo Técnico do App

Onboarding

Tela de apresentação com explicação breve do conceito (“RPG financeiro”).

Botão de iniciar → leva para o chat com IA.

Armazena estado inicial do usuário (level = null, score = 0).

Chat — Módulo de Diagnóstico

IA faz perguntas sequenciais (usar mensagens e UI de input curto):

Renda líquida

Fatura do cartão

Dívidas (boolean + valor opcional)

Status SPC/Serasa

Quantos cartões utiliza

Tem reserva (boolean)

Regras de classificação (lógica local):

Dívida alta ou gasto > renda → Sobrevivente

Fatura equilibrada → Equilibrado

Reserva + controle básico → Planejador

Sobra mensal + interesse em investir → Investidor

Armazenar resultado em user.level.

Tela de Bens e Objetivos

Inputs simples: moto, carro, casa, quitado/financiado, e intenção de compra.

Se intenção = true → liberar componente informativo sobre consórcio.

Trilhas (Baseadas no Nível)

Se user.level = “Sobrevivente”

Gerar lista de missões:

Missão Corte Rápido (reduzir gasto em categoria X)

Missão Cartão Único (educação sobre cartão sem anuidade)

Missão 30 Dias no Verde

Se user.level = “Equilibrado” ou “Planejador”

Mostrar trilha para organização e reserva.

Se user.level = “Investidor”

Abrir módulo Perfil de Investidor.

Perfil de Investidor

Perguntas (risco, prazo, objetivos, conhecimento).

Classificação:

Conservador

Moderado

Arrojado

Armazenar em user.investorProfile.

Pizza de Investimentos

Gerar gráfico (componente “pie chart”) com as fatias:

Tesouro

CDB

LCI/LCA

Fundos

Previdência

ETFs/Ações

Peso das fatias baseado no user.investorProfile.

Cada clique abre card explicativo (texto curto).

Trilhas Educativas

Módulo com cards:

Renda fixa

Variável

Fundos

Previdência (“pague-se primeiro”)

Dashboard (Painel do Jogador)

Score FinQuest (0–1000): calculado por fórmula simples:

score = base + missões cumpridas + nível + consistência

Exibição dos níveis

Missões pendentes

Botão para reabrir o chat com IA

Comportamento da IA

Deve conduzir todas as etapas por chat.

Estilo: curto, direto, motivador.

Deve validar entradas básicas (tipo renda numérica).

Deve disparar rotas no fluxo conforme respostas.

Pode oferecer resumo semanal: detecção simples baseada nas respostas salvas localmente (mock).

Requisitos Visuais

Interface jovem, cores vibrantes.

Elementos de RPG: níveis, barras de progresso, badges.

Componentes limpos e minimalistas.

“Pizza de Investimentos” com cores distintas e acessíveis.

Entregável Requerido

Gerar:

Fluxo de telas completo

Navegação entre telas

Chat funcional (mock)

Dashboard com score

Módulo de missões

Módulo de perfil de investidor

Módulo da pizza de investimentos

Persistência simples de estado (sem backend real)

---

## 🎯 **Telas**

<img width="572" height="751" alt="Captura de tela 2025-11-27 072619" src="https://github.com/user-attachments/assets/1e1850e2-be76-4733-a4c6-d5f0c5e14fb0" />

<img width="663" height="731" alt="Captura de tela 2025-11-27 072639" src="https://github.com/user-attachments/assets/d7d0b396-b9b1-4ee7-9e65-c3b8d7d9b8b9" />

<img width="638" height="707" alt="Captura de tela 2025-11-27 072651" src="https://github.com/user-attachments/assets/24507378-9294-49e3-b1a5-245c8a44b657" />

<img width="557" height="723" alt="Captura de tela 2025-11-27 072703" src="https://github.com/user-attachments/assets/2f56e72c-1ac1-4fa0-a7a6-33048b8467c1" />

<img width="678" height="715" alt="Captura de tela 2025-11-27 072717" src="https://github.com/user-attachments/assets/c6e5c28b-3464-4804-80a0-b8302fb6b098" />

<img width="752" height="750" alt="Captura de tela 2025-11-27 072727" src="https://github.com/user-attachments/assets/9d0104bc-2f66-4fbf-b819-e6b00c8c6b8c" />

<img width="715" height="713" alt="Captura de tela 2025-11-27 072736" src="https://github.com/user-attachments/assets/35e8f95a-34fb-49b3-982c-dcc727c0a7eb" />

<img width="673" height="739" alt="Captura de tela 2025-11-27 072755" src="https://github.com/user-attachments/assets/9540e80a-af09-4691-bcd9-23e7795765ab" />

---

## 🧠 **Reflexão Rápida**

* **O que funcionou:** PRD refinado → interações mais eficientes no Lovable.
* **Desafio:** O app funcionou bem nas primeiras interações, mas não conseguiu gerar o diagnóstico financeiro.
* **Aprendizado:** O projeto precisa de mais desenvolvimento.















