---
title: Home
layout: home
nav_order: 1
---
Quando a aplicação é iniciada, 5 objetos ja estão em cena: *GuaranaManager*, *Scheduler*, *DownloadManager*, *UserSelector* e *WebService*.

Awake do *GuaranaManager* desativa os componentes *UserSelector* e *Scheduler* ate que eles sejam necessarios.

Start do *WebService* inicia o *MockDiscovery*, que registra uma porta disponivel do dispositivo e inicia um listener em uma thread separada. Quando o listener recebe uma request, ele registra o IP do dispositivo que fez a request e sua porta como a localização do GINGA na rede e desativa o *Discovery*.

Uma vez que o Discovery foi encerrado, o *WebService* utiliza o IP e a porta do GINGA para enviar uma request de registro para estabelecer a conexão. Se a request de conexão receber uma resposta positiva, o *WebService* inicia um *WebSocketClient*, que será responsável por enviar e receber as mensagens de comunicação com o GINGA desses ponto em diante.

Uma vez que a conexão foi estabelecida, o *GuaranaManager* ativa o *UserSelector*, fazendo uma request da lista de usuários e permitindo a seleção de um perfil de usuário, podendo ter diferentes opções de acordo com o perfil selecionado. No entanto, essa funcionalidade ainda não está implementada completamente, e um usuário padrão é selecionado automaticamente.

Nessa etapa, quando o Guaraná recebe uma mensagem do GINGA contendo um appId, indicando que são informações com a localização de uma cena, ele utiliza o *DownloadManager* para baixar o documento NCL360 que contém a definição da cena. 

Após o download bem sucedido, é iniciado o parser para o documento NCL360. O parser é responsável por iterar por cada um dos elementos definidos no documento e extrair as informações (coordenadas, dimensões, tipo, URL source, etc) das mídias, que são armazenadas em objetos do tipo *Media* e adicionadas a uma lista de um objeto *Document*, que representa a cena como um todo.

O Scheduler é então ativado. Ele é responsável por coordenar a execução das ações e transições da cena. Por exemplo, quando uma ação enviada pelo GINGA é recebida, o Scheduler registra a ação em uma lista e fará ela ser executada no momento correto, podendo ser o mais rápido possível ou após um delay definido. Ele também é responsável por notificar o GuaranaManager de transições que aconteceram, para que ele por sua vez notifique o GINGA.
