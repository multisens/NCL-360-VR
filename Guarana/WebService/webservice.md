---
layout: default
title: WebService
nav_order: 8
parent: WebServices
---

| Métodos       |
|:-------------|
| [Start](#Start)| 
| [Update](#Update)| 


## Start
Quando um objeto desse tipo é instanciado, atribui o GuaranaManager pai, na hierarquia da Unity, a ele.
## Update
Se possuir um Discovery atribuido e ele não estiver mais rodando, pega a URL do GINGA a partir do Discovery e atribui null novamente a ele. Em seguida instancia um objeto do tipo Register, que é responsável por enviar uma mensagem ao GINGA para estabelecer a conexão.

Caso possua um Register atribuido e ele não estiver mais rodando, atribui null a ele após receber sua URL. Utiliza a URL do GINGA com a qual a conexão foi estabelecida e instancia um objeto do tipo WebSocketClient, que é responsável por enviar e receber mensagens do GINGA.

Uma vez que a conexão foi estabelecida e o WebSocketClient está rodando, utiliza o método HasConnected para notificar o GuaranaManager que a conexão foi estabelecida, fazendo com que o WebService seja desativado e o UserSelector seja ativado.