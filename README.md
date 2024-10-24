# Desafio 1 - Integração Backend Ruby e Frontend JavaScript usando Docker Compose

## Visão Geral

Este projeto demonstra a integração de uma aplicação backend escrita em Ruby com um frontend em JavaScript. O Docker Compose é utilizado para orquestrar os containers das duas aplicações, facilitando o processo de desenvolvimento e execução local.

## Estrutura do Projeto

- **Backend (Ruby on Rails)**: Responsável por fornecer as APIs REST utilizadas pelo frontend.
- **Frontend (JavaScript)**: Consome as APIs fornecidas pelo backend e exibe os dados na interface.

## Requisitos

Antes de começar, certifique-se de que você tem o seguinte instalado no seu sistema:

- **Docker** e **Docker Compose**
- **Git**

## Passos para rodar o projeto localmente

### 1. Clone o repositório

Execute o seguinte comando no terminal para clonar o repositório:

git clone <URL_DO_REPOSITORIO>

### 2. Acesse o diretório do projeto

Navegue até o diretório do projeto:

cd <nome-do-diretorio-clonado>
### 3. Inicie os containers com Docker Compose

Dentro do diretório do projeto, execute o seguinte comando para iniciar os containers:

docker-compose up --build

Este comando irá construir as imagens Docker e iniciar os containers do frontend e backend.

### 4. Acesse a aplicação

O frontend estará disponível no navegador no endereço:

http://localhost:4173

O backend estará rodando na porta 3000, mas o frontend já consome as APIs do backend automaticamente, então não é necessário acessá-lo diretamente.

### 5. Parar os containers

Quando terminar de usar a aplicação, você pode parar os containers com o seguinte comando:

docker-compose down

## Como funciona a integração

O backend (Ruby on Rails) fornece endpoints RESTful que são consumidos pelo frontend. Essas APIs são acessadas através do serviço backend, configurado no arquivo docker-compose.yml.
O frontend (React) faz chamadas HTTP para esses endpoints utilizando o nome do serviço do backend, o que é facilitado pela rede interna criada pelo Docker Compose.

## Considerações finais

Certifique-se de que as portas 4173 (frontend) e 3000 (backend) estão disponíveis no seu ambiente local.

Para verificar logs ou erros dos containers, utilize o comando:

docker-compose logs

Este projeto é uma demonstração de como realizar a integração entre um frontend em React e um backend em Ruby utilizando Docker Compose, facilitando o desenvolvimento e a comunicação entre as duas partes da aplicação.
