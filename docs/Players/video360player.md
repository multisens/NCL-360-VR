---
layout: default
title: Video360Player
nav_order: 7
parent: Players
---


| Métodos       |
|:-------------|
| [ConfigureProjection](#ConfigureProjection)|
| [LoadContent](#LoadContent)|
| [Prepared](#Prepared)|
| [NaturalEnd](#NaturalEnd)|
| [ConfigureSound](#ConfigureSound)|
| [StartPresentation](#StartPresentation)|
| [StopPresentation](#StopPresentation)|
| [PausePresentation](#PausePresentation)|
| [ResumePresentation](#ResumePresentation)|

## ConfigureProjection
Atribui o vídeo 360 ao player atual, adaptando-se ao tipo de projeção definido na mídia, se é equiretangular ou cubemap. 
## LoadContent
Configura o componente VideoPlayer (Unity) do player atual, atribuindo a URL do vídeo a ser exibido, com o auxilio do método SetVideoURL da classe DownloadManager, e prepara o vídeo para ser exibido carregando-o para memória.

Também configura o comportamento do vídeo quando ele terminar de ser carregado, chamando o método Prepared, e quando ele terminar de ser exibido, chamando o método NaturalEnd.

Ao final, causa uma transição de estado chamando o método Prepared para notificar que o processo de PREPARATION foi concluído.
## Prepared
Método para fazer uma transição no evento PREPARATION, indicando que ele terminou.
## NaturalEnd
Método para fazer uma transição no evento PRESENTATION, indicando que ela terminou.

## ConfigureSound
Configura o audio do vídeo 360, de acordo com seu tipo, se deve ser mono ou espacial. Configura também o seu volume.
## StartPresentation
Ativa o componente que contém o vídeo 360, inicia o playback dele e o atribui como textura do skybox da cena.
## StopPresentation
Desativa o componente que contém o vídeo 360, para que ele não seja mais visível na cena, para o seu playback e retorna o skybox da cena para o padrão.
## PausePresentation
Pausa o playback do vídeo 360.
## ResumePresentation
Retoma o playback do vídeo 360 pausado anteriormente.