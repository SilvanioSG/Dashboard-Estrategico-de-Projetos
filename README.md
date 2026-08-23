# Dashboard EVM Executivo — Obra Alpha

Dashboard executivo para análise integrada de desempenho de projetos, desenvolvido com foco em **Earned Value Management (EVM)**, eficiência operacional, produtividade, gestão de riscos e acompanhamento de performance.

O projeto apresenta uma simulação de empreendimento denominada **Obra Alpha**, estruturada para demonstrar a aplicação prática de indicadores de Valor Agregado na análise de escopo, prazo e custos.

**Autor:** Silvanio Gois — Gestor de Operações e Negócios Orientado a Dados

---

## Visão Geral

O Dashboard EVM Executivo — Obra Alpha consolida indicadores de desempenho de projeto em uma interface única, permitindo analisar a evolução física e financeira, eficiência de custos, desempenho de prazo, produtividade, eficiência operacional e riscos.

A metodologia utilizada é o **EVM — Earned Value Management**, aplicada à simulação de um empreendimento com duração de 12 meses e diferentes cenários de desempenho.

O dashboard permite alternar entre cenários e períodos de análise, possibilitando uma leitura comparativa da performance do projeto.

A aplicação apresenta monitoramento do Valor Agregado integrado a indicadores de eficiência operacional e gestão de riscos.

---

## Objetivo

Demonstrar, de forma prática e visual, como indicadores de **Valor Agregado (EVM)** podem ser utilizados em conjunto com indicadores operacionais e de riscos para acompanhar o desempenho de um projeto.

A solução foi estruturada para analisar:

* desempenho de custos;
* desempenho de prazo;
* valor planejado;
* custo real;
* valor agregado;
* produtividade;
* eficiência operacional;
* riscos;
* previsão de custo final;
* variação no término;
* desempenho necessário para conclusão.

---

## Metodologia

O dashboard utiliza **Earned Value Management (EVM)** para integrar escopo, prazo e custos e medir a performance do projeto.

Os principais indicadores implementados são:

| Indicador | Descrição                         | Fórmula                    |
| --------- | --------------------------------- | -------------------------- |
| **PV**    | Planned Value — Valor Planejado   | Percentual planejado × BAC |
| **EV**    | Earned Value — Valor Agregado     | Percentual realizado × BAC |
| **AC**    | Actual Cost — Custo Real          | Custo real do período      |
| **CPI**   | Cost Performance Index            | EV / AC                    |
| **SPI**   | Schedule Performance Index        | EV / PV                    |
| **CV**    | Cost Variance — Variação de Custo | EV − AC                    |
| **EAC**   | Estimate at Completion            | AC + (BAC − EV) / CPI      |
| **ETC**   | Estimate to Complete              | EAC − AC                   |
| **VAC**   | Variance at Completion            | BAC − EAC                  |
| **TCPI**  | To Complete Performance Index     | (BAC − EV) / (BAC − AC)    |

As fórmulas são implementadas diretamente no processamento dos dados do dashboard.

---

## Indicadores do Dashboard

### Indicadores EVM

O painel apresenta, entre outros, os seguintes indicadores consolidados:

* CPI — Eficiência de Custo;
* SPI — Desempenho de Prazo;
* EV — Valor Agregado;
* AC — Custo Real;
* CV — Variação de Custo;
* TCPI — Índice de Desempenho para Conclusão.

Os indicadores são recalculados de acordo com o cenário e o período selecionados.

### Indicadores Operacionais

A análise operacional contempla:

* produtividade planejada;
* produtividade realizada;
* OEE médio;
* eficiência produtiva.

A produtividade é comparada entre o planejado e o realizado, enquanto o OEE é calculado a partir da média dos valores do período selecionado.

### Gestão de Riscos

O dashboard utiliza uma matriz de **Probabilidade × Impacto**, com classificação dos níveis de risco:

* Alto: ≥ 12;
* Médio: 6–11;
* Baixo: ≤ 5.

O valor do risco é calculado pela multiplicação da probabilidade pelo impacto.

---

## Visualizações

O dashboard reúne diferentes perspectivas de análise do projeto.

### Curva S

Apresenta a evolução do avanço físico e financeiro ao longo dos meses.

### Tendência Financeira

Apresenta a evolução de:

* PV;
* AC;
* EV.

### Previsão Final

Apresenta a previsão de custo final por meio do **EAC — Estimate at Completion**.

### Produtividade

Apresenta a produção em unidades por mês, permitindo comparar desempenho planejado e realizado.

### OEE

Apresenta o indicador de eficiência dos equipamentos.

### Mapa de Riscos

Apresenta visualmente a distribuição dos riscos segundo Probabilidade × Impacto.

Essas visualizações fazem parte da estrutura principal do dashboard.

---

## Análise Temporal

O dashboard permite selecionar diferentes períodos de análise:

* Visão Completa — Ano;
* Acumulado — YTD;
* 1º Trimestre — Q1;
* 2º Trimestre — Q2;
* 3º Trimestre — Q3;
* 4º Trimestre — Q4.

## O período selecionado altera o conjunto de dados utilizado nos cálculos, tabelas, gráficos, indicadores operacionais e resumo executivo.

## Cenários de Análise

O dashboard disponibiliza três cenários:

1. **Estudo Realista — Padrão**
2. **Cenário Crítico**
3. **Cenário Otimizado**

A seleção do cenário altera o conjunto de dados utilizado para os cálculos e visualizações.

### Cenário Realista

**BAC:** R$ 1.500.000
**Duração:** 12 meses

O cenário considera atrasos no primeiro trimestre relacionados ao licenciamento, problemas de disponibilidade de materiais durante o segundo e terceiro trimestres e uma aceleração no quarto trimestre para recuperação do cronograma.

Resultado final apresentado no projeto:

* CPI: 0,80;
* SPI: 0,98;
* Estouro: 25%;
* OEE médio: 81%.

Os dados utilizados incluem avanço planejado e realizado, custos reais, riscos, produtividade planejada e realizada e OEE mensal.

### Cenário Crítico

**BAC:** R$ 1.800.000
**Duração:** 12 meses

O cenário representa uma condição de forte deterioração de desempenho, incluindo paralisação por problemas trabalhistas, riscos elevados, baixa produtividade e baixo desempenho dos equipamentos.

Resultado final apresentado no projeto:

* CPI: 0,47;
* SPI: 0,67;
* Estouro: 111%;
* OEE médio: 56%.

Os dados do cenário apresentam risco 4 × 4 ao longo dos meses, avanço físico significativamente inferior ao planejado, custos elevados e produtividade reduzida.

### Cenário Otimizado

**BAC:** R$ 1.400.000
**Duração:** 12 meses

O cenário representa uma condição de desempenho superior, com equipes especializadas, processos otimizados, produtividade acima do planejado e gestão proativa de riscos.

Resultado final apresentado no projeto:

* CPI: 1,12;
* SPI: 1,00;
* Economia: 11%;
* OEE médio: 94%.

## Os dados utilizados apresentam avanço físico superior ao planejado em diversos períodos, custos abaixo do orçamento, risco 1 × 1 e níveis elevados de produtividade e OEE.

## Pacotes de Serviço

O dashboard apresenta os pacotes de serviço associados ao cenário selecionado, incluindo:

* serviço;
* responsável;
* quantidade;
* valor unitário;
* status;
* total estimado.

No cenário realista, por exemplo, estão definidos os serviços de Escavação e Fundações, Estrutura de Concreto, Instalações Hidráulicas, Acabamentos e Paisagismo e Entrega.

---

## Cronograma Macro

O projeto possui uma representação do cronograma macro em formato semelhante a um Gantt.

Para cada mês são apresentados:

* fase;
* percentual planejado;
* percentual realizado.

As fases utilizadas pelo processamento são:

* Fundação;
* Estrutura;
* Acabamento;
* Entrega.

---

## Detalhamento Mensal

O dashboard apresenta uma tabela mensal com:

* mês;
* físico realizado;
* PV;
* AC;
* EV;
* CPI;
* SPI;
* CV;
* risco.

Essa estrutura permite analisar a evolução dos indicadores ao longo do projeto e identificar períodos com maior ou menor desempenho.

---

## Resumo Executivo

O painel gera dinamicamente um resumo executivo considerando o período selecionado.

O resumo apresenta:

* avanço físico acumulado;
* CPI acumulado;
* EAC;
* VAC;
* ETC;
* TCPI.

Também são geradas recomendações de acordo com o desempenho de custos observado no período.

---

## Validação dos Dados

De acordo com a documentação incorporada ao próprio dashboard, as relações utilizadas na simulação foram estruturadas e validadas considerando:

* progresso físico × custo;
* OEE × produtividade;
* riscos × performance;
* filtros × cálculos acumulados;
* narrativas × dados utilizados.

O projeto é apresentado como um dashboard técnico com dados realistas e relações matemáticas validadas para aplicação de EVM.

---

## Tecnologias Utilizadas

A implementação apresentada no arquivo utiliza:

* HTML5;
* CSS3;
* JavaScript;
* Chart.js 4.4.0;
* Chart.js DataLabels 2.2.0;
* fonte Inter.

## O projeto é estruturado como uma aplicação web client-side, com os dados dos cenários definidos no próprio JavaScript e os indicadores calculados dinamicamente no navegador.

## Estrutura Conceitual

O fluxo de processamento do dashboard pode ser representado da seguinte forma:

```text
Dados do Cenário
       |
       v
Avanço Planejado + Avanço Realizado + Custos
       |
       v
PV / EV / AC
       |
       v
CPI / SPI / CV
       |
       v
EAC / ETC / VAC / TCPI
       |
       +------------------+
       |                  |
       v                  v
Produtividade          OEE
       |                  |
       +--------+---------+
                |
                v
        Análise de Performance
                |
                v
        Gestão de Riscos
                |
                v
          Resumo Executivo
                |
                v
        Plano de Ação
```

---

## Acesso ao Projeto

**Dashboard EVM Executivo — Obra Alpha**

https://silvaniosg.github.io/Dashboard-Estrategico-de-Projetos/

---

## Autor

### Silvanio Gois

**Gestor de Operações e Negócios Orientado a Dados**

Site profissional:

https://www.silvaniogois.com.br/

LinkedIn:

https://www.linkedin.com/in/silvanio-gois

GitHub:

https://github.com/SilvanioSG

---

## Sobre o Projeto

Este projeto integra o portfólio de soluções desenvolvidas por **Silvanio Gois**, demonstrando a aplicação de conceitos de gestão de projetos, EVM, indicadores operacionais, análise de riscos e visualização de dados em um dashboard executivo.

O projeto foi desenvolvido com dados simulados para demonstrar a aplicação da metodologia e o comportamento dos indicadores em diferentes condições de desempenho.

**Dashboard técnico com dados realistas e relações validadas — EVM aplicado.**

---

## Direitos

© 2025 Silvanio Gois — Dashboard Executivo EVM.

Todos os direitos reservados.
