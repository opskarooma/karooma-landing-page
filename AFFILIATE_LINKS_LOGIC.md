# 🛒 Karooma Radar: Registro de Atribuição de Links

Este documento serve como a base de dados para o Agente Atlas injetar corretamente os IDs de afiliado conforme a plataforma detectada pelo Radar.

---

## 🔑 Credenciais de Atribuição (IDs de Afiliado)

| Plataforma       | ID / Tag de Afiliado     | Método de Injeção                     |
| :--------------- | :----------------------- | :------------------------------------ |
| **Amazon BR**    | `karoom-20`              | Parâmetro URL: `?tag=karoom-20`       |
| **Mercado Livre**| `opskarooma`             | API / Link Curto via Painel           |
| **Shopee BR**    | [Aguardando Ativação API]| Injeção via Shopee Open API           |
| **Magalu**       | `karoo.ofertas`          | Link da Vitrine / Sub-ID              |
| **SocialSoul**   | [Aguardando Cadastro]    | Deep Link Estruturado                 |

---

## 🛠️ Lógica de Construção de Links Blindados

O Agente Atlas deve seguir este protocolo ao encontrar uma oferta:

### 1. Link Direto Amazon (Simples)
- **Regra:** Transformar qualquer URL de produto em:
- `https://www.amazon.com.br/dp/[ASIN]/?tag=karoom-20`

### 2. Link Mercado Livre (Cookie de 7 dias)
- **Regra:** Usar o buscador para validar o menor preço e gerar o link via API do Mercado Pago/Afiliados para garantir o cookie extendido.

### 3. Link Shopee (Automação API)
- **Regra:** Enviar a URL original para a Open API da Shopee e retornar o link curto `shope.ee/...` já com o tracking.

---

## 📊 Matriz de Prioridade de Recomendação
Se um produto estiver disponível em múltiplas lojas, a Karoo decidirá por:
1. **Menor Preço Final** (Produto + Frete).
2. **Melhor Prazo de Entrega** (Essencial para pais em emergência).
3. **Maior Comissão para a Karooma** (Em caso de empate nos itens acima).

---
*Gerenciado pelo Agente Atlas - Estratégia Karooma 2026*
