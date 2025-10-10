---
layout: default
title: Descriptor
nav_order: 2
parent: Cabeçalho
---

O elemento Descriptor é utilizado para definir caraceristicas de apresentação de uma mídia. 

Exemplo: 

```xml 
<descriptor id="d360" region="default.sky" projection="equirectangular" volume="1" dur = "268"/>
 ```
ou 
```xml 
<descriptor id="dlegenda" region="rleg1"/>
 ```

O elemento Descriptor pode receber os seguintes parâmetros ⠀

| Parâmetros   |
|:-------|
| [Id](#id)|
| [Region](#region)|
| [Dur](#dur)|
| [Volume](#volume)| 
| [SoundType](#soundtype)|
| [Projection](#projection)|


## Id
Identificador do descritor.
## Region 
Região que define a posição onde um objeto será posicionado. A indicação da região é feita indicando o identificador da região. Além do identificador das regiões definidas no próprio documento, é possível utilizar dois identificadores predefinidos. O identificador default.sky define que o objeto deverá ser exibida no ambiente como um todo (vídeo 360º). O identificador default.floor define que o objeto deverá ser apresentado no chão.
## Dur 
Duração explícita do objeto que se sobrepõe a sua duração natural.
## Volume
Volume do som. O valor desse atributo é um número entre 0 (sem som) e 1 (volume máximo).
## SoundType 
Especifica se o som deverá ou não ser espacializado, utilizando os valores 3D ou 2D, respectiva
mente. O valor padrão para esse atributo é 2D.
## Projection 
Especifica o tipo de projeção da mídia 360. Os possíveis valores para esse atributo são "equirectangular", "cylindrical-equal-area", "icosahedron", "cubemap", "adjusted-cubemap", "equiangular-cubemap" e "rotated-sphere"