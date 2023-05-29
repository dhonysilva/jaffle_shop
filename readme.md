Esse repositório é uma versão _Containerized_ do projeto Jaffle Shop.

# Jaffle Shop

O Jaffle Shop é um projeto para testes e aprendizdo do dbt.


> `jaffle_shop` is fictional eccommerce store. This dbt project transforms raw data from an app database into a customers and orders model ready for analytics.

O repositório original ser econtrado [aqui](https://github.com/dbt-labs/jaffle_shop).

A referência para a contrução do Dockerfile e docker-compose.yml desse repositório veio do post do [Giorgos Myrianthous](https://towardsdatascience.com/jaffle-shop-dbt-docker-93a9b14532a4).

# Docker

Para iniciar o conteiner execute os dois comando abaixo em seu terminal.

```
docker-compose build
````

```
docker-compose up
````

Liste todos os conteineres em operação.
```
docker ps
````

Copie o Id do container dbt.

Execute o comando abaixo para acessar o conteiner.
```
docker exec -it <container-id> /bin/bash
````

Instalar as dependências - Não é necessário nesse projeto. 
```
dbt deps
````

Build seeds
```
dbt seed --profiles-dir profiles
````

Build data models
```
dbt run --profiles-dir profiles
````

Run tests
```
dbt test --profiles-dir profiles
```
