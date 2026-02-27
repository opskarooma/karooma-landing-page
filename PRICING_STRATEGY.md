# 💰 Estratégia de Precificação e Pacotes - Karooma.life

Este documento consolida a estrutura de monetização e os níveis de serviço da Karooma, focada em entregar alívio mental para famílias através da IA.

---

## 🎯 Filosofia de Preço
- **Foco:** Baixa barreira de entrada e alto valor percebido (ROI de tempo/energia).
- **Modelo:** Assinatura mensal recorrente (SaaS).
- **Interface:** 100% via WhatsApp/Telegram.

---

## 📦 Detalhamento dos Pacotes

### 1. Plano SOSSEGO (O "Pé na Porta")
*Ideal para famílias que precisam organizar o básico sem complicação.*

- **Valor:** **R$ 19,00 / mês**
- **Recursos Inclusos:**
    - Interface via WhatsApp/Telegram.
    - Transcrição de Áudios (Whisper) limitada.
    - Agenda Familiar Sincronizada (2 usuários).
    - Lista de Compras Compartilhada.
    - Protocolo de Confirmação (Loop de segurança).

### 2. Plano FLUXO (O "Melhor Valor")
*Ideal para o dia a dia intenso, onde a IA atua de forma proativa.*

- **Valor:** **R$ 49,00 / mês**
- **Recursos Inclusos:**
    - **Tudo do Plano Sossego.**
    - Transcrição de Áudios ilimitada.
    - **Radar de Ofertas Ativo:** Monitoramento de preços de itens essenciais.
    - **Resumo de Grupos:** Resumos inteligentes de grupos de escola e família.
    - **Detecção de Incerteza:** A Karoo pergunta se não entender algo devido a ruído.

### 3. Plano TOTAL (O "Concierge Digital")
*Experiência completa com suporte multimodal e evolução personalizada.*

- **Valor:** **R$ 99,00 / mês**
- **Recursos Inclusos:**
    - **Tudo do Plano Fluxo.**
    - **Karoo Voice (Multimodal):** Respostas da Karoo em áudio (TTS) para ouvir no carro.
    - **Gestão de Documentos:** Alertas de prazos (vacinas, exames, renovações).
    - **Suporte Prioritário:** Canal direto para dúvidas e ajustes de rotina.
    - **Co-criação Beta:** Acesso a novas ferramentas antes do lançamento oficial.

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
