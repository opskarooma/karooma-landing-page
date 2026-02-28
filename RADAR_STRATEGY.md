# 🛒 Estratégia Técnica: Radar de Ofertas Karooma

O Radar de Ofertas é o "motor de economia" da Karooma, transformando a Karú em uma assistente proativa que ajuda a pagar a própria assinatura.

---

## 🏗️ 1. O Fluxo do Usuário (UX)
1. **Ativação:** O usuário diz: "Karú, monitora o preço da Fralda Pampers G. Me avisa se baixar de R$ 80".
2. **Confirmação:** A Karú identifica o produto, gera o link blindado (Associates) e confirma: "Entendido! Estou vigiando a Fralda Pampers G para você. ✅"
3. **Alerta Proativo:** Quando o preço cai, a Karú envia: "🔥 Oferta! A Fralda que você queria baixou para R$ 75. [Link Blindado para Compra]"

---

## 🛠️ 2. A Lógica Técnica (O "Pulo do Gato")

### Nível A: O Link Blindado (Segurança de Comissão)
Para evitar o erro "Something went wrong" da Amazon e garantir sua comissão:
- **Formato:** `https://www.amazon.com.br/dp/[ASIN]/?tag=karoom-20`
- O Agente **Atlas** será responsável por converter links brutos ou nomes de produtos em links limpos com o seu ID.

### Nível B: O Monitoramento (Backend)
Como não podemos sobrecarregar a VPS fazendo "scraping" a cada minuto:
1. **Periodicidade:** O Atlas checa os preços 2x por dia (Madrugada e Meio-dia).
2. **Ferramenta:** Usaremos a skill `web_fetch` ou uma integração simples com a **API de Afiliados da Amazon** (mais estável).
3. **Filtro de Relevância:** Só enviamos o áudio/mensagem se o desconto for real (> 5% ou abaixo do teto definido pelo usuário).

---

## 🧠 3. O Papel do Agente Atlas
O Atlas gerenciará uma lista chamada `radar_status.json`:
```json
{
  "user_id": "opskarooma",
  "items": [
    {
      "asin": "B07PBXXXX",
      "name": "Fralda Pampers G",
      "target_price": 80.00,
      "last_price": 89.90,
      "link": "https://www.amazon.com.br/dp/B07PBXXXX/?tag=karoom-20"
    }
  ]
}
```

---

## 🚀 Próximos Passos
1. **Criar a Skill Custom `karooma-radar`**: Um script simples em Python/Node que lê essa lista e checa os preços.
2. **Ajustar o Prompt da Karú**: Para que ela saiba "vender" esse benefício durante a conversa.

---
*Documento de Engenharia Karooma - 2026*
