
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

---

## 💻 **PROMPT FINQUEST (MVP GAMIFICADO)**

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

## 🔍 **Telas**

<img width="3008" height="1502" alt="capturas" src="https://github.com/user-attachments/assets/4583d489-7522-4a89-8ebc-51099a4d2219" />

---

## 🧠 **Reflexão Rápida**

* **O que funcionou:** PRD refinado → interações mais eficientes no Lovable.
* **Desafio:** O app funcionou bem nas primeiras interações, mas não conseguiu gerar o diagnóstico financeiro.
* **Aprendizado:** O projeto precisa de mais desenvolvimento.















