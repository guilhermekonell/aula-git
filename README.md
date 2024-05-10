# GIT - Comandos básicos

## Configurações básicas

Para setar o nome que será demonstrado em nossos commits e operações:

```
git config --global user.name "Fulano de Tal"
```

Para setar o email que será demonstrado em nossos commits e operações:

```
git config --global user.email fulano.tal@gmail.com
```

## Inicializar um novo repositório

Para inicializar um novo repositório, basta executar o seguinte comando:

```
git init
```

Este comando irá criar um novo repositório na pasta posicionada atualmente. Também irá criar uma pasta `.git` que é usado para controle do próprio git.

## Clonar um repositório já existente

Para clonar um repositório já existente, executamos o comando:

```
git clone <link para o repositório>
```

Este comando irá fazer uma cópia do repositório remoto.

## Gravar novas alterações em arquivos

Para gravar novas alterações, executamos primeiramente o comando:

```
git add <path do arquivo>
```
ou
```
git add .
```
para adicionar todos os arquivos alterados.

## Visualizar o status das alterações

Para visulizar os status das alterações, executamos o comando

```
git status
```

Este comando irá listar no prompt de comando, os arquivos alterados e seu status.

## Vizualizar modificações

Para visualizar as modificações que foram feitas nos arquivos, executamos o comando:

```
git diff
```
ou
```
git diff <path de um arquivo>
```
para visualizar as modificações de um arquivo específico.

Este comando irá demonstrar no prompt de comando as modificações que foram realizadas nos arquivos.

## Modificando arquivos

Para efetivar as modificações dos arquivos em nosso repositório Git, utilizamos o comando:

```
git commit -m "<Mensagem>"
```

Também temos a possibilidade de refazer o ultimo commit para adicionar um novo commit ou alterar a mensagem. Para isso executamos:

```
git commit -m "<Mensagem>" --amend
```

## Desfazendo alterações

Para que possamos desfazer alterações enviadas ao repositório do Git, executamos o seguinte comando:

```
git reset --soft HEAD~1
```

Também podemos voltar o nosso repositório para um commit específico:

```
git reset --hard XXXXXXXXX
```

Obs: Cuidado ao utilizar o parâmetro "--hard", pode ser que esse processo faça você perder arquivos e modificações que você não deseja.

## Criando branchs de trabalho

Para criar uma nova branch, executamos o seguinte comando:

```
git branch teste
```

Para posicionarmos o nosso respositório local nesta branch, utilizamos o comando:

```
git checkout teste
```

Ou podemos fazer isso utilizando o seguinte comando:

```
git checkout -b teste
```
Este comando irá fazer o processo de criar e posicionar nesta branch em um único passo.

## Visualizando logs das alterações

Para visualizar um log sobre as alterações que ocorreram no passado, utilizamos o comando:

```
git log
```

Este comando irá listar no nosso prompt de comando, um log das alterações que já foram realizadas anteriormente.

## Atualizando seu repositório local com as novas alterações no repositório remoto

Para que possamos atualizar a nossa branch com as alterações contidas no repositório remoto, utilizamos o seguinte comando:

```
git fetch origin
```

e após, podemos atualizar a nossa branch local com as novas alterações:

```
git pull origin teste
```

## Resolvendo conflitos

Para resolver conflitos, executamos os seguintes passos:

- texto ao contrário.
