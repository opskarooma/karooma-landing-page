# 📍 Módulo Karooma: Geofencing & Integração Bring!

Este documento define a especificação técnica para o cruzamento de geolocalização com a lista de compras familiar.

---

## 🎯 Objetivo
Eliminar o esquecimento de itens ao passar perto de pontos de venda, automatizando a consulta à lista de compras "Bring!" baseada no GPS do usuário.

---

## 🛠️ Especificações Técnicas (Equipe Atlas)

### 1. Conector de Dados
- **Ferramenta:** `python-bring-api`.
- **Ação:** Sincronização periódica da lista "Bring!" com a memória local da Karoo.

### 2. Lógica de Cerca Digital (Geofencing)
- **Gatilho:** OpenClaw Location Field (Lat/Long).
- **Raio de Ação:** 500 metros dos POIs (Points of Interest) salvos.
- **Categorização:** O Atlas deve aprender que "Café" pertence à categoria "Supermercado" e disparar o alerta apenas em locais pertinentes.

---

## 🛡️ Auditoria de Segurança & Privacidade

O **Auditor de Diretrizes** estabelece:
1. **Isolamento de GPS:** Os dados de localização real-time NUNCA devem ser armazenados de forma permanente. Devem ser processados e descartados após o trigger.
2. **Consentimento:** O usuário deve ativar o "Modo Radar de Rua" explicitamente.
3. **Filtro de Ruído:** Não disparar mais de um alerta de proximidade para o mesmo item em um intervalo de 4 horas (evitar "spam" de localização).

---

## 📈 Roadmap de Implementação
- **Semana 1:** Testar conexão com a API não-oficial do Bring!.
- **Semana 2:** Protótipo de Geofencing com 1 ponto fixo (Ex: Mercado de costume).
- **Semana 3:** Entrega do áudio proativo: "Oi, você está no [Mercado]. Não esqueça o [Item]."

---
*Aprovado pela Equipe Karooma - Fevereiro 2026*
