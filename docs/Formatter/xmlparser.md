---
layout: default
title: XMLParser
nav_order: 2
parent: Formatter
---
Classe responsável por fazer o parse de um NCL360 e criar os objetos de tipo Media de acordo com o que foi definido no documento.

| Métodos       |
|:-------------|
| [Update](#parse)| 
| [SetDocument](#parsemedia)| 
| [AddAction](#parsedescriptor)| 
| [AddDelayedAction](#parseregion)| 

## Parse
Faz o parse inicial de um documento NCL360, adicionando as regions e descriptors a suas respectivas listas. Utiliza o método ParseMedia para fazer o parse de cada uma das mídias definidas.
## ParseMedia
Faz a leitura de um elemento \<media> do documento e cria um objeto do tipo Media atribuindo a ele a URL da mídia e o id. Faz também o parse do atributo descriptor e chama o método ParseDescriptor. 
## ParseDescriptor
Faz a leitura de um elemento \<descriptor> do documento, checando a existencia dos atributos soundType, volume, project e dur, que são opcionais. Caso existam, atribui os valores aos atributos do objeto Media. Em seguida, faz o parse do atributo region e chama o método ParseRegion.
## ParseRegion
Faz a leitura de um elemento \<region> do documento e atribui seus valores ao objeto Media recebido como parâmetro. Se for uma mídia que deve ser exibida no skybox, chama o método SetInSky do objeto Media para acionar a flag.

Se for outro tipo de mídia, faz o parse das coordenadas polares e azimutais, do raio e dos outros atributos que são opcionais, como largura e altura. Esses valores são atribuidos ao objeto Media recebido.