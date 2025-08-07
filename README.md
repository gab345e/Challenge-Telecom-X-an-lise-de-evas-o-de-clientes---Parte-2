# Challenge-Telecom-X-an-lise-de-evas-o-de-clientes---Parte-2
Propósito do Projeto
Este projeto tem como objetivo principal analisar e prever a evasão (churn) de clientes de uma operadora de telecomunicações. Usamos variáveis relacionadas ao perfil dos clientes, contratos e uso dos serviços para identificar padrões que indicam a probabilidade de cancelamento, ajudando a criar estratégias de retenção.

Estrutura do Projeto
O projeto está organizado em pastas para facilitar a navegação:

Data: contém os dados tratados em formato CSV.

Notebooks: contém o notebook principal com todo o fluxo da análise exploratória, preparação dos dados, modelagem e avaliação.

Visualizações: pasta onde ficam os gráficos gerados durante a análise.

Preparação dos Dados

As variáveis foram classificadas em:

Categóricas: como gênero, tipo de contrato, métodos de pagamento, presença de dependentes e serviços adicionais.

Numéricas: como tempo de contrato (tenure), custo mensal e total gasto.

Foram realizados tratamentos de valores faltantes com remoção ou preenchimento.

Variáveis categóricas foram transformadas em variáveis binárias via codificação (One-Hot Encoding).

Aplicamos normalização para os modelos que exigem, como Regressão Logística e KNN, usando o StandardScaler.

Os dados foram divididos em conjunto de treino e teste (exemplo: 80% treino e 20% teste).

Modelagem e Justificativas

O modelo de Regressão Logística foi escolhido por sua facilidade de interpretação e necessidade de normalização para melhorar o desempenho.

O modelo Random Forest foi usado por ser robusto, não exigir normalização e capturar relações complexas entre variáveis.

Para lidar com o desbalanceamento das classes (mais clientes ativos do que evadidos), aplicamos técnicas como SMOTE.

Análise Exploratória de Dados (EDA)

Gráficos boxplot mostraram que clientes com menor tempo de contrato e menor gasto total têm maior propensão a evadir.

Gráficos de dispersão ajudaram a identificar agrupamentos distintos entre clientes que permaneceram e os que saíram.

A matriz de correlação indicou que as variáveis numéricas têm baixa correlação linear direta com o churn, apontando que variáveis categóricas também são importantes.
