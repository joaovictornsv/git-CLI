<div align="center">
  
  <img src="https://i.imgur.com/0l2bQ8n.png" width="500px">
   
  *🔧 Repositório em construção*
  
  *📖 [Dicionário Git](https://github.com/joaovictornsv/git-CLI/blob/main/dictionary.md)*
  
  *🤝 Aberto para PR's*
  
  *📝 Credits: [Beanstalk Guides](http://guides.beanstalkapp.com/) & [Git](https://git-scm.com/)*
  
 </div>
 
<hr> 

<div align="center">
  
## *Sumário*
*1. [Iniciando o git](#1-iniciando-o-git)*\
*2. [Trabalhando com Repositório remoto](#2-trabalhando-com-repositório-remoto)*\
*3. [Adicionando arquivos para área de preparação](#3-adicionando-arquivos-para-área-de-preparação)*\
*4. [Área de preparação](#4-área-de-preparação)*
  
 </div>
 
<hr>

## 1. Iniciando o git

`git init`

Rodando esse comando na sua pasta será criado um novo repositório local. <br/>
Caso essa pasta ja seja um repositório, esse será reiniciado.
<hr>

## 2. Trabalhando com Repositório remoto

Repositório remoto consite em um repositorio com **serviço de nuvem**, o qual o codigo fica armazenado além do repositório local <br/>
Exemplos de serviços de nuvem: Github, Gitlab, Bitbucket

### 2.1 Relacionando repositório local com remoto

`git remote add <nome_do_remote> https://github.com/Username/Nome_do_repositório.git` <br/>
OBS: nome do remote **normalmente** usado: `origin`
<hr>

## 3. Adicionando arquivos para área de preparação

`git add`

Antes de ficar disponível para um commit, os arquivos e/ou pastas do seu repositório precisam ser adicionados ao Git index, ou área de preparação.

O Git index contém as últimas alterações da sua árvore de trabalho antes do próximo commit.

### 3.1 Uso:
Para todas as alterações:<br/>
`git add .`

Para um arquivo específico:<br/>
`git add <nome_do_arquivo>`

Para uma pasta específica:<br/>
`git add <nome_da_pasta>`
<hr>

## 4. Área de preparação

`git commit -m 'mensagem do commit'`

Área de preparação é onde as mudanças feitas nos arquivos que foram adicionados com o `git add` serão preparadas (Staged changes)
