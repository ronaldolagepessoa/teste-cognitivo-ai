# teste-cognitivo-ai
Teste técnico para a Cognitivo.ai

a. Como foi a definição da sua estratégia de modelagem?

Como estratégia, fiz testes com modelos mais simples, passando por modelos mais robustos até atingir um nível de qualidade
aceitável. É muito comum a prática de se partir imediamente para modelos mais complexos. Isso pode complicar desnecessariamente,
o processo de modelagem.

A retirada de algumas features que aparentavam não influenciar o resultado da variável target também foi uma estratégia utilizada. 

b. Como foi definida a função de custo utilizada?

Para os modelos de regressão foi utilizado o erro médio quadrático como função de custo. A minimização dessa função garante
o ajuste do modelo ao conjunto de treinamento (dentro das limitações de cada modelo é claro).

c. Qual foi o critério utilizado na seleção do modelo final?

Tanto para o modelo de regressão como para o modelo de clasificação, foi utilizado a rotina de treinamento e teste
K-Folds com k=10. Esse procedimento divide o conjunto de dados em k partes iguais, repetindo a rotina de 
teste k vezes, revesando os entre cada uma das partes em relação a escolha do conjunto de teste e conjunto de treinamento. Em cada iteração, k-1 partes são utilizadas como treinamento enquanto uma das partes é utilizada para teste. Os resultados de cada teste são sumarizados para obter a média dos mesmos.

d. Qual foi o critério utilizado para validação do modelo? Por que escolheu utilizar este método?
Para a regressão utilizamos o score r² como critério de qualidade, equanto para a classificação utilizamos a taxa de acertos.

e. Quais evidências você possui de que seu modelo é suficientemente bom?

Durante o processo de tratamento dos dados boa parte do volume de informação foi perdido. Embora, para alguns dos modelos, os resultados dos teste tenham sido satisfatórios, para garantir a operação do modelo, mais dados seriam necessários.
