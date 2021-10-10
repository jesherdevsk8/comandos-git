## Criar e setar Token de acesso Pessoal Github e Git no Linux (Manjaro-Linux)

### Entre no github.com    

1. No canto superior direito de qualquer página,
clique na sua foto de perfil e, em seguida, clique em Configurações
2. Na barra lateral esquerda, clique em Developer settings (Configurações do desenvolvedor).
3. Na barra lateral esquerda, clique em Personal access tokens (tokens de acesso pessoal).
4. Click Generate new token.
5. Give your token a descriptive name.
  "My bash Script"
6. To give your token an expiration, select the Expiration drop-down menu, then click a default or use the calendar picker.
7. coloque a opção No expiration   Obs( Se for um token pessoal )
8. Selecione todas permissões possíveis Obs( Se tbm for um token pessoal )
9. Click Generate token.

### Feito Isso - Execute no terminal o comando

git config --global credential.helper cache

Login: Seu Usuario

Senha: Token Aqui

### Para Retirar a Chave de Acesso

git config --global --unset credential.helper   // Para tirar verificação automática do Token