---
layout: default
title: Image2DPlayer
nav_order: 2
parent: Players
---

| Métodos       |
|:-------------|
| [LoadContent](#LoadContent)|
| [SetContent](#SetContent)|
| [StartPresentation](#StartPresentation)|
| [StopPresentation](#StopPresentation)|



## LoadContent
Inicia um coroutine com o método DownloadImage da classe DownloadManager, que faz o download da imagem encontrada na URL source passada para o método.

## SetContent
Atribui a imagem baixada como a textura do componente Renderer do player, para que ela seja exibida para o usuário na cena. Também chama o TriggerTransition da classe Media para notificar que o processo de PREPARATION foi concluído.
## StartPresentation
Deixa o componente que contém a imagem do player como ativo, para que seja visível na cena.
## StopPresentation
Deixa o componente que contém a imagem do player como desativado, para que não seja mais visível na cena.