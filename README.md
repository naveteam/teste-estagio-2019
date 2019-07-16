# Teste para vaga de estagiário

## Premissas

-   Utilizar **apenas JavaScript** puro para resolver o problema (**não é permitido o uso de jquery**).

-   Estilo fica ao critério do candidato, e não é o foco principal do teste.

-   Só será aceito o uso de bibliotecas de estilo e clientes HTTP (axios, fetch, etc).


## Desafio

O objetivo é fazer uma tela em que o usuário possa criar, excluir, e listar suas postagens.

Espera-se que o usuário possa digitar um `id` (identificador unico) de usuário e carregar os posts referente a esse `id`.

Se nada for digitado, ocorre o carregamento das postagens de todos os usuários.

## Documentação da API

**ATENÇÃO:** Como se trata de uma `fake` API, ela não mantém os dados, portanto todos os dados que vierem de retorno não vão conter os dados reais que foram enviados em requisições POST.

-   API RESTful

-   Url: `https://jsonplaceholder.typicode.com/posts`

-   Para fazer as requisições HTTP recomendamos o uso da biblioteca [axios](https://github.com/axios/axios) usando o seu link de cdn.

Exemplo de requisição:

```javascript
  axios.get('/posts/1')
  .then(function (response) {
    // handle success
    console.log(response);
  })
  .catch(function (error) {
    // handle error
    console.log(error);
  })
  .then(function () {
    // always executed
  });
```


#### Endpoints

##### Listagem de posts

GET `https://jsonplaceholder.typicode.com/posts`

##### Listagem de posts por usuário

GET `https://jsonplaceholder.typicode.com/posts?userId=${userId}`

VARIABLES

`userId` : Id do usuário que deseja listar os posts

##### Criar um post

POST `https://jsonplaceholder.typicode.com/posts`

BODY

```javascript
{
  title: 'foo',
  body: 'bar',
  userId: 1
}
```

##### Excluir um post

DELETE `https://jsonplaceholder.typicode.com/posts/${postId}`

VARIABLES

`postId` : Id do post que deseja excluir

## Observações

O que mais será levado em conta é o código JavaScript escrito no teste. Não será levado em consideração o código css. Ainda assim, esperamos uma tela com um minímo de estilo.

## Entrega

Criar um repositório com o código e mandar convite para joaopedro@nave.rs e felipe@nave.rs .
