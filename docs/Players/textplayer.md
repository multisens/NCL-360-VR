---
layout: default
title: TextPlayer
nav_order: 5
parent: Players
---
Essa classe herda de Player é responsável por exibir textos na cena, alguns métodos abstratos são sobrescritos mas não possuem funcionalidade pois não se aplicam a esse tipo de mídia.

| Métodos       |
|:-------------|
| [SetSize](#SetSize)| 
| [LoadContent](#LoadContent)| 
| [SetContent](#SetContent)| 
| [StartPresentation](#StartPresentation)| 
| [StopPresentation](#StopPresentation)| 

## SetSize
Método que define as dimensões do player de acordo com as dimensões definidas na mídia.
## LoadContent
Inicia um coroutine com o método DownloadText da classe DownloadManager, que faz o download do conteúdo do texto.
## SetContent
Acessa o componente TextMesh do player para atribuir o conteúdo do texto baixado para que ele seja renderizado na cena. O conteúdo da variavel text é atribuido pelo DownloadText que terá sido chamado anteriormente.

Também chama o TriggerTransition da classe Media para notificar que o processo de PREPARATION foi concluído.