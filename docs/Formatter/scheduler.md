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
## SetDocument
Atribui um Document representando a cena que o Scheduler está controlando.
## AddAction
Recebe uma tupla de com um nodeid, representando o id de uma mídia, um EventType e um EventTransition. Essa tupla é adicionada à lista actions, que contem todas as ações que o Scheduler deve notificar outras classes, assim que possível, para que elas sejam executadas. 
## AddDelayedAction
Recebe uma tupla de com um nodeid, representando o id de uma mídia,um float representando o delay, um EventType e um EventTransition. Essa tupla é adicionada à lista delayedActions, que contem todas as ações que o Scheduler deve notificar outras classes. A diferença para o AddAction é que as ações dessa lista só devem ser executadas uma vez que o tempo definido no delay já tenha passado.

## AddEventTransition
Assim como o AddAction, recebe uma tupla de com um nodeid, representando o id de uma mídia, um EventType e um EventTransition. A tupla é adicionada à lista eventTransitions, que contem as transições que devem ser passadas ao GINGA, informando que elas aconteceram.