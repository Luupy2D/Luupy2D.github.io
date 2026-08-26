---
layout: post
title: "Dia 01: Preparando o ambiente para testar o pygame"
date: 2026-08-25
---

O primeiro passo antes de tudo foi a instalação do Python. De acordo com o site oficial do Python (python.org) a forma mais tranquila de seguir a instalação é baixando um manager através da loja da Microsoft. Feito isso instalo a versão mais recente 3.14. O site recomenda também a utilização de venvs para organizar as dependências de módulos, o que provalvemente será objeto de um futuro post no blog.\
Agora é instalar o módulo pygame. Esse módulo é como uma camada de abstração para a funcionalidade da biblioteca SDL do C. Essa biblioteca permite que programas acessem componentes gráficos e sonoros do sistema permitindo a criação de experiências multimidia, como por exemplo: jogos. O pygame traz esta funcionalidade à linguagem Python.

Tudo ótimo até ai... mas ao tentar instalar o módulo pygame através do gerenciador de pacotes do Python (chamado pip), surge um erro cabuloso! Um tal de "subprocess-exited-with-error”... ao pesquisar na net me deparo com a curiosa situação: o pygame não oferece wheels para as versões mais recentes do Python. Esses wheels são tipo um pacote já pre-compilado pra facilitar a instalação dos módulos. Sem ele seria necessário compilar tudo manualmente, um trabalhão! Enfim, o que encontrei:\
A equipe de desenvolvimento do pygame se dividiu e duas versões são mantidas no momento: o pygame original, com número menor de desenvolvedores e o pygame-ce, uma nova versão. Sem realmente ir atrás de saber qual o melhor optei pela utilização do pygame-ce pelo simples fato de ter sido uma instalação lisa e completamente livre de erros! Já é um começo melhor...

O Visual Studio é a IDE que estarei utilizando pois já o tinha instalado no meu notebook. Apesar do VSCode ser mais que suficiente, acho que é uma ótima oportunidade para se familiarizar com esta ferramenta. Foi bem tranquilo também instalar o suporte para Python. Sendo assim, abro um novo projeto para finalmente testar o pygame. Nesta página: https://pyga.me/docs/ temos dois exemplos de código que geram uma tela básica pintada com um fundo roxo. Escolhendo o segundo exemplo, crio o arquivo pygametest.py, copio o código e executo... vejamos o resultado:

<p align="center">
  <img src="{{ 'images/pygametest.png' | relative_url }}" alt="Print de tela mostrando execução do código exemplo do pygame no Visual Studio" width="600">
  O print é de um segundo momento após leves modificações, então não está exatamente igual ao exemplo do site, mas a ideia é a mesma. Um círculo que se movimenta usando as teclas WASD do teclado.
</p>

Em um primeiro momento, é isso! Algumas outras coisas que descobri:\
  *Diretório padrão do Python no Windows (instalado pela loja da Microsoft): C:\Users\##SEU_USUARIO##\AppData\Local\Python\pythoncore-3.14-64
  *Diretório onde ficam os módulos instalados no sistema pelo pip: C:\Users\##SEU_USUARIO##\AppData\Local\Python\pythoncore-3.14-64\Lib\site-packages

Onde ##SEU_USUARIO## é a pasta com seu nome de usuário. E também, se sua versão do Python for diferente os números acompanhando o nome pythoncore- serão outros.
Obrigado por ler e até a próxima!  
