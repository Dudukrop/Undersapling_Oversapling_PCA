# Census Data Processing and Classification

Este projeto envolve a análise e processamento de dados do censo para prever a faixa de renda dos indivíduos. Utilizando técnicas de aprendizado de máquina e pré-processamento de dados, o projeto implementa classificadores para prever se a renda de uma pessoa é superior a $50.000 por ano.

## Overview do Projeto

O projeto utiliza um conjunto de dados de censo com 32.561 entradas, cada uma contendo 15 atributos, incluindo idade, trabalho, educação, estado civil, ocupação, e mais. O objetivo é prever a variável alvo `income`, que indica se a renda de um indivíduo é maior ou menor/igual a $50.000.

## Etapas do Projeto

### Importação de Bibliotecas e Carregamento de Dados

- Bibliotecas utilizadas: `pandas`, `numpy`, `matplotlib`, `seaborn`, `sklearn`, `imblearn`.
- O dataset é carregado usando `pandas` e inspecionado para entender a estrutura dos dados.

### Análise Exploratória de Dados

- Contagem de instâncias em cada classe de renda utilizando `seaborn` para criar um gráfico de barras.
- Uso de `numpy` para obter a distribuição de classes em `income`.

### Pré-processamento de Dados

- **Label Encoding**: Transformação de variáveis categóricas em numéricas para processamento eficiente.
- **One-Hot Encoding**: Conversão de colunas categóricas em colunas binárias para melhor representação no modelo.

### Balanceamento de Dados

- **Undersampling**: Uso da técnica Tomek Links para reduzir a classe majoritária e melhorar o equilíbrio.
- **Oversampling**: Utilização da técnica SMOTE para aumentar a classe minoritária.

### Divisão dos Dados

- Os dados são divididos em conjuntos de treinamento e teste utilizando `train_test_split` do `sklearn`.

### Treinamento do Modelo

- **Random Forest Classifier**: Um modelo de floresta aleatória é treinado para prever a faixa de renda.
- Ajuste dos hiperparâmetros `n_estimators`, `criterion`, `min_samples_leaf`, e `min_samples_split`.

### Avaliação do Modelo

- **Métricas de Avaliação**: Uso de `accuracy_score` e `classification_report` para avaliar o desempenho do modelo.
- Comparação dos resultados do undersampling e oversampling para entender o impacto no desempenho.

### Redução de Dimensionalidade

- **PCA**: Aplicação da Análise de Componentes Principais para reduzir a dimensionalidade dos dados e melhorar a eficiência computacional.

## Conclusão

Este projeto demonstra o uso de várias técnicas de pré-processamento de dados e balanceamento de classes para melhorar a precisão de modelos de aprendizado de máquina na previsão de faixas de renda. O uso de técnicas como undersampling e oversampling, junto com o PCA, ajuda a lidar com problemas de desbalanceamento e complexidade dos dados.

## Requisitos

- Python 3.x
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Imbalanced-learn

## Execução do Projeto

1. Certifique-se de ter todas as bibliotecas necessárias instaladas.
2. Carregue os dados do censo e execute o script de pré-processamento.
3. Treine o modelo usando os dados preparados.
4. Avalie o desempenho do modelo utilizando os conjuntos de teste.

## Referências

- [Scikit-learn Documentation](https://scikit-learn.org/stable/documentation.html)
- [Imbalanced-learn Documentation](https://imbalanced-learn.org/stable/)
