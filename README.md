# Técnicas de Machine Learning

## Holdout
Divide dados de treino e teste aleatóriamente, por default 70% dos dados são separados para treino e 30% teste.

![holdout](https://user-images.githubusercontent.com/115194365/213077586-63cd3b76-373c-40f1-a18a-57dbcd252d83.jpg)


Vantagens:
 - Funciona bem com grandes volumes de dados, pois os dados em grande quantidade oferecem às porções de treino e teste uma variância que podem se aproximar dos dados em produção, tornando nosso modelo muito bom.
 
Desvantagens:
 - As amostras de treino e teste como são aleatórias se forem feitas com baixo volume de dados elas correm o risco de pegar porções de treino e teste muito parecidos, então essas porções pode gerar a primeira vista uma boa avaliação do modelo, porém quando coloca-mos em produção os dados em produção podem ter uma variância muito grande desproporcional às amostras tornando nosso modelo ruim.

## Cross Validation
O cross validation tem objetivo de treinar e testar o modelo com todos os dados disponíveis, pois ele realiza vários "Holdout" nos dados disponíveis gerando uma grande variância de treino e teste.

![cross](https://user-images.githubusercontent.com/115194365/213079301-8c946e9a-fe8a-4b67-b877-ff5bb8c71757.jpg)

Vantagens:
 - Evita o problema da aleatóriedade
 - Resultado robusto

Desvantagem: 
 - Problema de desempenho, pois rodar uma grande quantidade de dados pode ser demorado e custoso.
