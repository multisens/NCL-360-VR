---
layout: default
title: Player
nav_order: 4
parent: Players
---
Essa é uma classe abstrata que serve de base para os players de cada tipo de mídia. Alguns métodos que possuem funcionalidade igual independente do tipo da mídia são implementados aqui, enquanto outros são abstratos e são sobrescritos nas classes filhas.

Ela é um MonoBehaviour, indicando que é uma classe que pode ser atribuida a um GameObject em uma cena na Unity, e esses objetos exibirão as mídias ao usuário. Cada uma da classes filhas que herdam essa classe é responsável por exibir um tipo de mídia na cena, como imagem, vídeo, texto, etc. 

| Métodos       |
|:-------------|
| [CheckView](#CheckView)| 
| [SetMedia](#SetMedia)| 
| [SetDownloadManager](#SetDownloadManager)| 
| [SetPosition](#SetPosition)| 
| [SetSize](#SetSize)| 

## CheckView
Caso o objeto que contém o player esteja ativo na cena Unity, atribui o componente que contém o conteúdo da mídia (Renderer) a uma variavel. Se o componente estiver visível (aparecendo na camera da visão do usuário), muda a variavel inView para true e chama o método TriggerTransition da classe Media para notificar que ele esta sendo visualizado.

Caso o objeto não esteja visível, faz o processo oposto e muda a variavel para false, caso ela seja true.
## SetMedia
Atribui um objeto Media a uma variavel.
## SetDownloadManager
Atribui um objeto DownloadManager a uma variavel.
## SetPosition
Método responsável por posicionar o player no lugar correto da cena, de acordo com as coordenadas definidas na mídia. 
## SetSize
Método que define as dimensões do player de acordo com as dimensões definidas na mídia.