### GIT

Git
Sistema de controle de versões. Facilita o trabalho em equipe e o controle de mudanças entre arquivos e diretórios.

Github
Plataforma online de hospedagem para repositórios Git. Existem outras como GitLab e Bitbucket.

### GIT SETUP

Instalar o Git
<a href="https://git-scm.com/" target="_blank">https://git-scm.com/</a>

Configurar Nome

```shell
$ git config --global user.name "Seu Nome"
```

Configurar Email

```shell
$ git config --global user.email "email@gmail.com"
```

### GIT COMANDOS

Inicia um repositório

```shell
$ git init
```

Adiciona o arquivo style.css ao index do git. Com o $ git add -A, adicionamos todos os arquivos.

```shell
$ git add style.css
```

Mostra os arquivos que tiveram mudanças.

```shell
$ git status
```

Irá fazer fazer o commit do código adicionado com uma mensagem.

```shell
$ git commit -m 'Descrição'
```

### CRIAR REPOSITÓRIO NO GITHUB

Github
Criar conta: <a href="https://github.com/" target="_blank">https://github.com/</a>

Novo Repositório
<a href="https://github.com/new" target="_blank">https://github.com/new</a>

Adicionar diretório remoto

```shell
$ git remote add origin https://github.com/seuusuario/seurepositorio.git
```

Push do primeiro commit

```shell
$ git push -u origin master
```

Se for a sua primeira vez
Uma tela de login irá aparecer, utilize os dados da sua conta Github.

### BRANCHINGS

Branch
Uma das principais vantagens do git é a possibilidade de criarmos 'ramificações'. Assim podemos trabalhar em funcionalidades adicionais para um projeto, sem modificarmos o 'ramificação princpal', o master.

Toda vez que formos adicionar uma nova funcionalidade, devemos iniciar criando um novo branch ao invés de fazermos alterações direto no master. O que for modificado no branch não afetara o master.

```shell
$ git branch nomebranch
```

Irá mudar de branch. Podemos usar o atalho $git checkout -b novobranch, assim ele cria e muda de branch ao mesmo tempo.

```shell
$ git checkout nomebranch
```

Mostra os branch's criados.

```shell
$ git branch
```

### WORKFLOW

Sempre crie um branch

Toda funcionalidade nova, crie um branch para desenvolver a mesma.

```shell
$ git checkout -b feature1
```

Após o desenvolvimento e commit, vá até o master e veja se existem mudanças

```shell
$ git checkout master
```

e

```shell
$ git pull
```

Volte para o branch e dê um merge com o master

```shell
$ git checkout feature1
```

e depois

```shell
$ git merge master
```

Conflitos
Se existirem conflitos você será avisado e deverá lidar com os mesmos

Git Push
Após lidar com os conflitos faça o push do branch:

```shell
$ git push
```

e

```shell
$ git push --set-upstream origin feature1
```

### LIDANDO COM PULL REQUEST

No Github
Agora você possui um novo branch no github e pode fazer o pull request (juntar ao master).

Compare e Pull Request
Pode adicionar comentários. Create Pull Request.

Merge Pull Request
Geralmente é o lider do projeto / responsável por fazer o review do seu código. Pode deletar o branch após o merge com o master.

### MAIS GIT

.gitignore
Lista de arquivos que não devem ser manipulados pelo git. node_modules é um bom exemplo.

Commit sem texto
Ao usar o `shell$ git commit` você entra no modo completo de comentário, com um editor de texto direto na linha de comando. Utilize esc + :wq para sair do mesmo.

Bitbucket
Permite repositórios privados e gratuitos. <a href="https://bitbucket.org/product" target="_blank">https://bitbucket.org/product</a>

### GITHUB PAGES

Criar repositório
O nome deve ser seuusuario.github.io

HTML Simples
O site só funcionará em html/css/js simples, sem linguagem de servidor

Qualquer projeto
Qualquer projeto poderá ter uma página para o mesmo. Vá em Settings > GitHub Pages > selecione master branch e salve. E acesso seuusurio.github.io/repositorio/
