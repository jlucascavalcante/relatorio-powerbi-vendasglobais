# 🌍 Dashboard Analítico de Vendas Globais — Power BI

Dashboard de análise de pedidos globais com foco em desempenho por categoria, subcategoria, país e prioridade de pedido — permitindo identificar padrões de desconto, concentração geográfica e distribuição de volume entre segmentos de clientes.

---

## 🎯 Problema de negócio

Em operações de vendas globais, é comum que gestores tomem decisões de precificação e desconto com base em percepções gerais sobre quais categorias ou mercados performam melhor. Este dashboard centraliza os dados de pedidos entre 2011 e 2014 para responder perguntas objetivas: onde estão concentrados os pedidos? Quais subcategorias acumulam os maiores descontos médios? A prioridade do pedido varia de forma relevante entre países?

---

## 🔍 Principais insights

- **Volume total de 12,64 mil pedidos** distribuídos entre múltiplos países, segmentos e categorias ao longo de 4 anos.
- **Suprimentos dominam o volume**, representando ~61% do total de pedidos por categoria — mais que o dobro de Tecnologia e Móveis combinados.
- **Tables é a subcategoria com maior desconto médio**, seguida por Binders e Machines — o que levanta a questão se esses descontos estão sendo aplicados de forma estratégica ou apenas para escoar volume.
- **Estados Unidos concentram o maior volume de pedidos** entre todos os países analisados, com destaque para pedidos de prioridade Média e Alta — sugerindo um mercado maduro com demanda consistente.
- **Distribuição geográfica ampla**, com presença em todos os continentes, mas com forte assimetria: poucos países respondem pela maior parte do volume.
- Os segmentos **Consumidor, Corporativo e Home Office** permitem filtrar o comportamento de cada perfil de cliente — útil para times comerciais e de planejamento.

---

## 📄 Estrutura do dashboard

O relatório é composto por uma única página analítica com os seguintes visuais:

| Visual | Descrição |
|---|---|
| **KPI — Total de Vendas Globais** | Cartão com o total geral de pedidos (12,64 mil) |
| **Média de Desconto por Subcategoria** | Gráfico de barras horizontais ordenado por desconto médio |
| **Total de Vendas por Categoria** | Gráfico de rosca com participação percentual de cada categoria |
| **Média de Vendas por País** | Mapa geográfico com bolhas proporcionais ao volume médio por país |
| **Total de Vendas por País e Prioridade** | Gráfico de barras empilhadas segmentado por prioridade (Alto, Médio, Baixo, Crítico) |

**Filtros disponíveis:** Ano (slider 2011–2014), Segmento (Consumidor, Corporativo, Home Office) e País.

---

## 🛠️ Stack técnica

- **Ferramenta:** Power BI Desktop
- **Transformação de dados (Power Query):** limpeza e padronização da base, tratamento de tipos de dado, renomeação de colunas e remoção de campos não utilizados
- **Visualizações:** mapa geográfico (Bing Maps), gráfico de rosca, barras horizontais, barras empilhadas e cartão KPI
- **Sem medidas DAX** — todas as agregações utilizam as funções nativas do Power BI

---

## 📊 Fonte dos dados

Dataset de pedidos de varejo global com cobertura de 2011 a 2014, originalmente utilizado em curso de formação em dados. O dashboard, os visuais, a formatação e a estrutura analítica foram desenvolvidos de forma independente — incluindo a escolha dos gráficos, paleta, layout e cruzamentos exibidos.

---

## 🔗 Acesse o relatório

[Acesse o dashboard](https://app.powerbi.com/view?r=eyJrIjoiYmVlMTg0MmMtYWI4MS00OGRkLWIxYmYtNjJhZmM2MzY3ZTc3IiwidCI6ImIyZTE2Mjk3LTJlZDYtNDFiOC1iODIyLWE5NTRlOTViZDJmMCIsImMiOjR9)

---

## 📌 Limitações e próximos passos

- Os valores exibidos são **contagens de pedidos**, não receita financeira — comparações entre países e categorias refletem volume, não valor monetário.
- A análise atual não cruza **desconto médio com volume de pedidos** por subcategoria — próximo passo natural seria identificar se as subcategorias com maior desconto são também as de maior ou menor volume, para avaliar se o desconto está gerando ou apenas acompanhando demanda.
- Uma próxima iteração poderia incluir **métricas de crescimento ano a ano** por país e categoria, aproveitando o slider de ano já disponível como filtro.
