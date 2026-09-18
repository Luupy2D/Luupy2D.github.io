---
title: Criação do site do projeto através do Github Pages
description: ""
date: 2026-09-18T19:35:50.082Z
preview: ""
tags:
    - site
categories:
    - Projeto
layout: post
slug: criacao-do-site
---
*Neste post explicarei como foi o processo de montar o site. Veremos também como funciona para rodar o site no computador para fazer alterações locais.*

# 1. Criando o repositório do site no Github
Pra hostear um site com sua conta no github é preciso criar um repositório com um nome nesse formato:
```
##NOME_DE_USUARIO##.github.io
```
Substitua *##NOME_DE_USUARIO##* pelo seu nome no github. No nosso exemplo o nome do repositório ficou `Luupy2D.github.io`.

> Acho que deve ter como criar a página com a url diferente do nome de usuário, mas ficarei devendo a explicação!

Ok. Com o repositório criado vamos clonar ele para editar no VSCode. Pode clonar ele mesmo estando vazio no momento! O processo de como clonar está explicado [neste post]({% post_url 2026-08-29-usando-o-git-no-vscode %}). Para adicionar o esqueleto do site, vamos instalar o *Jekyll*.

<br>

# 2. Instalando Jekyll para rodar o site localmente
O *jekyll* é uma aplicação construída na linguagem *Ruby* então antes de tudo temos que instalar o *Ruby*.

### Baixando e instalando o Ruby com DevKit
Baixe a versão do *Ruby+Devkit* [nesta página](https://rubyinstaller.org/downloads/archives), porém **FIQUE LIGADO**: é de ***extrema importância que você baixe a versão 3.1 ou inferior!!!!!!*** Fui vítima da ideia de achar que baixando a versão mais recente daria certo, pois não deu! O *Jekyll* dá vários erros causados por incompatibilidade com as novas versões, daí tive que desinstalar a versão 4.0, baixar e instalar tudo de novo.. cuidado!!

> A versão que estou usando sem erros é a 3.1.6-1 (`rubyinstaller-devkit-3.1.6-1-x64`) olha ai o link direto pra já baixar esta versão: [Baixar](https://github.com/oneclick/rubyinstaller2/releases/download/RubyInstaller-3.1.6-1/rubyinstaller-devkit-3.1.6-1-x64.exe).

Ok. Baixado, rode o instalador, dê o bom e velho next,next...install. Vai aparecer um *prompt* de comando pra instalar mais algumas coisas, aceite a instalação digitando *S* ou *Y*.

Pra ter certeza que deu certo, abra qualquer *prompt* de comando e digite `ruby -v`. Se aparecer a versão do *Ruby*, deu certo (***Não esqueça do aviso sobre a versão!! Tem que ser 3.1 ou menor!!!!***).
 
### Instalando e inicializando o site via Jekyll
Em um *prompt* de comando digite `gem install jekyll`. Os *gems* são os pacotes do *Ruby*, seria algo próximo do *pip* no *Python*.

Terminada a instalação, abra a pasta do seu site no VSCode. Abra um terminal no próprio VSCode, assim ele já estará na pasta certa. Execute este comando:
```
jekyll new --skip-bundle
```

Um monte de arquivos aparecerão na pasta! Abra o arquivo *Gemfile* criado: este arquivo gerencia as dependências do site. 
1. Comente a linha que começa com `gem jekyll` **colocando** um jogo da velha "#" no inicio da linha.
2. **Descomente** a linha que começa com `gem github-pages`, **retirando** o jogo da velha no início. 

Feito isto, pode salvar e fechar o *Gemfile*.

Voltando ao terminal execute este comando: `bundle add webrick`. Agora finalizamos executando:
```
bundle install
```
Que vai instalar as dependências do site.

### Rodando o site localmente
Para rodar o *Jekyll*, execute este comando no terminal (de preferência do VSCode):
```
bundle exec jekyll serve
```

Hora da verdade... se a configuração nos passos anteriores deu certo, depois de carregar ele vai deixar o processo rodando com a mensagem `>Server running... press ctrl-c to stop.`. Agora para acessar o site, vá em qualquer navegador e na barra da url coloque: `localhost:4000`. O site *default* deve aparecer!

<figure style="text-align: center;">
  <img src="{{ 'assets/images/criacao-site1.png' | relative_url }}" alt="Print de tela com o site rodando em localhost" width="600">
  <figcaption>A primeira versão do site rodando localmente.
  </figcaption>
</figure>

> Caso houve algum erro, ou alguma coisa não deu certo, veja estas páginas - elas me ajudaram bastante no processo: [Criando um site de páginas GitHub com Jekyll](https://docs.github.com/pt/pages/setting-up-a-github-pages-site-with-jekyll/creating-a-github-pages-site-with-jekyll) - [Testando seu site de páginas GitHub localmente com o Jekyll](https://docs.github.com/pt/pages/setting-up-a-github-pages-site-with-jekyll/testing-your-github-pages-site-locally-with-jekyll)

<br>

# 3. Outras coisas
- As páginas do site tem extensão *.md* ou *.markdown* - é possível também inserir HTML nestes arquivos sem nenhum problema.
- Existe uma extensão no VSCode chamada **Front Matter CMS** que se integra com o site para permitir a edição de posts do blog diretamente no VSCode. *Recomendo!*
- O arquivo `_config.yml` cuida das configurações gerais do site.
- Coloque em seu arquivo `.gitignore` os nomes de outros arquivos pra eles não serão enviados ao repositório quando for feito *commit*. É recomendado adicionar o `Gemfile.lock`.