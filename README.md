# Precificador Mercado Livre

Dashboard de precificação para vendedores do Mercado Livre (Brasil). Você informa o custo e o preço do item e o painel calcula todos os custos da operação e o lucro líquido por venda.

Arquivo único, sem build: abra `index.html` no navegador.

## O que ele calcula

| Custo | Regra usada |
|---|---|
| Comissão | % da categoria × preço (Clássico 10–14%, Premium 15–19%) |
| Custo por unidade | Anúncios abaixo de R$ 79: tabela por faixa de peso × faixa de preço (regra em vigor desde março de 2026) |
| Frete grátis | Anúncios a partir de R$ 79: tabela do Mercado Envios por peso faturável, com desconto por reputação |
| Peso faturável | Maior valor entre peso real e peso cubado (C × L × A ÷ 6000) |
| Full, Flex e envio próprio | Custo operacional do Full por unidade ou custo real da sua entrega |
| Impostos | % sobre o preço (Simples Nacional ou carga efetiva) |
| Ads, afiliados, devoluções e perdas | % sobre o preço |
| Embalagem, outros | valor fixo por pedido |

Saídas: lucro líquido, margem, markup, repasse do Mercado Livre, composição do preço, ponto de equilíbrio, preço sugerido para a margem desejada, comparação Clássico × Premium, simulação de −25% a +25% e o gráfico de lucro × preço com o degrau dos R$ 79.

## Tabelas de tarifas

As tabelas de custo por unidade e de frete vêm pré-preenchidas com **valores de referência de 2026**. Os valores oficiais variam por categoria, peso, dimensões e reputação e estão no Simulador de custos do painel do vendedor. Abra a seção **Tabelas de tarifas** no fim do dashboard, ajuste os valores e eles ficam salvos no navegador.

## Fontes

- Mercado Livre Developers, "Custos por vender" (`/sites/MLB/listing_prices`): comissão por categoria e lógica do custo fixo por tipo de logística e limite de frete grátis.
- Central do vendedor, "Custos de venda" e "Simulador de custos".
