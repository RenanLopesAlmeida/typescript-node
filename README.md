# Sobre o desafio do bootcamp da Rocketseat :rocket: 

Repositório do desafio de criar uma aplicação para continuar treinando o que venho aprendendo até agora no Node.js junto ao TypeScript, utilizando o conceito de models, repositories e services para isolar a regra de negócio da aplicação!

Essa será uma aplicação para armazenar transações financeiras de entrada e saída, que deve permitir o cadastro e a listagem dessas transações.


## Configuração :gear:

Assim que clonar o projeto, instale as dependências com o comando **yarn** no seu terminal
Para rodar a aplicação, basta dar um **yarn dev:server** no seu terminal

## Rotas :fire:

**endpoint do tipo post: http://localhost:3333/transactions**
A rota deve receber title, value e type dentro do corpo da requisição, sendo type o tipo da transação, que deve ser income para entradas (depósitos) e outcome para saídas (retiradas). Ao cadastrar uma nova transação, ela deve ser armazenada dentro de um objeto com o seguinte formato :


corpo da requisição
```
  {
    "title": "salario",
    "value": 4500,
    "type": "income"
  }

```
 **endpoint do tipo get: http://localhost:3333/transactions**
 
 Essa rota retorna uma listagem com todas as transações que você cadastrou até agora, junto com o valor de soma de entradas, retiradas e total de crédito. Essa rota retorna um objeto com o formato a seguir:
 
 ```
  {
  "transactions": [
    {
      "id": "uuid",
      "title": "Salário",
      "value": 4000,
      "type": "income"
    },
    {
      "id": "uuid",
      "title": "Freela",
      "value": 2000,
      "type": "income"
    },
    {
      "id": "uuid",
      "title": "Pagamento da fatura",
      "value": 4000,
      "type": "outcome"
    },
    {
      "id": "uuid",
      "title": "Cadeira Gamer",
      "value": 1200,
      "type": "outcome"
    }
  ],
  "balance": {
    "income": 6000,
    "outcome": 5200,
    "total": 800
  }
}

```

## Testes :sparkles:

Para rodar os testes, basta executar no terminal **yarn test**
