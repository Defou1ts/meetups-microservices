# Meetups Api

🎉 Meetups microservices

## Installation:

Clone this repository and clone microservices inside root path of this repository. Write next lines:

```
$ git clone https://github.com/Defou1ts/meetups-gateway.git && cd meetups-gateway && yarn install && cd ..
$ git clone https://github.com/Defou1ts/meetups-auth-microservice.git && cd meetups-auth-microservice && yarn install && cd ..
$ git clone https://github.com/Defou1ts/meetups-microservice.git && cd meetups-microservice && yarn install && cd ..

```

Then create .env file inside root path of this repository and configure it.
Full environment denends on these variables and all microservices will use these variables for their connections. Example with simple configuration:

```
PORT=5000

RABBIT_MQ_HOST=rabbit
RABBIT_MQ_PORT=5672
RABBITMQ_DEFAULT_USER=admin
RABBITMQ_DEFAULT_PASS=admin
RABBITMQ_SERVER_ADDITIONAL_ERL_ARGS=-rabbit log_levels [{connection,error},{default,error}] disk_free_limit 2147483648

POSTGRES_HOST=postgres
POSTGRES_USER=postgres
POSTGRES_DB=meetups
POSTGRES_PASSWORD=root
POSTGRES_PORT=5432
PG_DATA=/var/lib/postgresql/data

JWT_ACCESS_TOKEN_SECRET=access-secret
JWT_ACCESS_TOKEN_EXPIRATION_TIME=900
JWT_REFRESH_TOKEN_SECRET=refresh-secret
JWT_REFRESH_TOKEN_EXPIRATION_TIME=28800

SALT=5

```

Start production or development docker-compose file with folowwing command:

```
$ docker-compose --file docker-compose.prod.yml up --build
$ docker-compose --file docker-compose.dev.yml up --build
```

Wait, first start can take few minutes.

If you used .env above, service will be available by http://localhost:5000

## Basic functionality:

- One to Many relations
- Many to Many relations
- Users role guards
- Input data validation
- HTTP correct requests and responses
- JWT authorization with access token and refresh token
- Swagger Docmentation

## Technologies stack & project structure:

- **_NestJS_**
- **_PostgreSQL_**
- **_Sequelize_**
- **_Swagger_**
- **_Eslint_**
- **_Prettier_**
- **_PassportJS_**
- **_RabbiqMQ_**
- **_Microservices_**
