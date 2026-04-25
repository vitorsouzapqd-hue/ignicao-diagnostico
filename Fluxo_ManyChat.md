# 🤖 Fluxo ManyChat — Diagnóstico de Nutrição

Este documento detalha a estrutura da automação no ManyChat para entregar o Quiz e conduzir o lead até a oferta do Protocolo Ignição. Como o quiz roda em um link externo (HTML próprio), o fluxo usa gatilhos de tempo para fazer o follow-up.

---

## 🎯 Gatilho de Entrada (Trigger)
- **Onde:** Comentários em qualquer Post ou Reel / Mensagem Direta (DM).
- **Palavra-chave:** "IGNIÇÃO", "ignicao", "Ignição", "ignição".
- **Ação Imediata:** Curtir o comentário e responder (ex: *"Te mandei o link no Direct."* / *"Olha a DM."*).

---

## 📨 Mensagem 1: A Entrega (Imediata)
**Objetivo:** Fazer o lead clicar no link do quiz imediatamente, sem enrolação.

**Copy:**
> "Oi. O link pro diagnóstico tá aqui embaixo.
>
> São 7 perguntas rápidas. Leva menos de 3 minutos e te mostra exatamente onde a sua nutrição tá vazando energia antes e durante a prova.
>
> Vai fundo:"

**Botão:** `[ 📊 ACESSAR DIAGNÓSTICO ]`
*(Link: URL de onde o index.html está hospedado)*

**Ação no clique do botão:**
- Adicionar Tag: `Lead_Iniciou_Diagnostico`
- Iniciar Smart Delay: Esperar 45 minutos.

---

## 📨 Mensagem 2: O Diagnóstico e a Oferta (Após 45 minutos)
**Objetivo:** Pegar o lead logo após ele ter visto o resultado do quiz e apresentar o Protocolo Ignição como a solução para os "buracos" identificados.

**Condição:** Enviar apenas se a Tag `Lead_Iniciou_Diagnostico` existir.

**Copy:**
> "Conseguiu terminar o diagnóstico?
>
> Independente se o seu perfil deu 'No Chute', 'Quase Lá' ou 'Blindado', uma coisa é certa: a prova cobra a conta de tudo que você improvisou no treino. O muro do km 30 não perdoa erro de cálculo.
>
> É pra resolver exatamente isso que o Protocolo Ignição existe. Não é planilha genérica. É um método de 4 fases que a gente constrói no seu corpo e testa antes do dia D.
>
> Dá uma olhada em como funciona a Mesa de Controle:"

**Botão:** `[ 🔥 VER PROTOCOLO IGNIÇÃO ]`
*(Link: Página de Vendas ou WhatsApp de Conversão)*

**Ação:**
- Iniciar Smart Delay: Esperar 24 horas.

---

## 📨 Mensagem 3: O Fechamento (Após 24 horas)
**Objetivo:** Quebra de objeção e senso de oportunidade/urgência para quem não clicou na oferta no dia anterior.

**Copy:**
> "A maioria dos corredores treina meses para uma prova e joga todo o esforço fora nas últimas 24 horas porque errou a mão no carboidrato ou no timing do gel.
>
> Você não precisa descobrir do jeito difícil.
>
> O Protocolo Ignição te entrega previsibilidade. Você sabe o que comer, que horas comer e como o seu estômago vai reagir, porque a gente já validou isso nos treinos longos.
>
> Se você quer parar de correr na base da sorte e começar a correr com dados, a hora é agora."

**Botão:** `[ 🎯 GARANTIR MINHA VAGA ]`
*(Link: Página de Vendas ou WhatsApp de Conversão)*

---

## 🛠️ Dicas Avançadas de Configuração
1. **Janela de 24h:** O ManyChat permite enviar mensagens automáticas sem custo dentro de uma janela de 24 horas após a última interação do usuário. Este fluxo respeita essa regra perfeitamente.
2. **Fallback:** Se o Instagram bloquear o envio de links imediatos para contas novas, peça para a pessoa digitar "EU QUERO" na DM antes de soltar o link do Quiz.
3. **Tom de Voz:** Mantenha a copy seca e direta. Sem muitos emojis, mantendo a estética *Athletic Editorial* até na conversa do robô.
