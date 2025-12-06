# 🏠 Previsão de Preços de Casas --- *Projeto de Machine Learning*

Bem-vindo ao meu projeto **PrecoCasas**, onde desenvolvi um modelo de **[Regressão Linear](https://developers.google.com/machine-learning/crash-course/linear-regression?hl=pt-br)** para prever preços de imóveis com base em diversos atributos. 

Este projeto foi criado com foco em **aprendizagem prática**, explorando desde o pré-processamento dos dados até a construção e avaliação do modelo final.

## 📌 Objetivo do Projeto

O objetivo é **prever o preço de casas** utilizando um modelo de Machine Learning supervisionado.

# 🧹 1. Limpeza e Preparação dos Dados
Antes de treinar qualquer modelo, eu precisei garantir que os dados estivessem **consistentes**, **completos** e **prontos para serem utilizados**.  
As principais etapas foram:

### ✔️ Exclusão de valores ausentes (NaN)

### ✔️ Remoção de colunas com dados categóricos

A qualidade dos dados é essencial para a qualidade das previsões — por isso, essa etapa foi fundamental.

# 🛠️ 2. Engenharia de Atributos

A engenharia de atributos foi essencial para transformar dados brutos em informações úteis para o modelo.

### 🔢 [Ordinal Encoder](https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.OrdinalEncoder.html) (Scikit-Learn)
Converti variáveis categóricas em valores numéricos ordenados usando o `OrdinalEncoder`, permitindo que o modelo interpretasse padrões presentes nas categorias.

### 🧩 Função `.map()` do [Pandas](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.map.html)

Utilizei também `.map()` para transformar categorias específicas em valores numéricos personalizados, permitindo uma modelagem mais direcionada em variáveis importantes do dataset.

# 📏 3. Padronização dos Dados

### 🧮 [StandardScaler (Scikit-Learn)](https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.StandardScaler.html)

Apliquei **padronização** com `StandardScaler` para deixar os dados numéricos em uma mesma escala (média 0, desvio 1).

### ✔️ Por que padronizei?

-   Evita que atributos grandes dominem o modelo
-   Melhora o desempenho da Regressão Linear
-   Acelera e estabiliza o processo de treinamento
    

Essa etapa foi fundamental para obter boas métricas de erro.

# 🤖 4. Modelo Utilizado --- Regressão Linear

O modelo escolhido foi a **[Regressão Linear](https://developers.google.com/machine-learning/crash-course/linear-regression?hl=pt-br)**, uma técnica simples e eficiente para compreender relações entre variáveis numéricas.

### ✔️ Por que escolhi este modelo?

Eu realizei testes com **diferentes algoritmos**, comparando seus resultados por meio das métricas **RMSE** e **MAE**.  

A partir dessa comparação, a **Regressão Linear apresentou o melhor desempenho**, sendo a escolha ideal para este projeto.

### 🧠 Como funciona?

A Regressão Linear ajusta uma linha (ou hiperplano) que melhor representa a relação entre os atributos e o preço da casa, calculando coeficientes que indicam a influência de cada variável na previsão.

# 📊 5. Avaliação do Modelo

Avaliei a performance do modelo utilizando:

### 📉 **[MSE (Mean Squared Error)](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.mean_squared_error.html)**

Mede o erro quadrático médio, dando mais peso a erros maiores.

### 📈 **[MAE (Mean Absolute Error)](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.mean_absolute_error.html)**

Mede o erro absoluto médio, indicando o quão distante a previsão fica do valor real.

### 📌 **Gráfico de dispersão (Matplotlib)**

Criei um gráfico comparando os valores reais e previstos, permitindo visualizar o alinhamento e detectar discrepâncias no comportamento do modelo.

### ⭐ **Resultado Geral (Kaggle)**

A acurácia atingiu **82,5%**, de acordo com a avaliação automática da plataforma [Kaggle](https://www.kaggle.com/).

# 📂 6. Estrutura do Projeto



    📦 PrecoCasas
    ├── PrecoCasas.ipynb			# Jupyter Notebook com todo o fluxo do projeto
    ├── README.md			 		# Arquivo de documentação
    └── dataset/					# Dataset utilizado no projeto

# 🚀 7. Tecnologias Utilizadas

-   [Python](https://docs.python.org/pt-br/3/)
-   [Pandas](https://pandas.pydata.org/docs/)
-   [NumPy](https://numpy.org/doc/)
-   [Scikit-Learn](https://scikit-learn.org/stable/)
-   [Matplotlib](https://matplotlib.org/stable/index.html)
-   [Jupyter Notebook](https://docs.jupyter.org/en/latest/)

# 📝 8. Conclusão

Esse projeto foi uma excelente oportunidade para aplicar conceitos essenciais de Machine Learning, tais como:

-   Limpeza de dados
-   Engenharia de atributos
-   Padronização
-   Teste e comparação de modelos
-   Análise gráfica das previsões

Com essa base, consegui alcançar **82,5% de acurácia** no Kaggle e construir um pipeline de previsão funcional e bem estruturado.
