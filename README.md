# Teste para vaga de estagiário

## Instruções

- Utilizar **apenas JavaScript** puro para resolver o problema (**não é permitido o uso de jquery**);

- Tente sempre utilizar a abordagem ES6+ para resolver os exercícios;

- **Entrega:** todas as soluções devem estar em um único repositório (github, gitlab, bitbucket, etc…) de forma **pública**;

- Neste repositório deve haver, na raiz, um README.md, com as instruções de execução do código desenvolvido;

- Estilo fica ao critério do candidato, e não é o foco principal do teste;

- Só será aceito o uso de bibliotecas de estilo e clientes HTTP (axios, fetch, etc);

- Caso não consiga resolver todos os exercícios, não tem problema, envie mesmo assim.

## Desafio

### Resolver os seguintes exercícios

- **E.1** Crie uma função que recebe dois argumentos string e retorna o de maior comprimento.

- **E.2** Crie uma função que recebe três argumentos, uma função e duas string, aplique a função nas duas string e imprima o resultado.

- **E.3** Crie uma função que recebe vários argumentos do tipo string e imprime todos juntos

- **E.4** Dado a seguinte string `'teste 1 de 2 string 3'`, substitua todas as ocorrências de números pelo valor `'[removido]'`.

- **E.5** Dado o dicionário `{4: 'a', 3: 'e', 1: 'i', 5: 's'}` substitua os números na frase `'T35t3 d3 35t4g1o'` conforme o dicionário.

- **E.6** Utilizando a api da viacep (https://viacep.com.br/) e o seu cep como entrada imprima o seu endereço no formato `'ENDERECO, NUMERO, CIDADE/ESTADO'`.

**Para os seguintes exercícios** considere o array de objetos:

```
[
    {id: 1, nome: 'juca', sobrenome: 'da silva', idade: 42},
    {id: 2, nome: 'daniel', sobrenome: 'gonçalves',  idade: 21},
    {id:3, nome: 'matheus', sobrenome: 'garcia', idade: 28},
    {id: 4, nome: 'gabriel', sobrenome: 'pinheiro',  idade: 21}
]
```

- **E.7** Imprima uma mensagem de saudação com o nome completo para cada um dos objetos. O nome deve ter a primeira letra maiúscula.

```
Ex.:
Olá, Fulano de tal!
Olá, Juca da silva!
...
```

- **E.8** Imprima a soma das idades (dica: reduce)

- **E.9** Imprima se existe algum objeto menos 25 anos.

- **E.10** Imprima todos os elementos menores de 30 anos.

- **E.11** Ordene o array de forma decrescente por idade, em caso de empate o desempate é pelo id.

# Exercício de front-end

## Desafio

O objetivo é fazer uma tela em que o usuário verá uma listagem de postagens.
Cada postagem terá uma listagem com seus referentes comentários.
Um post pode ter ou não comentário, dependendo do que vier da API.

## Documentação da API

- API RESTful
- URL: https://jsonplaceholder.typicode.com/
- Para fazer as requisições HTTP recomendamos o uso da biblioteca [axios](https://github.com/axios/axios) usando o seu link de cdn.

Exemplo de requisição:

```javascript
axios
  .get("/posts")
  .then(function(response) {
    // handle success
    console.log(response);
  })
  .catch(function(error) {
    // handle error
    console.log(error);
  })
  .then(function() {
    // always executed
  });
```

## Endpoints

GET `https://jsonplaceholder.typicode.com/posts` (busca a listagem de postagens)
GET `https://jsonplaceholder.typicode.com/comments` (busca a listagem de comentários)

## Observações

O que mais será levado em conta é o código JavaScript escrito no teste. Não será levado em consideração o código css. Ainda assim, esperamos uma tela com um minímo de estilo para diferenciar o que é postagem e o que é comentário.

Dica: Para saber quais os comentários de cada postagem, é necessário fazer a comparação do `id` que vem na postagem, com o campo `postId` que vem nos comentários. Qual são iguais, significa que aquele comentário é referente aquela postagem.
