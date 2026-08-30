---
title: Usando o Git no VSCode
description: Um breve passo a passo para ativar controle de versão no VSCode.
date: 2026-08-30T13:57:08.752Z
preview: ""
tags:
    - git
    - vscode
categories:
    - Tutorial
layout: post
---

Para poder editar localmente os arquivos que estão no *Github*  é uma boa ideia instalar o *Git*. O *VSCode* já vem com ferramentas padrões de integração, o que facilita um pouco. 
## 1. Instalar e configurar o Git

O Git pode ser baixado através [deste site](https://git-scm.com/). A instalação padrão já vem com o *Git Bash*, um terminal no estilo *Linux*. Depois de instalado, execute o *Git Bash*. Nele, precisamos digitar dois comandos para configurar quem é o usuário, ou seja, qual conta do *Github* está fazendo as alterações. Primeiro coloque seu nome do usuário:
```
git config --global user.name "Nome-de-usuario-do-github"
```
O `--global` garante que a configuração será usada em todos os projetos no computador. Agora o *e-mail*:
```
git config --global user.email "seu-email@email.com"
```
O *e-mail* é o mesmo da sua conta *Github*, assim você será creditado pelas mudanças (os *commits*).


## 2. Clonar o repositório no Github

Clonar é basicamente criar uma cópia do repositório no seu PC para editar a vontade. No navegador, acesse a página do repositório que deseja clonar. Dá pra testar com [nosso site](https://github.com/Luupy2D/Luupy2D.github.io). 

> **Importante**: *Só é possível modificar um repositório que é seu ou você tem permissões para fazer alterações. Para acessar o repositório de outra pessoa use o botão Fork. Ele cria uma "versão" pra você editar como se fosse sua.*

Clique no botão verde escrito `<> Code`. Copie a URL que aparece.

<img src="{{ 'assets/images/usandogit1.gif' | relative_url }}" alt="Copiando link do repositório">


Abra o *VSCode* (se já estava aberto, reinicie para ele perceber que o *Git* foi instalado), use o atalho `Ctrl+Shift+P` e execute o comando `Git: Clone`. Ele vai perguntar de onde é pra clonar, assim cole o endereço que foi copiado anteriormente. Depois basta escolher uma pasta do computador para copiar os arquivos. O *VSCode* vai perguntar se deseja abrir a pasta criada, clique em *Abrir*.


## 3. Usando o controle de versão
> *Em algum momento deste passo o VSCode vai pedir pra fazer login no Github, ou pedir permissão para acessar credenciais. Aceite qualquer pedido usando as credenciais da conta que foram usadas no passo 1.*

Tem um ícone no canto esquerdo do *VSCode* para acessar o Controle de Origem (*Source Control*), tem um formato de três bolinhas interligadas. Ao criar ou modificar arquivos na pasta do seu "clone", vai aparecer um numerozinho neste ícone desta forma: ![Botão source control]({{ "assets/images/usandogit2.png" | relative_url }}). Clique no ícone.

Um botão azul `Commit` permite preparar suas mudanças para enviar ao *Github*. Acima dele tem um espaço para adicionar uma mensagem explicando que mudanças foram feitas. Clicando no botão, ele vai reclamar que você não adicionou arquivos, algo assim.. clicando em *Sim/Yes* ele prepara todos os arquivos automaticamente.

Com os arquivos preparados, clique novamente no botão azul (estará escrito *Sync Changes* ou *Sincronizar*... algo do tipo) para finalmente enviar os arquivos para o repositório (depois de mais uma confirmação). Se tudo deu certo, visite o repositório pelo *Github* e as mudanças estarão lá.
