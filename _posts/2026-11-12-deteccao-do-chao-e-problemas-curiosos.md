---
title: Detecção do chão e um problema curioso
description: ""
date: 2026-11-12T19:47:41.713Z
preview: ""
tags:
    - pygame
    - luupy2d
categories:
    - Projeto
layout: post
---
Para identificar quando o personagem está ou não no chão, criamos uma caixa de colisão logo abaixo do seu pé: se esta caixa colide com alguma superfície, o player está no chão. Pela lógica de funcionamento, irei chamar esse sistema de **sensor**.

Quando o player não está no chão, aplicamos uma força para baixo de forma constante, representando a gravidade. Para evitar que o player atravesse o chão, precisamos também zerar essa força quando o sensor encontra alguma superfície.

Isso permite implementar **o pulo**: Se o player está no chão, apertar o botão de pulo o joga para cima com força grande o suficiente para fazer o sensor não tocar mais no chão. Outra alternativa é desabilitar o sensor quando a velocidade vertical do player é negativa (ou seja, ele está sendo impulsionando para cima).

### Parado no Limbo

<p align="center">
<img src="{{ 'assets/images/deteccao1.png' | relative_url }}" 
alt="Um boneco no chão pairando no ar">
</p>

Ao testar a implementação desse sistema nos deparamos com a curiosa situação: A caixa de colisão do player (em azul) estava bem maior que o sensor (em verde), o que fazia com que, em algumas situações, o player ficasse parado como se estivesse no chão, mas o sensor acreditava que ele estava no ar! Este bug fazia o player **cair infinitamente, parado no lugar**.

A solução simples foi redimensionar o sensor, deixando-o quase do mesmo tamanho da caixa de colisão. Ainda assim fica uma dúvida importante:
- Como tratar a caixa de colisão? Se o player não for desenhado do tamanho exato permitido, a caixa será sempre maior que os gráficos visíveis, podendo causar problemas.