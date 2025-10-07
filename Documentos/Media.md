---
layout: default
title: Media
nav_order: 3
parent: Documentos
---
Classe que contêm a representação de uma mídia que poderá ser exibida em cenas.

| Métodos       |
|:-------------|
| [Running](#Running)| 
| [EvalTick](#EvalTick)| 
| [EvalAction](#EvalAction)| 
| [TriggerTransition](#TriggerTransition)| 
| [StartPreparation](#StartPreparation)| 
| [StartPresentation](#StartPresentation)| 
| [StopPresentation](#StopPresentation)| 
| [PausePresentation](#PausePresentation)| 
| [ResumePresentation](#ResumePresentation)|

## Running
Checa os estados PREPARATION e PRESENTATION da mídia e retorna true caso algum dos dois esteja como OCCURRING.
## EvalTick
Recebe um float, normalmente de um Time.deltaTime e caso a mídia atual esteja com seu estado PRESENTATION em OCCURRING, o utiliza para checar por quanto tempo a mídia está nesse estado. Ou seja, quanto tempo ela está sendo exibida e, caso a duração da mídia tenha sido excedida, a exibição é interrompida.
## EvalAction
Recebe dois objetos, um EventType e um EventTransition e checa se o evento em seu estado atual pode fazer a transição. Caso seja possível, chama o método da mídia atual referente a transição recebida, realizando a transição.
## TriggerTransition
Recebe um objeto EventType e um EventTransition. Caso o evento seja do tipo VIEW, PREPARATION ou PRESENTATION, chama o método [EvalEventTransition](https://gpmm.github.io/TestPages/Documentos/Document.html#evaleventtransition) do Document atual, passando o id da mídia atual, o evento e a transição recebidos serem adicionados a lista de mensagens a serem enviadas ao GINGA. Além disso, caso necessário, chama os métodos StartPresentation ou StopPresentation da mídia atual.
## StartPreparation
Prepara a mídia para ser exibida fazendo chamadas a métodos externos. Utiliza a source da mesma para determinar o típo de mídia representada, e cria um GameObject que é um player capaz de exibir o tipo de mídia de forma apropriada, configurando a posição em que ela deve ser exibida, incluíndo o audio caso presente, e a URL do conteúdo.
## StartPresentation
Inicializa a exibição da mídia atual caso ela ja esteja preparada. Caso contrário, deixa a variavel autostart como true, fazendo com que a mídia seja exibida assim que estiver pronta.

## StopPresentation
## PausePresentation
## ResumePresentation