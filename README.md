# Lab Concorrência em Golang - Leilão

<br>

## Sobre o projeto

Este é o repositório destinado ao laboratório "Concorrência com Golang - Leilão" do curso Pós Goexpert da faculdade FullCycle. O projeto permite ao usuário simular um leilão de produtos.

<br>

## Funcionalidades

- Criar um leilão.

- Buscar todos os leilões criados;

- Buscar um leilão em específico, usando seu id;

- Monitorar o status de um leilão.

<br>

## Como executar o projeto

### Pré-requisitos

Antes de começar, você vai precisar ter instalado em sua máquina as seguintes ferramentas:

- [Git](https://git-scm.com)

- [VSCode](https://code.visualstudio.com/)
  
- [Rest Client](https://marketplace.visualstudio.com/items?itemName=humao.rest-client)

- [Docker](https://www.docker.com/)

<br>

#### Acessando o repositório

```bash

# Clone este repositório

$  git  clone  https://github.com/pedrogutierresbr/lab-leilao-concorrencia-em-go.git

```

<br>

#### Executando a aplicação em ambiente dev

```bash

# Executar a aplicação

$  docker-compose  up  -d

# Parar e remover recursos da aplicação

$  docker-compose  down

```

<br>

#### Ações disponíveis

Serviços estarão disponíveis na seguinte porta:

- Web Server : 8080

```bash

# Você pode encontrar as ações no arquivo api / api.http


# Criar um leilão

POST http://localhost:8080/auction
Host:  localhost:8000
Content-Type:  application/json

{
"product_name":  "tuf gaming f15",
"category":  "computadores",
"description":  "auction computadores description",
"condition":  0
}

# Listar leilões criados

GET http://localhost:8080/auction?status=0
Host:  localhost:8000
Content-Type:  application/json

# Listar um leilão em específico (lembre-se de informar o id como param)

GET http://localhost:8080/auction/winner/:id
Host:  localhost:8000
Content-Type:  application/json

```

<br>

## Testes automatizados

```bash

# Abra um terminal

# Execute o seguinte comando

$  go  test  -v  internal/infra/database/auction/create_auction_test.go

```

<br>

## Licença

Este projeto esta sobe a licença [MIT](./LICENSE).
Feito por Pedro Gutierres [Entre em contato!](https://www.linkedin.com/in/pedrogabrielgutierres/)
