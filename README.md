<div align="center">
  
  <img src="https://i.imgur.com/0l2bQ8n.png" width="500px">
   
  *🔧 Repositório em construção*
  
  *📖 [Dicionário Git](https://github.com/joaovictornsv/git-CLI/blob/main/dictionary.md)*
  
  *🤝 Aberto para PR's*
  
  *📝 Credits: [Beanstalk Guides](http://guides.beanstalkapp.com/) & [Git](https://git-scm.com/)*
  
</div>
 
<hr> 

> ## *Sumário*
> *1. [Iniciando o git](#1-iniciando-o-git)*\
> *2. [Trabalhando com Repositório remoto](#2-trabalhando-com-repositório-remoto)*\
> *3. [Adicionando arquivos para área de preparação](#3-adicionando-arquivos-para-área-de-preparação)*\
> *4. [Área de preparação](#4-área-de-preparação)*\
> *5. [Criando branches](#5-criando-branches)*\
> *6. [Contribuindo com repositórios de terceiros](#6-contribuindo-com-repositórios-de-terceiros)*

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

### 4.1 Atalho

Com o comando abaixo, irá criar um commit com os arquivos marcados como **Commit candidate** e os **modified** e junta com a mensagem, mensagem do commit.

`git commit -am 'mensagem do commit'`

<hr>

## 5. Criando branches

Esse **master** é um **branch** que o git cria automagicamente quando você faz um commit sem estar em nenhum branch (como é o caso de um repositório recém criado).

> OBS: No github, por default, todo novo repo terá a branch nomeada como **main**, substituindo o branch **master**.

Quando usamos Git, quase todas as operações são feitas dentro de um branch. Um branch nada mais é que uma lista de commits. Você pode criar, apagar e renomear branches.

Para criar você usa o comando `git branch NOME_DO_BRANCH`. Para apagar `git branch -D NOME_DO_BRANCH`. E para renomear você usa `git branch -m NOME_ANTIGO NOME_NOVO`.

Exemplo:

- `git branch work` cria o branch work
- `git branch -D work` apaga o branch work
- `git branch -m work asdrubal` renomeia o branch work para asdrubal


### 5.1 Unindo branches

Para combinar as mudanças feitas de uma branch para outra branch usamos o comando ```git merge <nome_da_branch>```.

Exemplo: Unindo as mudanças feitas na branch **new_feature** na branch atual:

```git merge new_feature```

<hr>

## 6. Contribuindo com repositórios de terceiros

Um grande diferencial de plataformas **open-source** é a possibilidade de **contribuir com repositórios de terceiros**, para isso é preciso seguir os seguintes passos:

**1 -** Vá até o repositório que deseja contribuir `https://github.com/Username/Nome_do_repositório`
<br><br>

**2 -** Fork o repositório, com isso você criará uma **ramificação** do repositório principal, a qual poderá fazer mudanças, <br>
       pois essa será a **SUA** versão do projeto principal 
<br><br>

**3 -** Clone seu repositório "forkado" do projeto principal com: `git clone https://github.com/Seu_Username/Nome_do_repositório.git`
<br><br>

**4 -** Crie uma nova Branch: <br>
 `cd repositório` <br>
 `git branch nome_da_nova_branch`
 <br><br>
 
 **5 -** Mude para a nova branch: `git checkout nome_da_nova_branch`
 <br><br>
 
 **6 -** Faça alterações no seu repositório "forkado" e use o comando push <br>
 já que esta ultilizando uma nova branch, use o comando `git push --set-upstream origin nome_da_nova_branch`
 <br><br>
 
 **7 -** No github clique em **"Compare e Pull Request"** para enviar para o usuário do repositório as mudanças feitas comparadas com o repositório principal, com isso ele irá analisar as alterações e decidir aceitar ou não suas mudanças, com um Merge(adicionar suas mudanças ao codigo principal) <br>
**obs: importante deixar um comentário no pull request, explicando oque foi alterado no código**
