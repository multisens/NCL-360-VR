---
layout: default
title: Area
nav_order: 1
parent: Media
---

 O elemento Area é usado para definir um pedac¸o de uma mídia de áudio ou vídeo. Seu uso principal é permitir que sejam sincronizados diferentes objetos com trechos de um vídeo ou áudio.

Exemplo: 

```xml 
<media id="main" src="media/video360.mp4" descriptor="d360">
        <area id="scene1" begin="30s" end="90s"/>
        <area id="scene2" begin="120s" end="180s"/>
        <area id="scene3" begin="210s" end="300s"/>
    </media>
 ```

O elemento Area deve receber os seguintes parâmetros ⠀

| Parâmetros   |
|:-------|
| [Id](#id)|
| [Begin](#begin)|
| [End](#end)|


## Id 
Identificador da Area.
## Begin 
Tempo de início do trecho. Esse tempo é definido em segundos, podendo ser fracionado, em relação ao início da mídia.
## End 
Tempo de fim do trecho. Esse tempo é definido em segundos, podendo ser fracionado, em relação ao início da mídia.
