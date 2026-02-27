# 💰 Estratégia de Precificação e Pacotes - Karooma.life

Este documento consolida a estrutura de monetização e os níveis de serviço da Karooma, focada em entregar alívio mental para famílias através da IA.

---

## 🎯 Filosofia de Preço
- **Foco:** Baixa barreira de entrada e alto valor percebido (ROI de tempo/energia).
- **Modelo:** Assinatura mensal recorrente (SaaS).
- **Interface:** 100% via WhatsApp/Telegram.

---

### 🔄 Benefício Transversal: Karoo Intelligence (IA Everywhere)
*Disponível em todos os planos como base da interação.*

A Karoo não é apenas um bot de comandos; ela é uma IA de última geração (KaaS) integrada à rotina familiar. O usuário tem acesso a:
- **Pesquisa Contextual:** "Karoo, onde tem uma farmácia 24h aberta agora?" ou "Quais são os melhores parques infantis nesta região?"
- **Consultoria de Cuidado:** "Como tirar mancha de canetinha do sofá?" ou "Sugestões de lanche saudável para a lancheira escolar."
- **Síntese de Conhecimento:** "Resuma para mim as principais mudanças na lei de cadeirinhas de carro."
- **Modo 'Brainstorm':** Ajuda para planejar festas de aniversário, roteiros de viagem em família ou cardápios semanais.
- **Aprendizado de Contexto:** A Karoo entende o histórico da família para dar respostas cada vez mais precisas e personalizadas.

---

### ⚙️ O Motor Karooma: Orquestração Inteligente de LLMs (KaaS)
*Eficiência invisível: Qualidade máxima com custo otimizado.*

Sob o capô, a Karoo utiliza uma infraestrutura de **Orquestração Dinâmica de Modelos** (via OpenRouter), garantindo que cada tarefa seja processada pela IA mais capaz para aquele contexto específico:
- **Tarefas Rápidas (Sincronia/Agendas):** Processadas por modelos ultra-velozes (como Gemini 3 Flash), garantindo resposta instantânea.
- **Consultoria Complexa (Planejamento/Análise):** Para roteiros de viagem ou conselhos de cuidado, o sistema escala automaticamente para modelos de raciocínio profundo (como DeepSeek-V3 ou Claude 3.5 Sonnet).
- **Transcrição de Alta Fidelidade:** Integração do Whisper com modelos de correção gramatical para garantir que o áudio vire texto impecável.
- **Otimização de Custo:** A inteligência da Karoo seleciona o modelo com o melhor custo-benefício de tokens, permitindo manter os preços dos planos competitivos sem perder a qualidade premium.

---

## 📦 Detalhamento dos Pacotes

### 1. Plano SOSSEGO (O "Pé na Porta")
*Foco: Organização passiva e sincronia básica.*

- **Valor:** **R$ 19,00 / mês**
- **Entrega de Valor:** Eliminar o "esqueci de anotar/comprar".
- **Recursos Detalhados:**
    - **Interface:** Chat via WhatsApp ou Telegram (Entrada: Texto e Áudio).
    - **Karoo Intelligence:** Acesso à IA para pesquisas rápidas e dúvidas do dia a dia.
    - **Orquestração KaaS (Básico):** Uso de modelos de alta velocidade para respostas instantâneas.
    - **Transcrição:** Uso do Whisper para converter áudios do usuário em texto.
    - **Agenda Comum:** Sincronização de um calendário compartilhado (Google/Apple) para o casal.
    - **Lista de Compras:** Gestão de uma lista única acessível por ambos.
    - **Loop de Segurança:** A Karoo sempre confirma o que entendeu antes de agendar ou listar.

### 2. Plano FLUXO (O "Melhor Valor")
*Foco: Inteligência ativa e economia de tempo/dinheiro.*

- **Valor:** **R$ 49,00 / mês**
- **Entrega de Valor:** Reduzir a carga mental e economizar em compras recorrentes.
- **Recursos Detalhados:**
    - **Tudo do Plano Sossego.**
    - **Orquestração KaaS (Avançado):** Acesso automático a modelos especialistas (Claude/DeepSeek) para consultas complexas de saúde, educação ou planejamento.
    - **Radar de Ofertas:** Monitoramento automático de preços para itens da lista de compras (Fraldas, Leite, etc) com avisos de queda de preço.
    - **Resumo de Grupos Escolares:** Você encaminha as mensagens do grupo e a Karoo extrai datas, materiais e eventos importantes.
    - **Transcrição Ilimitada:** Prioridade no processamento de áudios longos.
    - **Ponte Familiar Ativa:** Envio de mensagens curtas de alinhamento para o parceiro(a) com um clique.

### 3. Plano TOTAL (O "Concierge Digital")
*Foco: Gestão de vida 360º e interface multimodal.*

- **Valor:** **R$ 99,00 / mês**
- **Entrega de Valor:** Delegar a burocracia e ter uma assistente que "fala" com você.
- **Recursos Detalhados:**
    - **Tudo do Plano Fluxo.**
    - **Orquestração KaaS (Premium):** Prioridade máxima de processamento e acesso aos modelos mais potentes do mercado sem restrições.
    - **Karoo Voice (Saída):** A Karoo responde com áudios curtos (TTS), ideal para ouvir enquanto dirige ou cuida das crianças.
    - **Gestão de Documentos:** Alertas preventivos para renovação de documentos (RG, CNH, Passaporte) e datas de saúde (vacinas, exames recorrentes).
    - **Módulos Personalizados:** Criação de um fluxo de automação exclusivo para a necessidade específica da sua casa.
    - **Canal de Co-criação:** Linha direta para sugerir e testar novas ferramentas do ecossistema Karooma.

---

## 🛠 Matriz de Custo (Back-end)
*Estratégia para manter a margem operacional:*

| Recurso | Nível de Custo | Estratégia de Uso |
| :--- | :--- | :--- |
| **Texto (LLM)** | Baixíssimo | Uso de Gemini 3 Flash / Flash-Lite. |
| **Transcrição (Whisper)** | Baixo | Processamento local ou via API rápida. |
| **Voz (TTS)** | Médio/Alto | Exclusivo para planos **Fluxo/Total** para proteger a margem. |
| **Sincronia de Agenda** | Baixo | Integração via API Google/Apple. |

---

## 📈 Próximos Passos
1. Validar a aceitação do plano de R$ 19,00 com os primeiros 10 usuários Beta.
2. Monitorar o custo de API de voz no plano Total para ajustar limites de uso, se necessário.
3. Criar a página de checkout (Stripe/Pix) integrada a estes valores.

---
*Atualizado em: 26 de Fevereiro de 2026*
