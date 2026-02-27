# 🚀 Onboarding Karooma: A Jornada do Alívio

Este documento detalha o fluxo de entrada do novo usuário para garantir que ele sinta o valor da Karoo em menos de 5 minutos.

---

## 🏎️ Fluxo "Fast-to-Value" (WhatsApp/Telegram)

### Passo 1: O Primeiro Contato (O "Oi, Karoo!")
Após o pagamento/cadastro, o usuário recebe um link direto para o WhatsApp da Karoo.
- **Mensagem Inicial da Karoo:**
  > "Olá, [Nome]! 🦘 Que alegria ter você aqui. Eu sou a Karoo, a nova assistente da sua família. Meu objetivo é tirar o peso da rotina dos seus ombros. Vamos começar?"

### Passo 2: O Perfil Familiar & Conexão de Contas
A Karoo faz 3 perguntas rápidas para entender o contexto e solicita as permissões necessárias:

1. **Membros:** "Quem faz parte da sua rotina central? (Ex: Marido, Esposa, Nome dos filhos)."
2. **Conexão de Agenda e E-mail (Oauth Seguro):** 
   > "Para eu gerenciar sua agenda e resumir e-mails da escola, preciso que você me dê um 'crachá' de acesso. Clique no link seguro abaixo para conectar seu Google ou iCloud. É rápido e seus dados ficam blindados pela nossa criptografia."
   - *Mecânica:* A Karoo envia um link para uma página simples de Oauth (Login com Google/Apple).
   - *Privacidade:* Explicamos que o acesso é restrito aos escopos de Calendário e Leitura de E-mail (opcional), seguindo o **Selo de Segurança Karoo**.
3. **Ponto de Dor:** "Qual é a coisa que mais te sobrecarrega hoje? (Ex: Lista de compras, grupos de escola, ou esquecer compromissos)."

---

## 📧 Configurações de E-mail: Por que e Como?

A Karoo solicita acesso ao e-mail para atuar como um **Filtro de Ruído Escolar/Burocrático**.

- **Modo de Requisição:** Nunca pedimos a senha. Pedimos a autorização via Oauth (botão "Entrar com Google").
- **Filtros Inteligentes:** O usuário pode configurar: "Karoo, só leia e-mails que venham do domínio `@escola.com.br` ou que contenham a palavra 'Boleto'".
- **Resumo Proativo:** "Recebi um e-mail da escola. O passeio de sexta foi confirmado e o valor é R$ 50. Quer que eu agende o pagamento?"
- **Segurança:** O acesso é feito via Tokens temporários que o usuário pode revogar a qualquer momento nas configurações do Google/Apple.

### Passo 3: O Primeiro "Uau" (A Transcrição)
A Karoo desafia o usuário:
- *"Mande um áudio agora, do jeito que vier à cabeça, sobre algo que você precisa organizar ou comprar hoje. Não se preocupe com a bagunça na fala!"*
- O usuário manda o áudio -> Karoo usa **Whisper** -> Karoo devolve: *"Entendido! Já coloquei [Item] na lista e marquei [Evento] na agenda. Viu como é fácil?"*

### Passo 4: Conectando o Parceiro(a)
- Karoo: *"Para a mágica ser completa, preciso falar com o seu braço direito. Pode me passar o contato dele(a) ou encaminhar este link de convite?"*
- Quando o parceiro entra, a Karoo se apresenta como a ponte entre os dois.

---

## 🛠️ Checklist Técnico de Onboarding

| Etapa | Ferramenta/Skill | Objetivo |
| :--- | :--- | :--- |
| **Boas-vindas** | Telegram/WACli | Gerar empatia e segurança. |
| **Sincronia** | Google/Apple API | Centralizar a "Fonte da Verdade" (Agenda). |
| **Amostra Grátis** | Whisper + LLM | Mostrar a inteligência de transcrição imediata. |
| **Ponte** | Message Tool | Ativar a comunicação entre o casal. |

---

## 🎯 Métricas de Sucesso do Onboarding (Aha! Moment)
O onboarding é considerado bem-sucedido quando:
1. O usuário manda o primeiro áudio e recebe a confirmação correta.
2. A agenda comum é conectada com sucesso.
3. O parceiro(a) aceita o convite e interage com a Karoo.

---
*Documento de Estratégia Karooma - 2026*
