# 📊 Análise Operacional e Estatística Descritiva

Este repositório contém a resolução de um projeto prático de Análise Exploratória de Dados (EDA) e Estatística Descritiva, desenvolvido em Python. O objetivo principal do projeto foi transformar dados "sujos" e brutos em insights operacionais através de limpeza rigorosa, transformação e visualização.

## 🎯 Escopo do Projeto

O projeto é dividido em dois desafios analíticos distintos:

### Atividade 1: Operação Aeroportuária (`dados_aeroporto.csv`)
Foco em engenharia e limpeza de dados (Data Wrangling) para entender padrões de atraso e o perfil operacional de um aeroporto.
* **Limpeza e Padronização:** 
  * Nivelamento de caixa (maiúsculas/minúsculas).
  * Remoção de espaços em branco invisíveis (`strip`).
  * Normalização Unicode (`NFKD`) para remoção robusta de acentos.
  * Identificação e remoção de registros duplicados verdadeiros e tratamento de valores nulos.
* **Enriquecimento de Dados:** 
  * Extração de horas de dados textuais (`pd.to_datetime`) e categorização em faixas de horário (Manhã, Tarde, Noite) usando `pd.cut()`.
  * Criação de colunas binárias vetorizadas com `numpy.where` e `.isin()` para identificar o status de embarque.
* **Visualização e Insights:**
  * Cruzamento de dados (`pd.crosstab`) para identificar a companhia com maior taxa de atrasos e os horários mais críticos da operação através de gráficos de barras empilhadas.

### Atividade 2: Métricas de Atendimento (`clientes_venda.csv`)
Foco em Estatística Descritiva pura para avaliar a eficiência do tempo de resposta a clientes.
* **Tratamento Matemático:** Substituição de separadores decimais (vírgula por ponto) e coerção de tipos para garantir o rigor dos cálculos em formato numérico.
* **Métricas Extraídas:** Média, Mediana, Moda (identificação de conjuntos amodais), Variância e Desvio Padrão.
* **Análise de Dispersão e Outliers:** Cálculo manual do Intervalo Interquartil (IQR) para provar a consistência do atendimento.
* **Visualização:** Construção de Histogramas e Boxplots usando `matplotlib` para confirmar visualmente a simetria da distribuição e a ausência de valores atípicos (outliers).

## 🛠️ Tecnologias Utilizadas

* **Python 3**
* **Pandas:** Estruturação, limpeza, cruzamento e cálculos estatísticos.
* **Matplotlib:** Plotagem de gráficos e representação visual de distribuições.
* **Google Colab:** Ambiente de desenvolvimento interativo.
