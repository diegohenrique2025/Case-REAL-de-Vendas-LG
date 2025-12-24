# 📱 Business Case: Análise de Vendas LG

Este repositório contém a resolução de um case técnico para a posição de **Analista de Dados**, focado na análise de performance comercial da LG. O desafio consistiu em transformar dados brutos de vendas em uma ferramenta de decisão estratégica.

## 📝 O Desafio (Situação de Negócio)
A empresa LG precisava visualizar e entender o comportamento de suas vendas nos últimos meses. O objetivo principal foi responder:
* Quais modelos de produtos possuem maior volume de vendas?
* Quais lojas e redes (Magalu, Via Varejo, etc) lideram o faturamento?
* Qual a evolução do desempenho de cada produto ao longo do tempo?
* Qual o Ticket Médio por loja e regional?

## 🛠️ Solução Técnica
* **Modelagem de Dados**: Implementação de um modelo **Star Schema** relacionando tabelas de Vendas (Fato) com Lojas e Produtos (Dimensões). 
* **Tabela Calendário**: Criação de uma `dCalendario` em DAX para permitir análises de inteligência temporal (YoY, MoM).
* **Medidas DAX Avançadas**:
    * `Faturamento Total = SUMX(fVendas, fVendas[QTD_VENDA] * RELATED(dProdutos[PRECO_UNITARIO]))`
    * `Ticket Médio = [Faturamento Total] / DISTINCTCOUNT(fVendas[ID_VENDA])`
    * `Performance vs Mês Anterior (%)`.

## 💡 Insights Gerados
1. **Curva ABC de Modelos**: Identificação dos modelos de TVs e Máquinas de Lavar que representam 80% do faturamento.
2. **Análise Regional**: Descoberta de disparidades de faturamento entre regionais (SPC vs RJ), sugerindo oportunidades de expansão.
3. **Eficiência por PDV**: Identificação de lojas com alto fluxo, mas ticket médio abaixo da média da rede.

## 📊 Visualização
*(Insira aqui os prints do seu projeto)*
![Dashboard LG](screenshots/dashboard_principal.png)

## 📁 Tecnologias Utilizadas
* **Power BI**
* **DAX**
* **Power Query (M)**
* **Excel/CSV**

---
*Este projeto foi desenvolvido como parte de um processo seletivo real, demonstrando competências técnicas e visão de negócio.*
