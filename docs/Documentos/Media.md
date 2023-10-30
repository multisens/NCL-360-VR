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
## StartPreparation
## StartPresentation

## StopPresentation
## PausePresentation
## ResumePresentation