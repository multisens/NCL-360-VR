---
layout: default
title: WebSocketClient
nav_order: 9
parent: WebServices
---

| Métodos       |
|:-------------|
| [ReceiveMessage](#ReceiveMessage)|
| [SendMessage](#SendMessage)|
| [Running](#Running)|
| [CloseSocket](#CloseSocket)|

## ReceiveMessage
Recebe uma string. Se a string conter "appId", indicando que é um documento com informações de uma cena, cria uma variavel do tipo ReceiveScene e envia para o GuaranaManager.
## SendMessage
Recebe um objeto que representa uma mensagem a ser enviada, transforma ela para o formato json e envia ao GINGA.
## Running
Returna o atual estado da variavel running.
## CloseSocket
Encerra a conexão com o GINGA e apaga o dispositivo atual da lista dos dispositivos conectados no GINGA.