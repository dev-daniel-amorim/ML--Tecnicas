# Validação Cruzada

Antes de entendermos validação cruzada, vamos falar sobre a divisão dos dados, após a etapa de pré-processamento dos dados vem a etapa de machine learning, a primeira ação do ML é a separação dos dados em:
- Treino: Serve para treinar/ensinar o modelo;
- Teste: Serve pra comprovar que nosso modelo funciona. Estes dados não participam do treinamento do nosso modelo.<br>

Importante salientar que essa separação dos dados deve ser feita de maneira aleatória garantindo a diversidade dos dados. 

# O que é a validação cruzada? (Cross Validation)
Separar dados não é o suficiente para garantir um excelente modelo preditivo, mas o modo como esses dados são separados, ou particionados, é que geram o que chamamos de Cross Validation, ou validação cruzada, em suma, vamos considerar que cross validation significa particionar dados, então esse modo de "particionar" pode ser dividido em:

## 1. Método HoldOut
É o modo mais simples de particionamento, mais rápido e menos custoso em termos de processamento porém não é indicado para grandes volumes de dados. Por default os dados são divididos em 70% de treinamento e 30% teste, mas isso é relativo, vai depender do seu volume de dados.

![holdout](https://user-images.githubusercontent.com/115194365/213264298-6d8b6a25-ef72-49ce-9aa0-b809aff380a4.jpg)

Como dissemos anteriormente esse modelo funciona para pequenas quantidades de dados, imagine uma situação em que, você valida seu modelo com acurácia de 80%,voçê informa ao seu chefe que aprova esses 80% e marca uma apresentação do seu modelo, na apresentação seu modelo apresenta uma acurácia de 63%? Isso pode acontecer pois em holdout tanto os dados de treino quanto os de teste não conhecem toda sua base de dados, para melhorar isso vamos para próximo método de validação cruzada, o k-fold.

## 2. Método K-fold
