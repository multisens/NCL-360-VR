---
layout: default
title: Link
nav_order: 3
parent: Corpo
---

O elemento Link define uma regra de sincronização para as mídias de uma cena. Ele utiliza o sub-elemento Bind para definir as regras condicionais e os gatilhos.

Exemplo: 

```xml 
<link>
    <bind component="main" interface="scene1" role="onBegin"/>
    <bind component="foto1" role="start" delay="5s"/>
</link>
 ```

O sub-elemento Bind pode receber os seguintes parâmetros ⠀

| Parâmetros   |
|:-------|
| [Component](#component)|
| [Interface](#interface)|
| [Delay](#delay)|
| [Role](#role)| 


## Component
Mídia na qual se originou e evento de gatilho.

## Interface 
Trecho da mídia no qual se originou o evento de gatilho. Se não definido é considerado que o gatilho foi originado na mídia como um todo.

## Delay 
Tempo de atraso entre o gatilho e a execução da ação.

## Role
Condição ou Ação que vai ser realizada por uma mídia. As condições e ações são pré definidas e podem ser encontradas abaixo:

| "Role" de Condição  | Descrição                                |
|-------------------|------------------------------------------|
| onBegin           | Mídia inicia sua apresentação            |
| onEnd             | Mídia encerra sua apresentação           |
| onAbort           | Mídia aborta sua apresentação            |
| onPause           | Mídia pausa sua apresentação             |
| onResume          | Mídia retoma sua apresentação            |
| onEndPreparation  | Mídia finaliza sua preparação            |
| onBeginView       | Mídia entra no campo de visão do usuário |
| onEndView         | Mídia sai do campo de visão do usuário   |

| "Role" de Ação | Descrição                             |
|-------------|---------------------------------------|
| start       | Inicia a apresentação de um mídia     |
| stop        | Encerra a apresentação de um mídia    |
| abort       | Interrompe a apresentação de um mídia |
| pause       | Pausa a apresentação de um mídia      |
| resume      | Reinicia a apresentação de um mídia   |
| prepare     | Inicia a preparação de um mídia       |