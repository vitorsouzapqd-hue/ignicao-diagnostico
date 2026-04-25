# 🎯 Estratégia da Isca Digital: Diagnóstico de Nutrição

Este documento detalha a lógica de conversão e os perfis de saída do quiz.

## 🗺️ Fluxo de Conversão
1. **Ativação:** Reel/Carrossel com CTA "Comenta IGNIÇÃO".
2. **Entrega:** Automação (ManyChat) envia o link do `Index.html`.
3. **Qualificação:** O lead responde 7 perguntas situacionais (anti-gaming).
4. **Diagnóstico:** Recebe um dos 3 perfis técnicos.
5. **Conversão:** CTA no final do quiz direciona para o WhatsApp ou Checkout do Protocolo Ignição.

---

## 📊 Perfis de Resultado

### 🔴 Perfil "No Chute" (0 a 4 pontos)
Corredor que improvisa. Foco na **URGÊNCIA**. 
- *Dor:* O muro do km 25.
- *Solução:* Método do zero.

### 🟡 Perfil "Quase Lá" (5 a 9 pontos)
Corredor com noção, mas com pontos cegos. Foco na **PRECISÃO**.
- *Dor:* Queda de pace no final sem explicação física aparente.
- *Solução:* Fechamento de buracos técnicos com dados.

### 🟢 Perfil "Blindado" (10 a 14 pontos)
Corredor consciente. Foco na **SOFISTICAÇÃO/AJUSTE FINO**.
- *Dor:* O detalhe que ele "não sabe que não sabe".
- *Solução:* Otimização marginal para recorde pessoal (RP).

---

## ⚙️ Notas de Implementação
- **Hospedagem:** O arquivo `Index.html` pode ser colocado no GitHub Pages, Vercel ou qualquer servidor estático.
- **ManyChat:** Configure o campo personalizado `perfil_nutricao` se possível para segmentar o e-mail marketing posterior.
