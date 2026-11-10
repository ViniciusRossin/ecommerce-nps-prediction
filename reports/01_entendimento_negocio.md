# 1. Entendimento do Negócio

## 1.1 Qual problema de negócio está sendo resolvido?

**Resposta:** A empresa cresceu rapidamente no e-commerce e passou a lidar com um volume cada vez
maior de pedidos, entregas e interações com clientes. Esse crescimento trouxe ganhos de escala, mas
também revelou um problema: o **NPS apresenta alta variabilidade** entre clientes com perfis
operacionais semelhantes — alguns se tornam promotores da marca, outros se tornam detratores, sem uma
causa evidente à primeira vista.

Hoje o NPS só é coletado **depois** do encerramento da jornada de compra, o que limita a capacidade
da empresa de antecipar problemas, priorizar ações corretivas e agir de forma preventiva. O problema
de negócio, portanto, é: **quais fatores operacionais realmente influenciam a satisfação do cliente,
e como a empresa pode agir proativamente para melhorar a experiência antes mesmo da aplicação da
pesquisa de NPS?**

## 1.2 Por que o NPS é importante para um e-commerce?

**Resposta:** O NPS funciona como um proxy direto de lealdade e propensão à recomendação. Em um setor
com custo de aquisição de cliente (CAC) elevado e concorrência intensa em preço e prazo, reter
clientes e estimular a recompra é mais barato do que adquirir novos. O NPS também atua como um
**termômetro antecipado de churn**: clientes insatisfeitos tendem a reduzir ou parar de comprar antes
mesmo de registrarem uma reclamação formal.

## 1.3 Quais áreas poderiam se beneficiar desses insights?

**Resposta:**
- **Logística**: priorizar rotas/transportadoras com mais atraso, revisar SLA de entrega.
- **Atendimento**: identificar gatilhos que geram múltiplos contatos e reduzir tempo de resolução.
- **Produto**: entender se categorias ou características específicas do pedido geram mais reclamação.
- **Pricing / Comercial**: avaliar se desconto ou parcelamento têm relação com a satisfação (ex.:
  expectativa de valor vs. experiência entregue).
- **Estratégia / CX**: priorizar investimento onde o retorno em satisfação é maior.

## 1.4 Reflexão: como o NPS impacta recompra, boca a boca e market share?

**Resposta:**

- **Recompra** — Clientes promotores tendem a comprar novamente e com mais frequência; detratores
  tendem a abandonar a base ou migrar para a concorrência. Essa relação é observável nos dados como
  correlação entre `nps_score` e `repeat_purchase_30d`.
- **Boca a boca** — Promotores geram recomendação orgânica, reduzindo o custo de aquisição de novos
  clientes. Detratores geram boca a boca negativo, avaliações ruins e reclamações públicas — custo
  especialmente alto em e-commerce, onde a reputação online influencia diretamente a decisão de
  compra de terceiros.
- **Market share** — Em mercados competitivos e comoditizados, a experiência de compra é um dos
  poucos diferenciais reais entre concorrentes. Um NPS baixo sustentado tende a erodir participação
  de mercado mesmo quando o preço é competitivo.

## 1.5 Quais indicadores de mercado poderiam complementar essa análise?

**Resposta:**
- Benchmark setorial de NPS (e-commerce brasileiro, por categoria de produto).
- SLA logístico médio do setor (tempo de entrega e taxa de atraso dos concorrentes).
- Índices de satisfação divulgados publicamente por concorrentes diretos.
- Dados de CAC/LTV do setor, para quantificar o custo real de um cliente detrator.
