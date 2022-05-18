# Principais comandos do Git

#### O shell padrão do git é o bash, o shell padrão do linux.

## Comandos Básicos:

### Obter ajuda dos comandos do Git
```
git help
git help git-config | git help <comando>   // Abrirá o manual do comando especificado

file:///C:/Program%20Files/Git/mingw64/share/doc/git-doc   // local dos manuais no Windows
```
### Configurar o Usuário do Git
```
git config --global color.ui true
git config --global user.name "Jesher Minelli"
git config --global user.email "jesherdevsk8@gmail.com"
ssh-keygen -t rsa -b 4096 -C "jehser@email.com"

```
### Comando de inicialização do Git
```
git init
```
### Verificar o status do Git
```
git status
```
### Adicionar arquivos no repositório local
```
git add nome.arq    // adiciona somente um arquivo
git add .      // adiciona todos arquivos da pasta
```
### Fazer um commit no repositório local
```
git commit -m "First Commit"
```
### Verificar registros de log do commit
```
git log
```
```
git log --oneline --graph --decorate --all
```

### Visualizar alterações realizadas com detalhes

- Obs adicione o hash do commit à frente do show, os três primeiros números já são o suficiente
```
git show c71e
```

### Revisar alterações atuais
```
git diff

git diff Nome-Arquivo     <-- você tbm pode especificar um arq

git diff --staged    <-- ver os comandos na Stage Area
```

### Editar título do commit
```
git commit --amend       // Abrirá o Editor padrão do teu OS
```

### Como excluir e restaurar arquivos dentro do Git

* Deletar um arquivo
```
git rm Nome-Arquivo
```
- Restaurar um arquivo após commit, com o id do commit
```
git log --diff-filter=D --summary    <- para ver o hash e o delte mode do commit

git checkout a7da3~1 Nome-Arquivo    <- para recuperar arquivo com os quatro primeiros hash seguido de ~1 do commit
``` 

### Sincronizar repositório local com repositório remoto no github
```
git remote add origin https://github.com/jesherdevsk8/teste.git
```
### Enviar repositório local para repositório remoto
```
git push -u origin master
git push    // Usar quando a master lá estiver relacionada com o repositório remoto
```
### Configurar e Setar Access Token do github no Linux
```
git config --global credential.helper cache

git config --global --unset credential.helper   // Para tirar verificação automática do Token
```
### Buscar e integrar com outro repositório  ou local branch
```
git pull
```
### Clonar repositório
```
git clone https://github.com/jesherdevsk8/teste.git
```
### Clonar repositório a partir de uma branch específica 
_*comando de clonar seguido da flag -b que significa branch, o nome da branch que deseja clonar que no exemplo abaixo é chamada de teste e por fim a url do repositório*_
```
git clone -b teste https://github.com/jesherdevsk8/teste.git 
```
### Criar uma Nova Branch, commitar e mudar

- Mostrar todas **ramificações(branch)**
```
git branch
```
- cria uma nova **ramificação(branch)**, mas você permanece na ramificação atual que efetuou o check-out.
```
git branch nova-branch
```
* _*Cria uma nova **ramificação(branch)** e alterna para essa ramificação imediatamente, podendo assim fazer o commit...*_
```
git checkout -b nova-branch2
```
* Commit 
```
git commit -m "first commit nova branch2"
```
* _*Para mudar de branch :- **por exemplo** voltar para master ou mudar para outra branch que não seja a master*_
```
git checkout master

git checkout nova-branch

git checkout nova-branch2
```
### Unir as Ramificações(Branchs)
```
git merge nova-branch
```
.
