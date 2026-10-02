---
title: Criamos o primeiro teste do projeto!
description: ""
date: 2026-10-02T00:37:07.001Z
preview: ""
tags:
    - luupy2d
categories:
    - Projeto
layout: post
---
O [link do repositório](https://github.com/Luupy2D/Luupy2D) já está disponível!

# Visão Geral
O projeto está estruturado como um pacote *pip*, desta forma o usuário pode clonar o repositório e instalar de forma (relativamente) simples. Como é uma versão de testes é recomendado criar um ambiente virtual no *Python* para separar o programa do resto do sistema: siga as instruções do arquivo README.

A interface principal é no terminal, através do comando `luupy2d`. este comando por si só não faz nada (por enquanto), mas é utilizado com três subcomandos:
- new: cria na pasta atual a estrutura de um jogo simples.
- load {demo}: copia o jogo ou demonstração contido na pasta de demos para a pasta atual.
- play: executa o jogo.

## O que temos até o momento?
#### Veja o comando *new* em ação:

<p align="center">
<img src="{{ 'assets/images/primeiroteste1.gif' | relative_url }}" 
alt="Teste com o comando new no terminal do Windows.">
</p>

Usando esse comando o usuário cria um jogo padrão, que ele pode alterar utilizando vários *assets*.

#### Veja o comando *load* em ação:

<div align="center">
<figure>
  <img src="{{ 'assets/images/primeiroteste2.gif' | relative_url }}" alt="Teste com o comando load rodando o jogo da cobrinha">
  <figcaption>Apenas uma demonstração: não quer dizer que na versão final teremos uma demo com o jogo da cobrinha.
  </figcaption>
</figure>
</div>

## O que virá pela frente?
- Comando *new*: permitir que o usuário coloque o nome de uma pasta para criar.
- Comando *load*: se o usuário apertar *tab*, oferecer uma lista das demos disponíveis.
- Jogo padrão: o arquivo do jogo *main.py* deve conter um código intuitivo que o usuário possa facilmente alterar.
- Novas *demos*!
- Novos *assets*.

Muita coisa pode mudar ao longo do desenvolvimento. Mas por enquanto é isso. Até a próxima!