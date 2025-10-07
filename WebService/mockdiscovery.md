---
layout: default
title: MockDiscovery
nav_order: 5
parent: WebServices
---
A classe MockDiscovery estende a classe Discovery, que contem a variável ServerLocation, que é utilizada para armazenar o ip e porta do GINGA.


| Métodos       |
|:-------------|
| [FreeTcpPort](#FreeTcpPort)| 
| [StartListener](#StartListener)| 
| [ListenerCallback](#ListenerCallback)| 


## FreeTcpPort
Esse método utiliza um listener para obter uma porta livre do dispositivo atual, uma vez que a porta é obtida, o listener é fechado e a porta é retornada.
## StartListener
Esse método constantemente monitora por novas requests https, ele é executado de forma assincrona. Quando uma request é recebida, o método ListenerCallback é utilizado para trata-la.
## ListenerCallback
Esse método é utilizado para tratar as requests recebidas pelo listener. Ele extrai da request o ip e porta do GINGA que enviou a request e salva na variavel ServerLocation. Quando esse processo termina, ela muda a variável keepRunning para false para que o listener seja parado.