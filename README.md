# Precificador de Marketplaces

Dashboard de precificação para vendedores brasileiros no Mercado Livre, na Shopee e no TikTok Shop. Você informa o custo e o preço do item e o painel calcula todos os custos da operação em cada canal e o lucro líquido por venda.

Arquivo único, sem build: abra `index.html` no navegador. Publicado em https://ursaum.github.io/ML-Strut-MCP/

## Como usar

1. Escolha o canal na aba do topo (Mercado Livre, Shopee ou TikTok Shop).
2. Preencha as entradas do item: custo, preço, impostos, Ads, afiliados, devoluções e perdas, embalagem, outros custos e a margem desejada. Elas valem para os três canais.
3. Preencha a seção do canal ativo (tipo de anúncio e logística no Mercado Livre; envio por sua conta na Shopee; Programa de Frete Grátis no TikTok Shop).

## O que cada canal calcula

| Canal | Regras usadas (referência 2026) |
|---|---|
| Mercado Livre | Comissão da categoria (Clássico 10–14%, Premium 15–19%). Abaixo de R$ 79: custo por unidade por faixa de peso × faixa de preço. A partir de R$ 79: frete grátis obrigatório pela tabela do Mercado Envios com desconto por reputação. Peso faturável = maior entre real e cubado (C × L × A ÷ 6000). Full, Flex e envio próprio. |
| Shopee | Tabela única por faixa de preço desde março de 2026: até R$ 7,99 cobra 50%; R$ 8 a 79,99 cobra 20% + R$ 4; R$ 80 a 99,99 cobra 14% + R$ 16; R$ 100 a 199,99 cobra 14% + R$ 20; R$ 200 ou mais cobra 14% + R$ 26. Programa de Frete Grátis já embutido. |
| TikTok Shop | Desde 15 de julho de 2026: até R$ 49,99 cobra 10%; R$ 50 ou mais cobra 6% + R$ 6 por item. Programa de Frete Grátis opcional com 6% sobre o preço. |
| Todos | Impostos, Ads, afiliados e devoluções/perdas em % do preço; embalagem e outros custos em valor fixo por pedido. |

Saídas: lucro líquido, margem, markup, repasse do canal, composição do preço, ponto de equilíbrio, preço sugerido para a margem desejada, comparação dentro do canal (Clássico × Premium, Programa de Frete Grátis, próxima faixa da Shopee), lucro nos três canais ao mesmo preço, simulação de −25% a +25% e o gráfico de lucro × preço com os degraus de tarifa de cada canal.

## Tabelas de tarifas

As tabelas vêm pré-preenchidas com **valores de referência de 2026**. Os valores oficiais mudam ao longo do ano e, no Mercado Livre, dependem de categoria, peso, dimensões e reputação. Abra a seção **Tabelas de tarifas** no fim do dashboard, ajuste os valores e eles ficam salvos no navegador.

## Fontes

- Mercado Livre Developers, "Custos por vender" (`/sites/MLB/listing_prices`): comissão por categoria e lógica do custo fixo por tipo de logística e limite de frete grátis.
- Central do vendedor Mercado Livre, "Custos de venda" e "Simulador de custos".
- Shopee Seller Centre, política de comissão por faixa de preço vigente desde 1º de março de 2026.
- TikTok Shop Seller Center Brasil, "Tarifa de Comissão da Plataforma", vigente desde 15 de julho de 2026.
