---
layout: default
title: Document
nav_order: 1
parent: Documentos
---
# Document.cs


Classe que contêm todos os elementos pertencentes a uma cena.

| Métodos       |
|:-------------|
| [AddMedia](#addmedia)| 
| [SetScheduler](#setscheduler)| 
| [SetManager](#setmanager)| 
| [Running](#running)| 
| [EvalTick](#evaltick)| 
| [EvalAction](#evalaction)| 
| [EvalEventTransition](#evaleventtransition)| 


## AddMedia
Recebe um objeto do tipo Media, atribui o Document atual ao objeto Media para passar referência de onde é utilizado, e adiciona o objeto Media ao seu Dictionary utilizando seu Id como chave.

## SetScheduler
Atribui um objeto do tipo Scheduler ao Document atual.
## SetManager
Recebe um objeto do tipo GuaranaManager e o atribui a todos os objetos Media do Document atual.
## Running
Checa os estados PREPARATION e PRESENTATION de todos os objetos Media do Document atual e retorna true caso algum deles esteja como OCCURRING.
## EvalTick
Recebe um float, normalmente de um Time.deltaTime e percorre todos os objetos Media do Document atual e chama o método EvalTick de cada um deles. Isso checa por quanto tempo cada uma das mídias que está em estado OCCURRING está sendo exibida e, caso a duração da mídia tenha sido excedida, a exibição é interrompida.

## EvalAction
Recebe um id referente a um objeto Media, um evento e uma transição. Caso consiga encontrar o objeto Media com o id recebido, chama o método EvalAction da mídia, passando o evento e a transição recebidos para checar se a transição é válida e, caso seja, realiza a transição.
## EvalEventTransition
Chama um método do Scheduler para adicionar uma tupla de id de mídia, um evento e uma transição a uma lista de transições a serem formatadas como uma menssagem a ser enviada ao GINGA.




