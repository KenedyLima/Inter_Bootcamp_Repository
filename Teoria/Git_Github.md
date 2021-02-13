# 								Git e Github



## Guia de conteúdo

- GUI x CLI
- Git: Debaixo dos Panos

- Objetos do Git

- Iniciando um Repositório com o Git

- Ciclo de vida dos Arquivos no Git

- Empurrando o Repositório Local para o Repositório Remoto

  

## Guia de comandos

- openssl sha1 <NOME DO ARQUIVO>
- git cat-file -t <SHA1 DO ARQUIVO>
- git init
- git add *
- git remote add origin <url do repositorio>

- git push origin master



## GUI x CLI

### GUI: Graphic User Interface

Interface de usuário onde é possível uma Interação Gráfica.

### CLI: Command Line Interface

Interface de usuário onde é possível interação somente atráves de Linhas de Comandos.



## Git: Debaixo dos Panos

O **Git** utiliza _Secure Hash Algorithm_ para encriptar os arquivos e deixá-los mais seguros pelo fato de usar um sistema distribuído.



### Secure Hash Algorithm (SHA1)

Algorítmo de encriptação que utiliza 40 caracteres. Esse algorítmo é super seguro pelo fato de facilitar a identificação em caso de alteração do conteúdo dos arquivos.

#### CHECANDO SHA1 DOS ARQUIVOS

**command line:**

openssl sha1 <NOME DO ARQUIVO>

**output**:

Será retornado 40 caracteres contendo números e letras.



## Objetos do Git

Checando o tipo de objeto dos objetos do seu repositório:

**command line:**

git cat-file -t <SHA1 DO ARQUIVO>

**output:**

Retornará qual tipo de objeto é esse



### Blobs

Os Blobs armazenam o conteúdo dos arquivos.

Ele também armazena metadados como:

- Tamanho
- Tipo

### Trees

As Trees armazenam arquivos (Blobs) e outras Trees. 

Correspondem a diretórios.



​				-- -- -- -- -- -- -- -- -- -- -- -- -- - -- -- -- -- -- -- -- -- --  **TREE** -- -- -- -- -- -- -- -- -- -- -- -- -- - -- -- -- -- -- -- -- -- --

​				I													   					   	I                                                                                   I

​				I														                          I																				   I

​				I														                          I																				   I

​			**BLOB**                                                                         **BLOB**                                                                          **TREE**

​																																													   I

​																																													   I

​																																									    		  **BLOB**

### Commits	

Os commits servem para dar uma significado á cada ciclo de vida no git, facilitando o entendimento de cada alteração nos arquivos.

Ele armazena informações importantes como:

- Autor 
- Mensagem 



## Iniciando um Repositório com o Git

Para iniciar um repositório Git rodar a seguinte linha de comando.

Dentro da pasta desejada inicie com:

**command line:**

git init

**output:** 

NULL



## Ciclo de vida dos Arquivos no Git

Todos os arquivos passam por 4 fases no seu ciclo de vida. 

- Untracked
- Tracked
  - Unmodified
  - Modified
  - Staged



### Untracked

Os arquivos nessa fase do ciclo não fazem parte dos arquivos que o git tem ciência da existência.

Para mudar o estado de um arquivo de _Untracked_ para  _Tracked_ use:



**command line:**

git add *

**output:**

Não será retornado nada, caso tenha, você obteve algum erro.



Com esse comando você adiciona todos os seus arquivos para o git, o "*" serve para isso.

Caso queira adicionar um arquivo específico troque o "*" pelo nome do arquivo.



### Tracked

#### Unmodified

Arquivos que ainda não foram modificados.

#### Modified

Arquivos que já sofreram alterações.

#### Staged

Os novos arquivos que são adicionados ao Git vem direto para essa fase.

Nessa fase do ciclo o arquivo está a espera de um commit para ser salvo.



Após "commitarmos" nossos arquivos, nosso commit entra em um estado de loop eterno, sempre passando pela fase _Unmodified_, _Modified_ e por fim _Staged_. Sempre esperando por um novo commit.



Caso esteja com alguma dúvida sobre o estado dos seus arquivos, dê um **_git status_** e o git te retornára todas as pêndencias com o seu repositório.

## Empurrando Repositório Local para o Repositório Remoto

Depois de iniciar seu repositório local, é necessário empurrá-lo para um _Code Hosting_ que será seu repositório remoto.

O mais utilizado é o Github, mas existem muitos outros.



### Adicionando o repositório

Depois de criar seu repositório no Github é necessário adicioná-lo no git.

Para adicionar o repositório use:

**command line:**

git remote add origin <url do repositorio>



### Empurrando o repositório

Depois de checar com o _git status_ se você não tem nenhuma pendência com seu repositório, já pode empurrá-lo para o Github. Para isso use:

**command line:**

git push origin master



