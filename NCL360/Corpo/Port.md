---
layout: default
title: Port
nav_order: 2
parent: Corpo
---

O elemento Port é utilizado para definir se uma mídia vai estar presente quando a cena começar. 

Exemplo: 

```xml 
<port component="main"/>
<port component="gualogo"/>
 ```

O elemento Port possui apenas um parâmetro ⠀

| Parâmetros   |
|:-------|
| [Component](#component)|


## Component
Identifica uma ou mais mídias que serão iniciadas quando começar a cena. O valor "main" representa o vídeo principal, mas pode ser passado o id de outros objetos de mídia.