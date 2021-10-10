# Principais comandos do Git

#### O shell padrão do git é o bash, o shell padrão do linux.

## Comandos Básicos:

### Obter ajuda dos comandos do Git

git help
git help git-config | git help <comando>   // Abrirá o manual do comando especificado

file:///C:/Program%20Files/Git/mingw64/share/doc/git-doc   // local dos manuais no Windows

### Configurar o Usuário do Git

git config --global user.name "Jesher Minelli"

git config --global user.email "jesherdevsk8@gmail.com"

### Comando de inicialização do Git

git init

### Verificar o status do Git

git status

### Adicionar arquivos no repositório local

git add nome.arq    // adiciona somente um arquivo
git add .      // adiciona todos arquivos da pasta

### Fazer um commit no repositório local

git commit -m "First Commit"

### Verificar registros de log do commit

git log

### Editar título do commit

git commit --amend       // Abrirá o Editor padrão do teu OS

### Sincronizar repositório local com repositório remoto no github

git remote add origin https://github.com/jesherdevsk8/teste.git

### Enviar repositório local para repositório remoto

git push -u origin master
git push    // Usar quando a master lá estiver relacionada com o repositório remoto

### Configurar e Setar Access Token do github no Linux

git config --global credential.helper cache

git config --global --unset credential.helper   // Para tirar verificação automática do Token

### Buscar e integrar com outro repositório  ou local branch

git pull

### Clonar repositório

git clone https://github.com/jesherdevsk8/teste.git

#### Clonar repositório a partir de uma branch específica 
#### comando de clonar seguido da flag -b que significa branch, o nome da branch que deseja clonar que no exemplo abaixo é chamada de teste e por fim a url do repositório

git clone -b teste https://github.com/jesherdevsk8/teste.git 