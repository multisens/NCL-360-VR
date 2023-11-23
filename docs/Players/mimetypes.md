---
layout: default
title: MimeTypes
nav_order: 3
parent: Players
---
Classe que define os tipos de mídias reconhecidas e possui métodos para verificar o tipo de mídia de um arquivo.

| Métodos       |
|:-------------|
| [GetBaseMimeType](#GetBaseMimeType)| 
| [GetMimeType](#GetMimeType)| 
| [GetAudioType](#GetAudioType)| 

## GetBaseMimeType
Recebe uma string com um path de um arquivo, verifica a e retorna o tipo de mídia base (imagem, vídeo, texto, etc) de acordo com a extensão do arquivo.

## GetMimeType
## GetAudioType
Recebe uma string com um path de um arquivo de audio, verifica a e retorna o seu tipo (ogg ou mp3) de acordo com a extensão do arquivo. O enum utilizado (AudioType) é definido pela Unity. Caso seja outro tipo arquivo de auido não suportado, retorna o tipo "Unknown".