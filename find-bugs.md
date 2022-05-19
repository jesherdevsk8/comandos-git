## informar ao Git que você vai iniciar uma busca por determinada alteração

> git bisect start

## para informar que o estado atual do código está "ruim", ou seja, o título não está no estado que você quer

> git bisect bad HEAD

## para informar o commit em que estava correto

> git bisect good hash

## para informar o commit que está ruim

> git bisect bad hash

## ver alteração de cada commit

> git show hash

- ver o responsavel por cada linha de alteração

> git blame nome.arq
