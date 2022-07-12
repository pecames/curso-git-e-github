# Roadmap Git/GitHub

---

## 🤔 Contextualizando o Git/Github

### Conceito e Objetivo

- Git
    
    O maior, mais moderno e mais famoso *[sistema de controle de versão](https://www.atlassian.com/br/git/tutorials/what-is-version-control#:~:text=Os%20sistemas%20de%20controle%20de,forma%20mais%20r%C3%A1pida%20e%20inteligente.)* do mundo **hoje**. O *[Git](https://git-scm.com/)* é um projeto de *[código aberto](https://pt.wikipedia.org/wiki/C%C3%B3digo_aberto#:~:text=C%C3%B3digo%20aberto%20(do%20ingl%C3%AAs%20Open,necessidade%20de%20pagar%20uma%20licen%C3%A7a)* e com manutenção ativa, desenvolvido em 2005 por *[Linus Torvalds](https://pt.wikipedia.org/wiki/Linus_Torvalds)*(criador do kernel do OS Linux).
    
    O Git é um sistema de controle de versão distribuído. Em vez de ter apenas um único local para o histórico completo das alterações do software, nele, todas as cópias feitas por cada desenvolvedor também possui o histórico completo de todas as versões anteriores.
    
    Além de ser distribuído, o Git foi projetado com desempenho, segurança e flexibilidade em mente.
    
- GitHub
    
    O *GitHub* é considerado é uma ferramenta essencial para o desenvolvimento de software. Atualmente, ele acomoda mais de 25 milhões de usuários, um número considerável de profissionais que estão utilizando o GitHub para melhorar o fluxo de trabalho e a colaboração.
    
    Basicamente, o GitHub é um serviço baseado em nuvem que hospeda um sistema de controle de versão(Git). Ele permite que os desenvolvedores colaborem e façam modificações em projetos compartilhados, mantendo um registro detalhado do seu progresso.
    

### Aplicação e Usabilidade

Um sistema de controle de versão, independente do tamanho da sua aplicação, é extremamente necessário para manter a organização, controle e segurança do seu sistema. Com isso, para um profissional de T.I é indispensável o conhecimento nesse tipo de ferramenta.

A ferramenta Git, sendo a maior do mercado, é requisito mínimo nas maiorias das vagas de T.I. E mesmo que nem todas as empresas utilizam o GitHub como como ferramenta principal, é sempre bom ter e manter o seu perfil bem atualizados com projetos pessoais e colaborações em projetos alheios.

Todos sabemos que existem diversas vantagens de manter seus projetos em nuvem, mas o Git não é só isso. O fato de ter todas as alterações feitas e a possibilidade de controlar e voltar em códigos de versões anteriores é um ótima funcionalidade e que salva os desenvolvedores diversas vezes, quando acabamos enviando algo errado por engano para o repositório principal.

Podendo também criar ramificações do projeto para trabalhar nele sem que atrapalhe os outros *devs* envolvidos no projeto também evita uma grande dor de cabeça.

Isso sem contar que cada desenvolvedor tem sua própria versão do mesmo projeto em sua máquina, fazendo com que ele possa fazer tudo que pode fazer no repositório principal.

O Git não resolve absolutamente todos os nosso problemas, e é certo que não é a “solução perfeita”, mas com certeza é o **melhor que temos até agora**.

### Exemplos e comparativos

- Exemplos
    
    **Empresas brasileiras que utilizam o GitHub**
    
    - [Nubank](https://github.com/nubank)
    - [QuintoAndar](https://github.com/quintoandar)
    - [Wirecard](https://github.com/wirecard)
    - [VTEX](https://github.com/vtex)
    
    **Empresas do exterior que utilizam o GitHub**
    
    - [Spotify](https://github.com/spotify)
    - [Pinterest](https://github.com/pinterest)
    - [Meta](https://github.com/facebook)
    - [Google](https://github.com/google)

Existem outros sistemas que concorrem com o GitHub, cada um com suas vantagens, desvantagens e característica.

Alguns desses sistemas são:

- [GitLab](https://about.gitlab.com/)
- [Bitbucket](https://bitbucket.org/)
- [GNU Savannah](https://savannah.gnu.org/)
- [SourceForge](https://sourceforge.net/)
- [Gitea](https://gitea.io/pt-br/)

---

## 🛠️ Praticando e aprendendo

### Crie sua conta

- Registre-se em *[github.com/singup](https://github.com/signup)*.

### Interface GitHub

Tour pela interface do GitHub.

- Overview
- Repositories
- Projects
- Packages
- Stars

### Iniciando projeto

- git config
    
    O primeiro passo no terminal é fazer a configuração de email e nome. Com ela você pode definir como aparecerá o seu nome durante as ações que fará no repositório
    
    ```bash
    $ git config --global user.name "Fulano da Silva"
    $ git config --global user.email fulanodasilva@exemplo.br
    ```
    
- git init
    
    Com o comando “*git init*” nós inicializamos o nosso repositório git dentro de um projeto. Isso significa que uma pasta oculta, chamada “*.git*” será criada na raiz do nosso projeto.
    
    Essa pasta vai conter arquivos que são necessários para fazer todo gerenciamento dos arquivos do nosso projeto, além de conter as funcionalidades disponibilizadas pelo sistema de gerenciamento.
    
    ```bash
    $ git init
    ```
    
- git remote
    
    Resumidamente, o git remote vai ser responsável por controlar o local remoto do seu repositório. Com ele podemos definir para onde estaremos enviando as alterações feitas no nosso ambiente local.
    
    ```bash
    git remote add origin "https://github.com/username/repositorie"
    ```
    

### Add, reset e restore

- Add
    
    Com o *[git add](https://git-scm.com/docs/git-add)* adicionamos as alterações feitas no repositório à lista de arquivos que vão considerados para serem enviados ao repositório remoto
    
    ```bash
    ## Adicionar arquivo separado ao stage
    $ git add arquivo.js
    
    ## Adicionar todos os arquivos ao stage
    $ git add .
    ```
    
- Reset
    
    O *[git reset](https://git-scm.com/docs/git-reset)* é, basicamente, o oposto do *git add*. Ele remove os arquivos da lista de arquivos à serem considerados no commit.
    
    ```bash
    ## Remover arquivo separado ao stage
    $ git reset arquivo.js
    
    ## Remover todos os arquivos ao stage
    $ git reset .
    ```
    
- Restore
    
    O comando *[git restore](https://git-scm.com/docs/git-restore)* restaura arquivos **modificados** que ainda não foram adicionados com o *git add*
    
    ```bash
    ## Adicionar arquivo separado ao stage
    $ git restore arquivo.js
    
    ## Adicionar todos os arquivos ao stage
    $ git restore .
    ```
    

### Primeiro ‘commit’

```bash
$ git commit -m "first commit"
```

- Flags adicionais
    
    ```bash
    ## Passe a flag -m antes da mensagem do commit
    $ git commit -m "first commit"
    
    # A flag -a pode ser usada para adicionar os arquivos modificados durante o commit
    ## Essa flag reprensenta o git add não adicionar arquivos novos
    $ git commit -a -m "first commit"
    
    ## As flags também podem ser usada em conjunto
    $ git commit -am "first commit"
    ```
    

### Pull, fetch & push

- Pull
    
    O [*git pull*](https://git-scm.com/docs/git-pull) é o comando usado para atualizar as branchs locais em relação às suas respectivas cópias remotas. 
    
    ```bash
    ## Busca a cópia remota e atualiza a branch atual através do merge de forma automática
    $ git pull
    
    ## Busca a cópia remota da branch que deseja buscar e faz o merge automático
    $ git pull origin master
    
    ## Busca a cópia remota da branch que deseja buscar e faz o merge automático
    $ git pull origin master
    
    ## Busca a cópia remota mas não faz o commit do merge
    $ git pull --no-commit origin master
    ```
    
- Fetch
    
    O *[git fetch](https://git-scm.com/docs/git-fetch)* é o comando responsável por atualizar a cópia remota no seu ambiente local.
    
    ```bash
    ## Atualiza as cópias das branchs remotas no seu ambiente local
    $ git fetch
    
    ## Atualiza uma cópia específica da branch remota no seu ambiente local
    $ git fetch origin master
    ```
    
- Push
    
    O comando *[git push](https://git-scm.com/docs/git-push)* é responsável por enviar as alterações  do seu ambiente local para o servidor remoto do git.
    
    ```bash
    ## Enviando branch local para servidor remoto
    $ git push origin master
    ```
    

### Criando e removendo branchs

As *[branchs](https://git-scm.com/docs/git-branch)* são semelhantes a linhas temporais diferentes, onde podemos criar funcionalidades, editar e remover arquivos, sem alterar a linha do tempo principal.

- Branchs locais
    
    Listando branchs
    
    ```bash
    ## O comando abaixo vai listar todas as branchs locais
    $ git branch
    ```
    
    Criando uma nova branch
    
    ```bash
    ## Utilizando o comando a baixo você criará uma cópia da branch atual
    $ git branch nome_da_branch
    ```
    
    Removendo uma branch
    
    ```bash
    ## Para remover uma branch basta adicionar a flag -D
    $ git branch -D nome_da_branch
    ```
    
- Branchs remotas
    
    Listando branchs
    
    ```bash
    ## O comando abaixo vai listar todas as branchs remotas
    $ git branch -r
    ```
    
    Criando uma nova branch
    
    ```bash
    ## Com o comando push nós conseguimos enviar a nossa nova branch local para o ambiente remoto
    $ git push origin nome_da_branch
    ```
    
    Removendo uma branch
    
    ```bash
    ## Para remover uma branch remota usamos o push com a flag -d
    $ git push -d origin nome_da_branch
    ```
    
- Checkout
    
    O *git [checkout](https://git-scm.com/docs/git-checkout)* é o comando usado para trocar de branchs ou commits
    
    ```bash
    ## Para mudar de branch use o comando checkout
    $ git checkout nome_da_branch
    
    ## Checkout para um commit específico
    $ git checkout 653c3026778595f1f0266c37b7fcae1c1cc4614a
    
    ## Criando branch durante o checkout 
    $ git checkout -b nova_branch
    ```
    

### Mergeando branchs

Se uma branch representa uma nova linha do tempo, um *[merge](https://git-scm.com/docs/git-merge)* seria uma fusão dessas linhas temporais.

- Criando merge
    
    ```bash
    ## Criando merge entre branchs
    $ git merge care_nova_branch
    ```
    
- Cancelando merge
    
    Caso um haja um conflito durante o merge, podemos cancelar usando o comando abaixo
    
    ```bash
    $ git merge --abort
    ```
    

### Conflito?

Quando estamos trabalhando com *merges* e *branchs*, é comum acabar gerando um conflito de git. Mas afinal, o que é um conflito de git?

Um conflito, geralmente, acontece quando tentamos fazer um *merge* entre duas *branchs* diferentes, e em cada uma delas há uma alteração diferente em uma parte específica do código. Quando isso acontece, o git não sabe qual das alterações ele deve priorizar, ou até mesmo se deve manter as duas.

### Revertendo commits

O comando *[revert](https://git-scm.com/docs/git-revert)* serve para reverter alterações já realizadas em uma branch.

```bash
## Revertendo último commit
$ git revert HEAD

## Revertendo commit específico com o hash do commit
$ git revert eb27aacfdaedc8ffe0f6f829b909135304fcf732
```

### Tagueamento

As *[tags](https://git-scm.com/docs/git-tag)* é uma forma de definir marcos e versões imutáveis do seu projeto.

- Criando tag
    
    ```bash
    ## Criando uma nova tag
    $ git tag -a v1.0.0
    
    ## Criando uma nova tag com mensagem 
    $ git tag -a v1.0.0 -m "Mensagem da tag"
    
    ## Enviando tag para repositório remoto
    $ git push origin v1.0.0
    ```
    
- Removendo tag
    
    ```bash
    $ git tag -d v1.0.0
    
    ## Removendo uma tag do ambiente remoto
    $ git push -d origin v1.0.0
    ```
    

### Gitignore & Readme

Existem alguns arquivos de “configuração”, que servem ou para explorar uma funcionalidade do sistema de versionamento, ou até mesmo facilitar a documentação do próprio projeto.

- .gitignore
    
    Quando estamos falando de projetos maiores, ou até mesmo pequenos projetos que utilizam dependências ou bibliotecas de terceiros, muitas vezes não precisamos subir todos os arquivos. O arquivo “*.gitignore*” serve para configurarmos os arquivos que queremos que sejam ignorados pelo git.
    
    Os arquivos presentes no *gitignore* não serão considerados pelo sistema de versionamento. 
    
    O arquivo aceita também expressões regulares e negações para não ignorar arquivos e pastas especificadas nele.
    
    ```bash
    ## ignorando pastas inteiras
    node_modules/
    vendor/
    
    ## ignorando arquivos dentro de subpastas
    app/pasta/arquivo.js
    
    ## ignorando arquivo na raiz do projeto
    arquivo.php
    
    ## ignorando arquivos com expressões regulares
    *.lock
    
    ## não ignorando pasta ou arquivo
    !arquivo.php
    !vendor/
    ```
    
- readme.md
    
    O arquivo “*readme.md*” é um arquivo geralmente presente em repositórios com a finalidade de documentar ou informar algo sobre o projeto. Caso o projeto tenha esse arquivo, ele será mostrado na página inicial do seu repositório.
    
    O *readme* possui sua extensão “*.md*” e é escrito na linguagem de marcação chamada *[markdown](https://www.markdownguide.org/getting-started/)*, que lembra bastante o HTML.
    
- .gitkeep
    
    Já o arquivo “*.keepme*” não oficialmente reconhecido pelo Git, mas tem uma funcionalidade interessante e é bastante usado.
    
    Ele é, basicamente, um arquivo oculto sem extensão, e serve para que o git não ignore pastas vazias. Caso o usuário precise manter uma pasta, mesmo ela estando vazia, basta adicionar esse arquivo na pasta.
    

### Clonado repositórios

- SSH
    
    O clone via SSH é feito através de uma configuração mais avançada, onde é utilizado o protocolo “*[Secure Shell](https://pt.wikipedia.org/wiki/Secure_Shell)*”, que é mais seguro e mais rápido que os demais protocolos.
    
    Para ser utilizado, o SSH exige uma configuração mais complexa e a geração de uma chave local e o cadastro dela no seu GitHub.
    
    Nesse método a autenticação é feita de forma automática, sem precisar inserir email, username, senha ou token pessoal.
    
- HTTPS
    
    O clone via HTTPS utiliza do protocolo padrão da Web e é basicamente a URL do repositório com “*.git*” no final.
    
    Antes a autenticação era feita com username e senha do usuário, mas no último ano foi definido que a autenticação só pode ser feita com o username e o personal token
    
    Para gerar o seu “*Personal Token*” acesse esse link: 
    
    [https://github.com/settings/tokens](https://github.com/settings/tokens)
    
- GitHub CLI
    
    No modo *[GitHub CLI](https://cli.github.com/)*, você pode fazer  o clone utilizando a CLI(Command Line Interface) disponibilizada pelo git.