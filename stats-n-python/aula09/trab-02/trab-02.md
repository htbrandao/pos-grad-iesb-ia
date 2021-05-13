# Trabalho 02

Neste trabalho, utilizaremos o dataset da aula passada: fraudes em cartões de crédito.

Note que o dataset é extremamente desbalanceado, com apenas cerca de 0.17% das transações sendo fraudulentas.

Para informações a respeito das colunas, consulte a referência no Kaggle apresentada no arquivo `Reference.txt`.

(Source: [https://www.kaggle.com/mlg-ulb/creditcardfraud](https://www.kaggle.com/mlg-ulb/creditcardfraud))

Sua tarefa consiste em realizar pelo menos as seguintes tarefas:

- Visualização do histograma de gastos geral do dataset (atente-se para uma escolha adequada do parâmetro **bins**)

- Visualização dos histogramas de gastos das transações fraudulentas e das transações não fraudulentas em separado (atente-se para uma escolha adequada do parâmetro **bins**)

- Para cada histograma gerado, indique, utilizando QQ-Plot, qual distribuição mais se adequa a ele e caracterize a distribuição (média e desvio padrão)

- Realize um teste A/B da seguinte forma: separe, aleatoriamente, dois grupos. O grupo A deve conter 50% das transações não fraudulentas e 50% das transações fraudulentas. O grupo B, por sua vez, deve conter os dados restantes. Por exemplo, se o dataset tivesse 100 transações (sendo 80 não fraudulentas e 20 fraudulentas), o grupo A teria 40 transações não fraudulentas e 10 transações fraudulentas (as mesmas quantidades se aplicariam ao grupo B). O grupo A deve ser o grupo de controle. O grupo B será o grupo que receberá a nova técnica de identificação de transações fraudulentas. Essa técnica consiste em: caso a transação possua um valor maior ou igual a 122.20, ela deve ser classificada como fraudulenta. Avalie o desempenho dessa nova técnica sobre a porcentagem de transações fraudulentas do grupo A. Qual a porcentagem das transações que realmente eram fraudulentas realmente foram classificadas como fraudulentas? A técnica aplicada no grupo B é melhor do que a do grupo A?

- Realize o seguinte teste de hipótese: transações fraudulentas possuem valores de gasto, na média, maiores ou iguais a 122.20 e

- Utilizando as classes `LogisticRegression` e `SMOTE`, realize oversampling e treine o modelo, relatando qual a porcentagem de transações fraudulentas detectadas.

  - Observação: para esta última tarefa, não utilize `pd.get_dummies`, faça apenas `X = df['Amount']`.