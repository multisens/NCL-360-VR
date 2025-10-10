---
layout: default
title: Media
nav_order: 1
parent: Corpo
has_children: true
---

 O elemento Media define o conteúdo de um objeto de mídia. Ele também possui um sub elemento Area que pode separar a mídia em diferentes cenas. 

Exemplo: 

```xml 
<media id="foto1" src="media/dia.jpg" descriptor="dpic"/>
 ```
ou 
```xml 
<media id="main" src="media/video360.mp4" descriptor="d360">
        <area id="scene1" begin="30s" end="90s"/>
        <area id="scene2" begin="120s" end="180s"/>
        <area id="scene3" begin="210s" end="300s"/>
    </media>
 ```

O elemento Media deve receber os seguintes parâmetros ⠀

| Parâmetros   |
|:-------|
| [Id](#id)|
| [Src](#src)|
| [Descriptor](#descriptor)|


## Id 
Identificador da mídia.
## Src 
URL com a localização do objeto de mídia a ser apresentado. A URL poderá ser local ou remota. No segundo caso o Guaraná irá baixar a mídia antes de executar ela. Quando não definido um valor para o Src, considera-se que a mídia não define um conteúdo a ser apresentado pela aplicação.
## Descriptor 
Descritor que define as características de exibição da mídia. O valor é o identificador do descritor a ser utilizado.