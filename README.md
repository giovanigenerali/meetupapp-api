# Rocketseat Desafio Final - Back End

[![Build Status](https://travis-ci.org/giovanigenerali/meetupapp-api.svg?branch=master)](https://travis-ci.org/giovanigenerali/meetupapp-api)

- ### Bancos de dados Postgres e Redis via Docker

  Docker - Postgres

  ```
  docker run --name postgres -p 5432:5432 -d kartoza/postgis
  ```

  Docker - Redis

  ```
  docker run --name redis -p 6379:6379 -d redis
  ```

- ### Instalar as dependencias do projeto

  ```
  npm install
  ```

- ### Configurar Postgres

  Conectar no `postgres` e criar um banco de dados chamado `meetupapp`

  - ### Executar as migrations

    ```
    adonis migration:run
    ```

  - ### Rodar o seed no database

    ```
    adonis seed
    ```

- ### Rodar a fila para envio de email

  ```
  adonis kue:listen
  ```

- ### Iniciar a aplicação

  ```
  adonis serve --dev
  ```

---

# Deploy Heroku

Rodar a fila para envio de email no Heroku

```
heroku run:detached ENV_SILENT=true node ace kue:listen -a <nome da aplicacao>
```

[Running tasks in background](https://devcenter.heroku.com/articles/one-off-dynos#running-tasks-in-background)
