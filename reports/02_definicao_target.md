# 2. Definição da Target

## 2.1 Qual variável representa a satisfação do cliente?

**Resposta:** `nps_score` — nota de 0 a 10 coletada após a experiência de compra.

## 2.2 Por que ela foi escolhida?

**Resposta:** É a única variável na base que mede **satisfação declarada pelo próprio cliente**, de
forma padronizada (mesma escala para todos), e já é a métrica-padrão de mercado para lealdade e
propensão a recomendar — o que facilita benchmarking externo e comunicação com o negócio.

## 2.3 Em que momento da jornada essa informação é coletada?

**Resposta:** Depois do encerramento da jornada de compra — ou seja, pós-entrega, quando o cliente já
vivenciou todo o ciclo (pedido, pagamento, logística e eventual atendimento/reclamação).

## 2.4 Existe algum risco de usar essa variável de forma inadequada?

**Resposta:** Sim, alguns riscos relevantes:

- **Viés de resposta**: só responde quem quis responder — clientes muito insatisfeitos podem
  simplesmente não responder (silêncio) em vez de dar nota baixa, distorcendo a amostra.
- **Defasagem temporal / vazamento de dados**: é coletada só no fim da jornada, então qualquer modelo
  que a use como target está, por definição, tentando *antecipar* algo que só existe depois do fato.
  É preciso garantir que as variáveis preditoras (entrega, atendimento) estejam disponíveis *antes*
  do NPS ser gerado, senão o modelo teria vazamento de dados (data leakage).
- **Confundir correlação com causalidade**: uma nota baixa pode refletir um fator pontual (ex.: um
  atraso isolado) e não necessariamente a experiência completa — usar isoladamente para punir ou
  premiar áreas pode gerar decisões injustas.
- **Perda de nuance ao categorizar**: se for convertida em "satisfeito/insatisfeito" para
  classificação, o ponto de corte escolhido (ex.: NPS ≥ 7) precisa ser justificado, senão perde
  granularidade de informação.
