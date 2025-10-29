# 📊 Desafio Zetta Lab: Análise Comparativa Socioeconômica Regional

## 🌟 1. Visão Geral e Contexto

Este projeto foi desenvolvido para atender ao desafio de "Ciência e Governança de Dados", que propõe a avaliação dos **agentes e fenômenos que mais causam impactos socioeconômicos no Brasil**. A análise busca integrar dados multidimensionais para fundamentar a compreensão das disparidades regionais e a necessidade de políticas públicas eficazes.

Para tal, o estudo se concentrou em uma **análise comparativa detalhada** entre as duas macrorregiões mais contrastantes do Brasil: **Nordeste e Sudeste**.

---

## 🎯 2. Pergunta Central

> Como poderíamos avaliar e prever/visualizar os agentes/fenômenos que mais causam impactos socioeconômicos no Brasil?

### Resposta (Etapa 1: Avaliação e Visualização):

A avaliação inicial (análise exploratória) demonstra que os fenômenos de maior impacto negativo (Insegurança Alimentar e Pobreza) se manifestam de forma desproporcional no Nordeste. O Sudeste, embora enfrente desafios de pobreza em números absolutos, mantém uma vantagem estrutural significativa em desenvolvimento humano (Educação) e menor vulnerabilidade.

---

## 🔍 3. Indicadores e Metodologia de Dados

Para traçar o panorama socioeconômico, foram coletadas e tratadas 10 bases de dados distintas, agregadas pelos seguintes indicadores:

| Indicador | Tipo de Fator | Agregação no Notebook |
| :--- | :--- | :--- |
| **Insegurança Alimentar Grave** | Bem-Estar / Crise Social | Média % por Região (Ano 2023) |
| **Pessoas na Linha da Pobreza** | Fator Econômico / Vulnerabilidade | Soma Absoluta por Região (Ano 2020) |
| **Frequência Escolar (18-24)** | Capital Humano / Educação | Média % por Região (Ano 2022) |
| **Valores de Bolsa Família** | Política Pública / Agente Mitigador | Soma Total R$ por Região (Ano 2020) |
| **Índice de Vulnerabilidade Social (IVS)** | Indicador Composto | Média do Índice por Região (Ano 2020) |

### Metodologia de Aquisição e Tratamento (Notebook):

1.  **Limpeza e Unificação:** Os dados foram importados em pares (Nordeste e Sudeste) e concatenados. Foi realizado o tratamento de strings e a conversão de colunas de ano para tipo numérico.
2.  **Agregação:** Os valores foram resumidos no nível regional (Nordeste e Sudeste). Foi utilizada a **Média** para indicadores percentuais/índices (IVS, Frequência, Insegurança) e a **Soma** para valores absolutos (Pessoas na Pobreza, Bolsa Família).
3.  **Análise de Disparidade:** Foi calculada a **Razão de Disparidade (NE/SE)**, que é a métrica central para a avaliação e visualização dos impactos regionais.

---

## 📈 4. Principais Insights da Análise Exploratória

A tabela de disparidade agregada (disponível na seção inicial do Notebook) resume o contraste estrutural entre as regiões:

| Indicador (Ano) | Razão de Disparidade (NE/SE) | Disparidade | Interpretação |
| :--- | :--- | :--- | :--- |
| **Insegurança Alimentar (2023)** | **2.18** | **+117.82%** | O Nordeste tem mais do que o **dobro** de domicílios em situação grave. |
| **Bolsa Família (2020)** | **2.04** | **+103.87%** | O investimento é mais que o dobro no Nordeste, evidenciando a dependência do programa. |
| **Pessoas na Pobreza (2020)** | 1.39 | +38.54% | Maior concentração absoluta de pobreza no Nordeste. |
| **IVS (2020)** | 1.29 | +28.54% | O Nordeste é estruturalmente mais vulnerável socialmente. |
| **Freq. Escolar Ens. Sup. (2022)** | 0.74 | **-26.34%** | O acesso à educação superior é significativamente menor no Nordeste (maior no Sudeste). |

### Conclusões Essenciais:

* **Agentes de Impacto Negativo:** A **Insegurança Alimentar** (Razão 2.18) e a **Pobreza** (Razão 1.39) são os fenômenos que mais marcam a desigualdade regional, exigindo foco imediato de políticas públicas.
* **Contraste Estrutural:** A análise visual (gráficos IVS e Pobreza) mostra que, embora ambas as regiões tenham sofrido o impacto da crise em 2020/2021, o Nordeste começa e se mantém em um patamar de vulnerabilidade ($28.5\%$ maior) e investimento social ($103.8\%$ maior) que reflete a necessidade de estratégias específicas e sustentáveis.
