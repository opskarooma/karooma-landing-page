# 🧠 Algoritmo de Compra Inteligente Karooma (V1)

Este documento define a lógica de decisão que o Agente Atlas utiliza para consolidar carrinhos de compras, otimizar fretes e reduzir a sobrecarga mental da família.

---

## 🏎️ 1. O Gatilho de Compra
A Karoo inicia o processo de fechamento quando:
- A meta de Frete Grátis é atingida por itens da lista atual.
- Um item crítico da lista entra em "Oferta Relâmpago".
- O usuário solicita: "Karoo, fecha a compra da semana".

---

## ⚙️ 2. Lógica de Consolidação (Regras de Desempate)

O Atlas deve calcular o **Custo Total Efetivo (CTE)** para cada cenário de loja:
`CTE = (Soma dos Preços) + (Frete) - (Desconto de Afiliação/Cashback)`

### Hierarquia de Decisão:
1.  **Prioridade 1: Meta de Frete Grátis.** Se faltar menos de 20% do valor para frete grátis, o Atlas DEVE buscar itens no histórico de cadência (café, fraldas, limpeza) para completar o carrinho.
2.  **Prioridade 2: Conveniência de Entrega.** Se a diferença de preço entre "Comprar tudo em 1 loja" vs "Dividir em 2 lojas" for menor que R$ 15,00, a Karoo recomendará o **Carrinho Único** (menos logística de recebimento).
3.  **Prioridade 3: Cashback/Afiliação.** Em caso de empate técnico de preço e frete, a Karoo prioriza o link que gera maior comissão para o ecossistema Karooma.

---

## 📉 3. Tabela de Sensibilidade ao Frete

| Diferença de Preço | Decisão Sugerida | Justificativa UX |
| :--- | :--- | :--- |
| Até R$ 10 | Manter na loja principal | Economia de tempo > Pequeno desconto. |
| R$ 11 a R$ 30 | Sugerir divisão de cestas | Equilíbrio entre economia e esforço. |
| Acima de R$ 31 | Forçar troca de loja | Economia significativa para o orçamento mensal. |

---

## 🔮 4. O "Item do Futuro" (Predição)
Sempre que o carrinho for fechado, o Atlas deve analisar:
- **Cadência de Uso:** "Este item costuma ser comprado a cada X dias?"
- **Estoque Estimado:** "Pelo histórico, o [Produto Y] deve acabar em 5 dias."
- **Ação:** Inserir um card de áudio: *"Toshio, notei que o sabão em pó está para acabar semana que vem. Quer colocar ele agora para aproveitar o frete de hoje?"*

---

## 🛠️ Stack Técnica
- **Motor de Raciocínio:** Kimi K2.5 (devido à longa memória e análise multivariável).
- **Banco de Dados:** `shopping_cadence.json` (Histórico de frequência).
- **Interface:** Carrinho Blindado via API Amazon/ML.

---
*Desenvolvido pela Inteligência Karooma - 2026*
