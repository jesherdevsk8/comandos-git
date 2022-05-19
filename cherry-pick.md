## Pegar commit de outra branch

**podemos trazer um único commit específico de outra branch para a branch em que estamos trabalhando.

Em que caso faz sentido trazer um commit específico para a branch atual?**

_Se uma implementação é necessária em sua branch e já foi feita em outra branch, pode fazer sentido trazer um commit específico, utilizando o git cherry-pick._

- crie uma nova branch

> git checkout -b nova-release

_Faça sua alteração e commit nela_

- Vamos supor que apareceu um novo bug na aplicação e você teve que parar o que estava fazendo, porém você comitou as alterações

- Faça checkout para master ou para outra branch que vai trabalhar
- Se caso precisar das alterações feitas no teu ultimo commit, execute

> git cherry-pick de82d78 

_Cole o hash do commit da sua branch nova-release_

_Execute o comando git rebase novo-release e confira que o Git executa apenas um trabalho, embora hajam dois commits na nova branch, pois um já foi trazido para o master_

> git rebase nova-release

