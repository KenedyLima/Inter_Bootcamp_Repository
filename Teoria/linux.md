# Linux :penguin:



## Guia de conteúdo

- Sobre o Linux
- Manipulando arquivos
- Manipulando usuários
- Manipulando grupos
- Informações do sistema
- Zipando arquivos
- Instalando programas



## Sobre o Linux

Criado por Linus Torsvaldx e seu time.



Linux não é sistema operacional, mas sim o _Kernel_ do Sistema.

_Kernel_ tem a função de comunicar os Hardwares com o Sistema Operacional.



## Manipulando Arquivos

- ls: Lista diretórios e arquivos
- cd: Muda de diretório
- touch: Cria arquivos
- cat: Mostra o conteúdo de arquivos
- tac: Mostra o conteúdo de arquivos começando por baixo
- nano: Editor de texto
- rmdir: Remove diretórios vazios
- rm: Remove arquivos
- rm -r: Remove diretórios não vazios

## Manipulando Usuários

- adduser: Adiciona um novo usuário
- logname: Mostra o usuário atual
- cat /etc/passwd: Mostra todos os usuários
- su: Muda de usuário
- passwd: Muda a senha de usuário
- deluser: Remove usuário
- deluser -r: Deleta usuário e pasta pessoal

## Manipulando Grupos

- addgroup: Adiciona um novo grupo
- cat /etc/group: Mostra todos os grupos existentes
- addgroup <user> <groupname>: Adiciona um usuário a um grupo
- delgroup <user> <groupname>: Remove um usuário de um grupo
- groups: Mostra os grupos que o usuário pertence
- delgroup: Remove um grupo

