---
layout: default
title: Region
nav_order: 1
parent: Cabeçalho
---

O elemento Region é utilizado para definir a posição, escala e comportamento de objetos de mídia no ambiente virtual, em relação ao ponto central do vídeo 360. 

Exemplo: 

```xml 
<region id="rleg1" polar="10d" azimuthal="90d" width="4m" height="6m" radius="6m" pin="environment" zIndex="1"/> 
 ```

O elemento Region pode receber os seguintes parâmetros ⠀

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