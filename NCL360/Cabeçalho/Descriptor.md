---
layout: default
title: Descriptor
nav_order: 1
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
| [Azimuthal](#azimuthal)|
| [Polar](#polar)|
| [Radius](#radius)|
| [Width e Height](#width-e-height)| 
| [zIndex](#zindex)|
| [Pin](#pin)|
| [PinType](#pintype)|


## Id
Identificador da região.
## Azimuthal 
Ângulo horizontal em relação a posição inicial do usuário para posicionamento de um objeto. O valor é definido em graus no formato xd, onde x é o valor do ângulo.
## Polar 
Ângulo vertical em relação a posição inicial do usuário para posicionamento de um objeto. O valor é definido em graus no formato xd, onde x é o valor do ângulo.
## Radius 
Distância em função da posição inicial do usuário em que um determinado objeto de mídia será apresentado. O valor é definido em metros.
## Width e Height
Largura e altura da região onde o obejto será apresentado, respectivamente. Ambos os valores são definidos em metros.
## zIndex 
Índice de sobreposição entre regiões. A região de maior índice é apresentada na frente de outras de índice menor.
## Pin 
Especifica em relação a que ponto de referência o objeto é fixado. Os valores possíveis são: environment para posicionar em relação ao ambiente como um todo, head para se mover junto com a câmera, leftHand ou rightHand para se mover junto com a mão esquerda ou direita, respectivamente. O valor padrão para esse atributo é environment.
## PinType 
Especifica se o objeto deverá ficar fixo em relação ao ângulo de rotação (rotation) ou posição (position).