---
layout: default
title: DownloadManager
nav_order: 2
parent: WebServices
---

| Métodos       |
|:-------------|
| [SetBaseLocation](#SetBaseLocation)| 
| [SetupURL](#SetupURL)| 
| [SetupVideoURL](#SetupVideoURL)| 
| [DownloadDocument](#DownloadDocument)| 
| [DownloadImage](#DownloadImage)| 
| [DownloadAudio](#DownloadAudio)| 
| [DownloadText](#DownloadText)| 


## SetBaseLocation
Atribui a URL do ginga e o appId da cena atual para compor as URLs que serão utilizadas para fazer as requests.
## SetupURL
Faz o tratamento de uma string contendo a URL de um arquivo e a retorna com a URL completa, retornando um path local caso o arquivo já tenha sido baixado.
## SetupVideoURL
Faz o tratamento de uma string contendo a URL de um arquivo de video e a retorna com a URL completa, retornando um path local caso o arquivo já tenha sido baixado.
## DownloadDocument
Recebe um objeto GuaranaManager, uma string contendo a URL de um documento com uma cena NCL360 e faz uma request GET para baixar o documento. Caso receba o arquivo com sucesso, atribui o documento ao GuaranaManager.
## DownloadImage
Recebe uma string contendo a URL de uma imagem e um player apropiado para exibir a imagem. Faz uma request GET para baixar a imagem e atribui a imagem ao player.
## DownloadAudio
Recebe uma string contendo a URL de um arquivo de audio e um player apropiado para tocar o audio. Faz uma request GET para baixar o audio e atribui o audio ao player.
## DownloadText
Recebe uma string contendo a URL de um arquivo de texto e um player apropiado para exibir o texto. Faz uma request GET para baixar o texto e atribui o texto ao player.