# Técnicas de Machine Learning

## Holdout
Divide dados de treino e teste aleatóriamente, por default 70% dos dados são separados para treino e 30% teste.

Vantagens:
 - Funciona bem com grandes volumes de dados, pois os dados em grande quantidade oferecem às porções de treino e teste uma variância que podem se aproximar dos dados em produção, tornando nosso modelo muito bom.
 
Desvantagens:
 - As amostras de treino e teste como são aleatórias elas podem pegar uma porção muito parecidas, então essa porção pode gerar uma boa avaliação do modelo, porém quando coloca-mos em produção os dados em produção podem ter uma variância muito grande desproporcional às amostras tornando nosso modelo ruim.

 
