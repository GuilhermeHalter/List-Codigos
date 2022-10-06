# Vue.Js
A mas Guilherme o que é o Vue.js? - você me pergunta.</br>

O Vue.js nada mais é do que um framework (um conjunto de códigos genéricos que permite o desenvolvimento de sistemas e aplicações) progressivo para a construção de interfaces de usuário.

# Introdução

<p align="center">Assuntos</p>

<p align="center">
  <a href="#router">Router</a> |
  <a href="#pinia">Pinia</a> |
  <a href="#api">API</a> |
  <a href="#axios">Axios</a> |
  <a href="#heroku">Heroku</a>
</p>

# Router



# Pinia



# API


# Axios

o que é o Axios?</br>
Axios é um cliente HTTP tanto para uso no node.js quanto em um navegador.

* Primeiramente você precisa instalar a biblioteca Axios:

npm install axios

* para importar o Axios em seus arquivos usamos:

import axios from 'axios'

sempre que importarmos o Axios usaremos uma função async.

* Verbos REST

Os principais verbos rest são os 

GET	| Busca um recurso</br>
POST	| Cria um recurso</br>
PUT	| Atualiza um recurso</br>
PATCH	| Atualiza parcialmente um recurso</br>

**Exemplo do metodo GET**

"categorias": [</br>
    {"id": 1, "descricao": "Carros"},</br>
    {"id": 2, "descricao": "Motos"},</br>
    {"id": 3, "descricao": "Caminhões"},</br>
]


async function buscarTodasAsCategorias() {</br>
    try {</br>
        const resposta = await axios.get('http://localhost:4000/categorias')</br>
        return resposta.data
    } catch(error) {</br>
        console.log(error)
    }</br>
}


essa função async tem como buscar os itens da lista "categoria" e mostralos na tela 




# Heroku




# SITE DO SOR EDUARDO

https://eduardo-da-silva.github.io/aula-desenvolvimento-web/
