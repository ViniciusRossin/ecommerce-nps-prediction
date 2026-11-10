# Tech Challenge Fase 1 — NPS Preditivo

Projeto desenvolvido para o Tech Challenge da Fase 1 da pós-graduação em IA Scientist.

## Objetivo do projeto

Um e-commerce em crescimento acelerado enfrenta alta variabilidade de NPS entre clientes com perfis
operacionais semelhantes. Hoje o NPS só é coletado após o encerramento da jornada de compra, o que
limita a capacidade da empresa de antecipar problemas e agir preventivamente.

Este projeto investiga **quais fatores operacionais (pedido, logística, atendimento) influenciam a
satisfação do cliente**, traduzindo dados operacionais em insights acionáveis para as áreas de
negócio (logística, atendimento, produto e estratégia), e avalia a viabilidade de um modelo preditivo
capaz de estimar a satisfação do cliente antes da aplicação da pesquisa de NPS.

## Descrição da base de dados

Arquivo: `data/desafio_nps_fase_1.csv` — 2.500 pedidos, 19 colunas, sem valores nulos.

| Coluna | Descrição |
|---|---|
| `customer_id` | Identificador único do cliente |
| `order_id` | Identificador único do pedido |
| `customer_age` | Idade do cliente |
| `customer_region` | Região geográfica do cliente |
| `customer_tenure_months` | Tempo de relacionamento do cliente com a empresa (meses) |
| `order_value` | Valor total do pedido |
| `items_quantity` | Quantidade de itens no pedido |
| `discount_value` | Valor de desconto aplicado |
| `payment_installments` | Número de parcelas do pagamento |
| `delivery_time_days` | Tempo total de entrega (dias) |
| `delivery_delay_days` | Dias de atraso na entrega |
| `freight_value` | Valor do frete |
| `delivery_attempts` | Número de tentativas de entrega |
| `customer_service_contacts` | Número de contatos com o atendimento |
| `resolution_time_days` | Tempo para resolução de problemas (dias) |
| `complaints_count` | Número de reclamações registradas |
| `repeat_purchase_30d` | Recompra em até 30 dias (0/1) |
| `csat_internal_score` | Score interno de satisfação |
| `nps_score` | **Target** — Nota de satisfação (NPS), 0 a 10 |

## Estrutura do repositório

```
.
├── data/        # base de dados bruta
├── notebooks/   # tratamento de dados, EDA e modelo preditivo
├── models/      # artefatos de modelo treinado (se aplicável)
├── reports/     # respostas conceituais e relatórios de apoio
└── README.md
```

## Metodologia

O projeto segue as etapas propostas pelo desafio, nesta ordem:

| # | Etapa | Status | Onde está |
|---|---|---|---|
| 1 | Entendimento do negócio | ✅ Concluído | [`reports/01_entendimento_negocio.md`](reports/01_entendimento_negocio.md) |
| 2 | Definição da target | ✅ Concluído | [`reports/02_definicao_target.md`](reports/02_definicao_target.md) |
| 3 | Análise Exploratória dos Dados (EDA) | ✅ Concluído | [`reports/03_eda.md`](reports/03_eda.md) (resumo de negócio) + [`notebooks/01_eda.ipynb`](notebooks/01_eda.ipynb) (código) |
| 4 | Modelo preditivo (opcional) | ⏳ A definir | `notebooks/` + `models/` |

## Como reproduzir os resultados

1. Clone o repositório: `git clone https://github.com/ViniciusRossin/ecommerce-nps-prediction.git`
2. Crie um ambiente virtual e instale as dependências: `pip install -r requirements.txt`
3. Execute os notebooks em `notebooks/` na ordem numérica indicada pelo nome do arquivo
   (`jupyter notebook notebooks/01_eda.ipynb`). Os gráficos são salvos em `reports/figures/`.

## Relatórios

- [`reports/01_entendimento_negocio.md`](reports/01_entendimento_negocio.md) — entendimento do
  problema de negócio (5 perguntas numeradas: problema, importância do NPS, áreas beneficiadas,
  impacto em recompra/boca a boca/market share, indicadores de mercado complementares).
- [`reports/02_definicao_target.md`](reports/02_definicao_target.md) — definição conceitual da
  variável target (4 perguntas numeradas: variável escolhida, justificativa, momento de coleta,
  riscos de uso inadequado).
- [`reports/03_eda.md`](reports/03_eda.md) — análise exploratória em linguagem de negócio (4 perguntas
  numeradas: fatores críticos, o que gera detratores, pontos de ruptura, perfil de cliente).
