---
layout: default
title: GuaranaManager
nav_order: 6
parent: Guarana
---

Objeto responsável por gerenciar a comunicação entre o GINGA e o Guarana/Unity.

| Métodos       |
|:-------------|
| [Awake](#Awake)| 
| [Update](#Update)| 
| [OnApplicationPause](#OnApplicationPause)| 
| [OnApplicationFocus](#OnApplicationFocus)| 
| [DebugMode](#DebugMode)| 
| [HasConnected](#HasConnected)| 
| [ReceivedDocument](#ReceivedDocument)| 
| [SetDocument](#SetDocument)| 
| [RemoveDocument](#RemoveDocument)| 
| [ReceiveAction](#ReceiveAction)| 
| [NotifyEventTransition](#NotifyEventTransition)| 
| [GeneratePlayer](#GeneratePlayer)| 
| [GenerateSkyPlayer](#GenerateSkyPlayer)| 


## Awake
Quando o objeto é inicializado, busca os objetos que ja estão na cena e os atribui a suas respectivas variáveis, cria as listas e deixa os objetos Scheduler e UserSelector como inativos ate que precisem ser chamados.
## Update
As seguintes condições são verificadas a cada frame:

Caso o objeto UserSelector esteja ativo mas ainda não esteja no estado running, recebe o nome do usuário selecionado e envia uma mensagem contendo esse nome para o GINGA.

Caso tenha recebido um documento, ou seja, a variável receivedScene não esteja vazia, configura o DownloadManager e inicia o download do conteúdo de forma assíncrona. Alem disso, registra os eventos reconhecidos pela cena. Ao final atribui null a receivedScene.

Caso a lista storedActionMsg não esteja vazia, cria uma lista temporária do mesmo tipo e percorre todos os elementos da lista configurando o tipo de evento de acordo com a mensagem. Se o UserSelector estiver ativo, significando que o usuário esta sendo escolhido, apenas ações do tipo PREPARATION podem ser executadas e as demais são adicionadas a lista temporária para serem tratadas no proximo frame. Se a mensagem é referente a uma ação que pode ser executada no momento, ela é transformada em uma variavel do tipo EventTransition e é passada ao Scheduler para ser executada. Ao final, a lista temporária é atribuida a storedActionMsg.


## OnApplicationPause
Caso a aplicação seja pausada, notifica o GINGA com uma mensagem de EventTransition do tipo PAUSE. Quando não estiver mais pausada, notifica o GINGA com uma mensagem de EventTransition do tipo RESUME.
## OnApplicationFocus
Caso a aplicação não seja o foco no dispositivo, notifica o GINGA com uma mensagem de EventTransition do tipo PAUSE. Quando retomar o foco, notifica o GINGA com uma mensagem de EventTransition do tipo RESUME.
## DebugMode
## HasConnected
Método chamado quando o webservice estabelece uma conexão. Atribui o WebSocketClient a sua variável assim como sua Location, desativa o webservice e ativa o UserSelector.
## ReceivedDocument
Atribui a mensagem referente a um documento a variável receivedScene.
## SetDocument
Recebe um arquivo XML contendo a descrição de uma cena, faz o parse dele e cria um objeto do tipo Document, atribui o GuaranaManager atual a esse Document, passa o Document para o Scheduler e deixa o Scheduler ativo.
## RemoveDocument
Desativa o Scheduler e deleta os objetos que estavam na cena.
## ReceiveAction
Recebe um objeto ReceiveAction representando uma ação e o adiciona a lista storedActionMsg.
## NotifyEventTransition
Se o evento for um dos aceitos pela cena, cria uma mensagem com as informações do evento e a envia para o GINGA.
## GeneratePlayer
Método responsável por instanciar novos players de mídia, utilizando o prefab correto dependendo do tipo da mídia.
## GenerateSkyPlayer
Método que instancia um vídeo 360° como skybox de uma cena.