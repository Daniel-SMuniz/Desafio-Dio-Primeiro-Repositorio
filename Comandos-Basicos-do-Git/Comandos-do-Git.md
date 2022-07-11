# Comandos básicos do Git :computer: 

## 

## git config

- Esse comando é fundamental para configurar sua identidade de usuário, inserindo informações como nome e email que serão empregadas em cada *commit*. 

## git init

-   O comando irá criar um repositório novo em branco e, a partir daí, será possível armazenar seu código fonte, alterar, salvaguardar alterações etc.

## git clone

- O git clone é mais avançado, uma vez que ele mesmo executa um comando git init internamente. Além disso, ele verifica todo o conteúdo do projeto.

## git add

- Esse comando Git adiciona os arquivos especificados de código ao seu repositório, sejam arquivos novos ou arquivos anteriores que foram alterados. Oferece diferentes possibilidades de sintaxe.

## git commit

- É fundamental se estabelecer uma diferença entre git add e git commit:

- git add adiciona seus arquivos modificados à fila para serem submetidos a um commit posteriormente. Os arquivos **não** passaram por um commit.
- O git commit executa o commit dos arquivos que foram adicionados e cria uma nova revisão com um log. Por outro lado, se você não adicionar nenhum arquivo, o git não fará o commit de nada.

É possível combinar as duas ações em um único comando: **$ git commit -a**.

Também é possível adicionar uma mensagem para a execução de um commit. Exemplo:

**$ git commit -m “seu comentário”**

## git branch

- É comum na maior parte do tempo possuir múltiplas variações em seu repositório Git, chamadas de *branches* (“ramificações”). A grosso modo, um *branch* é um caminho independente de desenvolvimento, uma alternativa.

A princípio pode parecer fácil se perder em diversos caminhos, mas o comando git branch facilita o gerenciamento de tudo isso. Com diferentes parâmetros, é possível listar, criar ou apagar os *branches**.*

Exemplos:

**$ git branch** (lista todas as ramificações)

**$ git branch <nome_do_branch>** (cria um *branch* com o nome especificado)

**$ git branch -d <nome_do_branch>** (deleta o *branch* com o nome especificado)

## git checkout

- Ainda sobre *branches*, esse comando Git pode ser utilizado para trocar de uma ramificação para outra.

Exemplo:

**$ git checkout <nome_do_branch>**

Também é possível combinar operações, criando e fazendo o checkout de um novo *branch* com um único comando:

**$ git checkout -b <nome_do_branch_novo>**

## git remote

- O comando Git remote estabelece uma conexão entre seu repositório local e um repositório remoto.

  Exemplo:

  **$ git remote add <nomecurto> <url>**

## git push

- Esse comando serve para subir suas modificações para um repositório **remoto** conectado anteriormente com git remote.

Exemplo:

**$ git push -u <nome_curto> <nome_do_branch>**

É importante especificar a origem e o *upstream* antes de usar o git push. Veja o exemplo:

**$ git push –set-upstream <nome_curto> <nome_do_branch>** 

## git fetch

- Quando você precisa baixar as mudanças criadas por outros membros do seu projeto colaborativo, você precisa do comando Git fetch. A partir desse comando, você irá receber todas as informações de commits, para avaliar, antes de aplicar essas alterações na sua versão local do repositório.

##  git pull



- O comando Git pull baixa o conteúdo (não os metadados) do que foi alterado no repositório remoto para o seu repositório local e imediatamente atualiza seu contreúdo para a última versão.

  Exemplo:

  **$ git pull <URL>**

## git stash

-  Esse comando Git armazena temporariamente seus arquivos modificados em uma área chamada *stash* (“esconderijo”), sem interagir com os outros arquivos até ser necessário.

​         Exemplo:

​     **$ git stash**

​         Para listar todos os seus “esconderijos”, usamos:

​     **$ git stash list**

​         Quando for o momento de aplicar o conteúdo do *stash* a um *branch*, usamos o

​          parâmetro “apply”:   

​     **$ git stash apply** 

## git show

- Quer detalhes específicos sobre um commit que o log não mostra? O comando Git show é a resposta.

  Exemplo:

  **$ git show <hash_do_commit>**

## git rm

- Para remover arquivos da sua pasta, você pode utilizar o comando Git rm.

  Exemplo:

  **$ git rm <nome_do_arquivo>**

## git help

 Git tem o comando help para trazer ajuda diretamente no terminal.

Exemplo:

**$ git help <comando que se tem dúvida>** 

## git merge

Esse comando Git integra as mudanças de dois *branches* diferentes em um único *branch*. Ele precisa ser iniciado a partir de um *branch* já selecionado, que será mesclado com outro, com o nome passado por parâmetro.

Exemplo:

**$ git merge <nome_do_branch>**

## git rebase

Git rebase a princípio parece fazer o mesmo que um comando git merge: ele integra dois *branches* em um *branch* único. Porém, esse comando refaz o histórico de commits, tornando-o linear. É o mais indicado para consolidar múltiplos *branches*.

Exemplo:

**$ git rebase <base>**

##  git pull –rebase

Essa é uma variação do comando pull mostrado anteriormente. A partir dessa instrução, o Git irá fazer um rebase (não um merge) depois de se utilizar um comando pull.

Exemplo:

**$ git pull –rebase**

## git cherry-pick

Esse é um comando poderoso que permite selecionar qualquer commit específico de um *brach* e aplicá-lo a outro *branch*, sem precisar de uma mescla completa. A operação fica adicionada no histórico.

Exemplo:

**$ git cherry-pick <commit-hash>**

## git archive 

Esse comando Git combina múltiplos arquivos em um único arquivo, como se fosse um arquivo zipado. Esse pacote pode ser aberto depois e os arquivos contidos podem ser extraídos individualmente.

Exemplo:

**$ git archive –format zip HEAD > archive-HEAD.zip**

## git blame

- O comando “dedo-duro”, blame ajuda a determinar qual usuário realizou qual mudança em um determinado arquivo.

Exemplo:

**$ git blame <nome_do_arquivo>**    

## git tag

- Tags são uma boa opção para marcar uma *branch* e evitar alteração, principalmente em releases públicos.

  Exemplo:

  **$ git tag -a v1.0.0**

  ## git diff

- Para comparar dois arquivos gits ou dois *branches* **antes** de passarem por um commit ou um push, é importante executar esse comando Git.

  Exemplos:

  comparando o repositório ativo com o repositório local: **$ git diff HEAD <nome_do_arquivo>**

  comparando duas ramificações: **$ git diff <\*branch\* de origem> <\*branch\* de destino>**

  ## git citool

- Esse comando Git oferece uma alternativa gráfica ao commit.

  Exemplo:

  **$ git citool**

  ## git whatchanged

- Esse comando oferece informações de log, mas em formato raw.

  Exemplo:

  **$ git whatchanged**

  

  











  





































