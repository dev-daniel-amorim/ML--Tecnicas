# Holdout x Cross Validation

## Separação de dados (particionamento)

Após a etapa de pré-processamento dos dados vem a etapa de machine learning, a primeira ação do ML é a separação dos dados em:
- Treino: Serve para treinar/ensinar o modelo;
- Teste: Serve pra comprovar que nosso modelo funciona. Estes dados não participam do treinamento do nosso modelo.<br>

Importante salientar que essa separação dos dados deve ser feita de maneira aleatória garantindo a diversidade dos dados.

# Método HoldOut
É o modo mais simples de particionamento, mais rápido e menos custoso em termos de processamento porém não é indicado para grandes volumes de dados pois a menor parte dos dados (teste) pode não ter dado o suficiente para determinar o todo (treino) diminuindo sua acurácia. Esse método consiste em separar os dados (por default) em 70% de treinamento e 30% teste, mas isso é relativo, vai depender do seu volume de dados e deve ser ajustado visando a melhoria na predição.

![holdout](https://user-images.githubusercontent.com/115194365/213264298-6d8b6a25-ef72-49ce-9aa0-b809aff380a4.jpg)

Como dissemos anteriormente esse modelo funciona para pequenas quantidades de dados, imagine uma situação em que, você valida seu modelo com acurácia de 80%, e informa ao seu chefe que marca uma apresentação do seu modelo, na apresentação seu modelo apresenta uma acurácia de 63%? Isso vai acontecer! pois sua base de treino e teste muda a cada execução do código implicando em variação da acurácia. No link abaixo fiz uma comparação entre os metodos Holdout e cross validation, note que Holdout sofre variação da sua acurácia enquanto cross validation se mantem estável.

[Clique aqui para ver o código fonte](https://github.com/dev-daniel-amorim/ML-Tecnicas/blob/main/Tecnicas%20de%20ML.ipynb)

# Cross Validation
Antes de comprender validação cruzada vamos entender que separar dados em treino e teste não é o suficiente para garantir um excelente modelo preditivo, mas o modo como esses dados são separados, ou particionados, é que podem fazer a diferença na acertividade do modelo.<br>
O Cross validation são métodos que visam melhorar a acertividade a partir do particionamento dos dados, diferentemente do holdout no cross validation são geradas X iterações nos dados de teste e treino, e o algoritmo faz uma média entre elas melhorando sua acurácia.

# Métodos de Cross Validation
## 1. Método K-fold
Esse método consiste em dividir os nossos dados em K partes iguais (por default em 10 partes), para cada parte ele executa o HoldOut, garantindo assim que os dados de treino e teste "conhecam" toda nossa base de dados, depois realiza uma média entre esses dados tornando mais acertiva nossa acurácia.



## 3. Método Leave-one-out (LOOCV)
pouco usado custoso


