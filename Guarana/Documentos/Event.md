---
layout: default
title: Event
nav_order: 2
parent: Documentos
---
Classe representando os eventos reconhecidos durante execução de uma cena, seus estados e suas transições.

| Métodos       |
|:-------------|
| [Type](#type)| 
| [State](#state)| 
| [Transition](#transition)| 


## Type
Retorna o tipo do evento.
## State
Retorna o estado atual do evento.
## Transition
Recebe uma transição, checa se é valida a partir do estado atual do evento e, caso seja, retorna true e altera o estado atual de acordo com a transição. Caso contrário, retorna false. 
