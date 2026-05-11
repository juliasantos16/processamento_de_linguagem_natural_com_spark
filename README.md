PySpark NLP: From Sentiment Analysis to Machine Learning Pipeline

Este projeto teve como objetivo realizar uma análise de sentimentos utilizando Processamento de Linguagem Natural (NLP) com PySpark, trabalhando com avaliações de filmes do banco de dados IMDB. Durante o desenvolvimento, foi construída toda a pipeline de preparação dos dados, transformação textual e treinamento de um modelo de Machine Learning capaz de identificar automaticamente se um comentário possui sentimento positivo ou negativo.

O fluxo do projeto:

### 1. Configuração do Ambiente e Leitura dos Dados

O projeto começa com a configuração do PySpark e a criação da sessão Spark. 
Em seguida, a base de dados foi carregada.

### 2. Exploração dos Dados

Foi realizada uma análise inicial do dataset para entender a estrutura, quantidade de registros, colunas e tipos de dados. 
Também foram observados comentários positivos e negativos para identificar possíveis padrões entre os sentimentos presentes nos textos.

### 3. Limpeza e Processamento Textual

Antes de aplicar ML os textos passaram por um processo de limpeza e preparação:

* Remoção de caracteres especiais utilizando expressões regulares;
* Tokenização dos textos, separando frases em palavras;
* Remoção de stopwords, eliminando termos pouco relevantes para a análise;
* Geração de uma WordCloud para visualizar as palavras mais frequentes do conjunto de dados.

### 4. Vetorização e Transformação dos Dados

Após o processamento textual, os textos foram transformados em dados numéricos utilizando técnicas de NLP:

* Bag of Words com `CountVectorizer`;
* Técnica de hashing para redução do vocabulário;
* Aplicação do TF-IDF para atribuir maior peso às palavras mais relevantes;
* Conversão da variável de sentimento em valores numéricos (0 e 1).

### 5. Construção do Pipeline

Todas as etapas de transformação e preparação dos dados foram organizadas em um Pipeline do PySpark, permitindo automatizar todo o fluxo de processamento em uma única execução.

### 6. Treinamento do Modelo

Com os dados prontos, utilizei a Árvore de Decisão (`Decision Tree Classifier`) para realizar a classificação dos sentimentos. 
O dataset foi dividido entre treino e teste para que o modelo pudesse aprender e posteriormente ser avaliado.

### 7. Avaliação e Testes

A performance do modelo foi avaliada utilizando a métrica de acurácia. 
Além disso, adicionei novas frases, onde o modelo conseguiu classificar corretamente os comentários positivos e negativos, demonstrando sua capacidade de generalização.

link do dataset: https://www.kaggle.com/datasets/luisfredgs/imdb-ptbr?resource=download
