# 📝 Estrutura de Cadastro Karooma (Onboarding Inicial)

Este documento define os campos e a lógica de captura de dados para transformar um visitante da Landing Page em um usuário ativo da Karú, minimizando a fricção.

---

## 🏗️ Nível 1: Captura de Lead (Landing Page)
*Objetivo: Criar compromisso e urgência sem cansar o usuário.*

- **E-mail Principal:** (Para comunicações oficiais e faturamento).
- **Nome do Usuário:** (Como ele gosta de ser chamado).
- **Celular (WhatsApp/Telegram):** (Campo crítico onde a Karú irá "morar").

---

## 🏗️ Nível 2: O Perfil Familiar (Primeiro Chat com a Karú)
*Objetivo: Humanizar a assistente e configurar a entrega de valor. Realizado via conversação.*

1. **Pronúncia Fonética:**
   - *"Toshio, para eu não errar seu nome nos nossos áudios, escreva aqui como eu devo falar ele (Ex: Toshio = To-shi-o)."*
   
2. **O "Braço Direito" (Parceiro/a):**
   - *"Quem é a pessoa que divide a rotina com você? Me passe o nome e o contato dela para eu criar nossa Ponte Familiar."*

3. **Membros Adicionais:**
   - *"Quais são os nomes e idades dos seus filhos (ou pets)? Isso me ajuda a filtrar ofertas de fraldas e produtos certos para você."*

4. **Conexão de Fonte da Verdade:**
   - **Agenda:** Autorização Oauth para Google Calendar ou iCloud.
   - **E-mail Escola:** (Opcional) Cadastro do remetente da escola para resumos automáticos.

---

## 🏗️ Nível 3: Preferências de Interface (A "Personalidade" da Karú)
*Objetivo: Ajustar o KaaS ao estilo de vida do usuário.*

- **Modo de Resposta:** 
    - [ ] Apenas Texto (Rápido/Discreto).
    - [ ] Híbrido: Texto + Botão de Voz (Economia).
    - [ ] Full Voice: Texto + Áudio Automático (Concierge).
- **Horário de Silêncio:**
    - *"Em qual horário você quer que eu fique 'no mudo' para não atrapalhar o sono da família?"*

---

## 🛠️ Checklist de Implementação Técnica

| Campo | Validação | Ferramenta |
| :--- | :--- | :--- |
| **WhatsApp/Telegram** | Verificação via código SMS/OTP | Twilio / WACli |
| **Agenda/E-mail** | Consentimento Oauth 2.0 | Google Cloud / Apple Dev |
| **Nomes Fonéticos** | Armazenamento no `Dicionário de Pronúncia` | Skill Edge-TTS Custom |

---
*Documento de Estratégia de Cadastro - Karooma 2026*
