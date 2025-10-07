---
layout: default
title: UserSelector
nav_order: 7
parent: WebServices
---

| Métodos       |
|:-------------|
| [SetBaseLocation](#SetBaseLocation)|
| [SetUser](#SetUser)| 
| [SendMessage](#SendMessage)| 
| [Running](#Running)| 
| [HasUsers](#HasUsers)| 
| [GetUserList](#GetUserList)| 
| [GetSelectedUser](#GetSelectedUser)|  

## SetBaseLocation
Utiliza a string recebida com a URL do GINGA para compor a URL para acessar lista de usuários.
## SetUser
Atribui o a string recebida como o nome do usuário selecionado e deixa a variavel running como false, indicando que o usuário foi selecionado.
## SendMessage
Utiliza a URL da lista de usuários para fazer uma request GET e receber a lista de usuários do GINGA.
## Running
Returna o atual estado da variavel running.
## HasUsers
Retorna se o objeto ja recebeu a UserList do GINGA.
## GetUserList
Retorna a lista de usuários recebida do GINGA.
## GetSelectedUser
Retorna o nome do usuário selecionado.