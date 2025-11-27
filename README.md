PRD
#########################################################################################

🎮 FinQuest — MVP Gamificado

Quero criar um aplicativo chamado FinQuest, focado em jovens e gamificação, para oferecer um diagnóstico financeiro em formato de jogo.
Abaixo está o PRD completo usado para gerar o MVP com fluxo de telas, lógica e componentes.

📌 Contexto

O FinQuest é um app de educação financeira gamificada.
A jornada do usuário funciona como um RPG financeiro, onde ele passa por níveis, recebe missões e sobe de ranking conforme organiza sua vida financeira.

Toda interação é conduzida por IA via chat, de forma leve, simples e motivadora.

🎯 Objetivo Principal

Criar um MVP funcional com:

fluxo de chat,
telas de progresso,
e uma "pizza de investimentos" para usuários classificados como poupadores.

🧑‍💻 Público-alvo

Jovens 16 a 30 anos que querem aprender finanças de um jeito:

fácil
prático
gamificado

Principalmente iniciantes que não gostam de planilhas ou apps complexos.

🏆 Níveis Financeiros (Gamificação)

O usuário progride nos níveis conforme responde às perguntas e cumpre missões:

🟥 Sobrevivente (endividado)
🟧 Equilibrado
🟨 Planejador
🟩 Investidor
🟦 Mestre (referência futura)

Cada nível libera novas missões.

🗺️ Missões do App
⚡ Missão Corte Rápido – cortar gastos de uma categoria
💳 Missão Cartão Único – usar apenas um cartão sem anuidade
💼 Missão Reserva – montar reserva de emergência
🎯 Missão Perfil de Investidor – definir perfil
📊 Missão Pizza de Investimentos – aprender cada classe de ativo
⏳ Missão Previdência Inteligente – aprender a “pagar-se primeiro”
📈 Score Financeiro

O app calcula um Score FinQuest (0–1000) baseado em:

renda
gastos estimados
dívidas
existência de reserva
missões cumpridas

🧭 Fluxo do App (MVP)
🟦 Tela 1 — Onboarding

Explica que o app é um jogo de evolução financeira

Botão “Começar”

🟪 Tela 2 — Chat com IA (Diagnóstico Rápido)

IA pergunta, uma por vez:

Renda líquida
Valor da fatura do cartão
Tem dívidas?
Está no SPC/Serasa?
Quantos cartões usa?
Tem reserva de emergência?

A IA classifica automaticamente o nível inicial.

🟩 Tela 3 — Bens e Objetivos

Perguntas simples:

Tem moto, carro ou casa?
Está quitado?
Quer comprar algum dos três nos próximos 12 meses?
Se sim → sugerir consórcio como alternativa educativa.

🟨 Tela 4 — Caminhos

Se for Sobrevivente

IA libera missões:

Corte Rápido
Cartão Único
30 Dias no Verde
Se for Poupador / Planejador

IA inicia a Análise de Perfil de Investidor

🟧 Tela 5 — Análise de Perfil

Perguntas rápidas:

Prazo
Tolerância ao risco
Objetivos
Conhecimento

Classificação:

Conservador
Moderado
Arrojado

🟦 Tela 6 — Pizza de Investimentos

Mostrar gráfico com:

Tesouro
CDB/LCI
Fundos
Previdência
ETFs / ações

Cada fatia abre uma explicação educativa simples.

🟩 Tela 7 — Trilhas Educativas

Aulas curtas sobre:

Renda fixa
Renda variável
Fundos
Previdência (foco em “pague-se primeiro”)

🟫 Tela 8 — Painel do Jogador

Exibe:

Score FinQuest
Nível atual
Missões abertas
Progresso semanal
Botão “Falar com IA”

🔧 Funcionalidades-Chave do MVP

Chat com IA conduzindo toda a jornada
Diagnóstico automático com poucas perguntas
Classificação por nível financeiro
Missões básicas para evolução
Análise de perfil de investidor
Pizza de investimentos
Painel com ranking, missões e score

🛠️ Tarefas para o Lovable

Criar o fluxo de telas completo
Interface moderna, estilo jovem/gamer
Componentes obrigatórios:
Tela de chat
Tela de missões
Painel de score
Pizza de investimentos
Níveis do jogador
Criar lógica básica de:
classificação de nível
score inicial
exibição de missões
Criar estrutura navegável (mesmo sem backend real)

🧠 Tom da IA do FinQuest

A IA deve ser:

simples
motivadora
objetiva
zero formalidade
estilo “consultor amigo”

Exemplo de tom:

“Bora ver em que nível financeiro você está? Nada de julgamento — é só o começo da sua jornada.”

🚀 Entregável Esperado

Quero um MVP navegável com:

telas
chat
missões
score
pizza de investimentos
navegação funcional

Tudo simples, leve e gamificado.

###############################################################################################

TELAS

<img width="572" height="751" alt="Captura de tela 2025-11-27 072619" src="https://github.com/user-attachments/assets/1e1850e2-be76-4733-a4c6-d5f0c5e14fb0" />

<img width="663" height="731" alt="Captura de tela 2025-11-27 072639" src="https://github.com/user-attachments/assets/d7d0b396-b9b1-4ee7-9e65-c3b8d7d9b8b9" />

<img width="638" height="707" alt="Captura de tela 2025-11-27 072651" src="https://github.com/user-attachments/assets/24507378-9294-49e3-b1a5-245c8a44b657" />

<img width="557" height="723" alt="Captura de tela 2025-11-27 072703" src="https://github.com/user-attachments/assets/2f56e72c-1ac1-4fa0-a7a6-33048b8467c1" />

<img width="678" height="715" alt="Captura de tela 2025-11-27 072717" src="https://github.com/user-attachments/assets/c6e5c28b-3464-4804-80a0-b8302fb6b098" />

<img width="752" height="750" alt="Captura de tela 2025-11-27 072727" src="https://github.com/user-attachments/assets/9d0104bc-2f66-4fbf-b819-e6b00c8c6b8c" />

<img width="715" height="713" alt="Captura de tela 2025-11-27 072736" src="https://github.com/user-attachments/assets/35e8f95a-34fb-49b3-982c-dcc727c0a7eb" />

<img width="673" height="739" alt="Captura de tela 2025-11-27 072755" src="https://github.com/user-attachments/assets/9540e80a-af09-4691-bcd9-23e7795765ab" />

############################################################################################











