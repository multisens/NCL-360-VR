---
layout: default
title: Video2DPlayer
nav_order: 6
parent: Players
---

Essa classe herda de Player é responsável por exibir videos 2D na cena.

| Métodos       |
|:-------------|
| [LoadContent](#LoadContent)|
| [Prepared](#Prepared)|
| [NaturalEnd](#NaturalEnd)|
| [ConfigureSound](#ConfigureSound)|
| [StartPresentation](#StartPresentation)|
| [StopPresentation](#StopPresentation)|
| [PausePresentation](#PausePresentation)|
| [ResumePresentation](#ResumePresentation)|


## LoadContent
Faz o setup de um objeto RenderTexture(objeto unity que contem uma textura renderizada em tempo real), atribui essa textura ao componente Renderer do player e utiliza o método SetuVideoURL da classe DownloadManager para atribuir a URL do vídeo a ser exibido.

Também configura o comportamento do vídeo quando ele terminar de ser carregado, chamando o método Prepared, e quando ele terminar de ser exibido, chamando o método NaturalEnd.

Ao final, causa uma transição de estado chamando o método Prepared para notificar que o processo de PREPARATION foi concluído.
## Prepared
Método para fazer uma transição no evento PREPARATION, indicando que ele terminou.
## NaturalEnd
Método para fazer uma transição no evento PRESENTATION, indicando que ela terminou.
## ConfigureSound
Configura o audio do vídeo 2D, de acordo com seu tipo, se deve ser mono ou espacial. Configura também o seu volume.
## StartPresentation
Ativa o componente que contém o vídeo 2D e inicia o playback dele.
## StopPresentation
Desativa o componente que contém o vídeo 2D, para que ele não seja mais visível na cena, e para o seu playback.
## PausePresentation
Pausa o playback do vídeo 2D.
## ResumePresentation
Retoma o playback do vídeo 2D pausado anteriormente.