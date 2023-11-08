---
layout: default
title: Scheduler
nav_order: 1
parent: Formatter
---

| Métodos       |
|:-------------|
| [Update](#update)| 
| [SetDocument](#setdocument)| 
| [AddAction](#addaction)| 
| [AddDelayedAction](#adddelayedaction)| 
| [AddEventTransition](#addeventtransition)| 

## Update
O método update é chamado a cada frame renderizado, ele é responsável por  monitorar e sincronizar as ações que devem ser feitas, chamando os métodos relevantes no momento correto. 

Uma das funções é chamar o método EvalTick da classe document, passando o [Time.deltaTime](https://docs.unity3d.com/ScriptReference/Time-deltaTime.html) atual. Além disso, sempre que alguma de suas listas (actions, delayedActions, eventTransitions) não estiver vazia, ele faz as chamadas necessárias para que as ações sejam executadas.
## SetDocument
Atribui um Document representando a cena que o Scheduler está controlando.
## AddAction
Recebe uma tupla de com um nodeid, representando o id de uma mídia, um EventType e um EventTransition. Essa tupla é adicionada à lista actions, que contem todas as ações que o Scheduler deve notificar outras classes, assim que possível, para que elas sejam executadas. 
## AddDelayedAction
Recebe uma tupla de com um nodeid, representando o id de uma mídia,um float representando o delay, um EventType e um EventTransition. Essa tupla é adicionada à lista delayedActions, que contem todas as ações que o Scheduler deve notificar outras classes. A diferença para o AddAction é que as ações dessa lista só devem ser executadas uma vez que o tempo definido no delay já tenha passado.

## AddEventTransition
Assim como o AddAction, recebe uma tupla de com um nodeid, representando o id de uma mídia, um EventType e um EventTransition. A tupla é adicionada à lista eventTransitions, que contem as transições que devem ser passadas ao GINGA, informando que elas aconteceram.