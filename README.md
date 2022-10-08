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

Para começar vamos importar o Router no arquivo "main.js" usando os seguintes codigos:

* import VueRouter from 'vue-router';

* Vue.use(VueRouter)

Logo após que você importou o Router, crie uma nova pasta com o nome que você quiser, no meu caso vou criar uma pasta com o nome "pages"
e dentro dessa pasta crie seus arquivos, eu vou criar 2 arquivos com os nomes de "PaginaUm.vue" e "PaginaDois.vue"

*Obs: os arquivos dentro da pasta tem que ter obrigatoriamente 2 letras maiusculas assim como no exemplo acima *

Ainda no arquivo "main.js" vamos configurar o ambiente do vue, para isso crie:

const router = new VueRouter({
  modes: 'history',
  routes: [
    { path: '/', component: PaginaUm},
    { path: '/', component: PaginaUm}
  ]
})











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

--**Exemplo do metodo GET**--

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


essa função async tem como objetivo buscar e retornar os itens da lista "categoria" 

--**Exemplo do metodo POST**--

{</br>
    "descricao": "Nova categoria"</br>
}

</br>

async function adicionarCategoria(nova_categoria)</br>
    try {</br>
        const resposta = await axios.post('http://localhost:4000/categorias', {nova_categoria})</br>
        return resposta.data</br>
    } catch(error) {</br>
        console.log(error)</br>
    }</br>
}

resultado:

{"id": 4, "descricao": "Nova categoria"}



--**Exemplo do metodo PUT e PATCH**--

{</br>
    "id": 2,</br>
    "descricao": "Motocicleta"</br>
}

async function alteraCategoria(categoria) {</br>
    try {</br>
        const resposta = await axios.put(`http://localhost:4000/categorias/${categoria.id}`, {categoria})</br>
        return resposta.data</br>
    } catch(error) {</br>
        console.log(error)</br>
    }
    
   
 resultado:
 
 {"id": 2, "descricao": "Motocicleta"}
 
 
 --**Exemplo do metodo DELETE**--
 
 async function excluirCategoria(id) {</br>
    try {</br>
        const resposta = await axios.delete(`http://localhost:4000/categorias/${id}`)</br>
        return resposta.data</br>
    } catch(error) {</br>
        console.log(error)</br>
    }</br>
}

# Heroku

Caso você ainda não tenha uma conta no Heroku, seguir os seguintes passos:

* Acessar o https://www.heroku.com/</br>
* Clicar no ícone SignUp para criar uma nova conta

Estando no dashboard de acesso, você deve criar uma nova aplicação, clicando em Create new app.
[imagem]

Escolha um nome para o aplicativo. É importante ressaltar que esse nome deve ser único. Então, certifique-se que a mensagem is available apareceu logo abaixo no nome escolhido, com isso, a aplicação está criada e os recursos necessários serão alocados na plataforma do Heroku.
[imagem]

Você será redirecionado para uma tela de configuração do deploy. Caso você tenha saído do Heroku, você pode obter uma lista dos aplicativos na tela de dashboard após o login. Então, basta clicar sobre o aplicativo desejado e ter acesso às mesmas configurações.
[imagem]

Depois de conectada a aplicação com o repositório no GitHub, basta escolher a branch para monitoramento e fazer o deploy.
[imagem]

Note que, como o repositório no GitHub está integrado com a aplicação, sempre que for realizado um push para a branch escolhida, a aplicação no Heroku será atualizada.







# CRÉDITOS

https://eduardo-da-silva.github.io/aula-desenvolvimento-web/ - Eduardo da Silva
