# DRF Cinema API
This is a simple API for a cinema. It allows you to create movies, cinemas, showtimes and bookings. It also allows you to list all movies, cinemas, showtimes and bookings.

## Features
- JWT authentication
- Create cinema halls, movies with actors and genres, movie sessions
- Filter movies by genre, actor, movie session
- Manage your tickets
- access to the admin panel
- access to the API documentation (Swagger)
- access to the API documentation (Redoc)

## Installation
#### Clone the repository
```sh
$ git clone git@github.com:yura-hudzovskyi/cinema_api.git
$ cd cinema_api
```

#### Run with docker-compose
!! Docker and docker-compose must be installed !!
1. Set environment variables in .env file. You can use .env.sample as an example.
```
POSTGRES_HOST=db
POSTGRES_USER=postgres
POSTGRES_PASSWORD=secret
POSTGRES_DB=postgres
POSTGRES_NAME=postgres
```
2. Run docker-compose
```sh
$ docker-compose up
```
Check the API at http://127.0.0.1:8000

## To get started with the API
1. If you want to use the admin panel, create a superuser
```sh
$ docker-compose run app "python manage.py createsuperuser"
```
2. If you want to use the API, create a user
```
http://127.0.0.1:8000/api/user/register/
```
After that, you can get a token for the user. Enter email and password, and save the token.
```
http://127.0.0.1:8000/api/user/token/
```

## API Documentation
1. Swagger
```
http://127.0.0.1:8000/api/doc/swagger/
```
2. Redoc
```
http://127.0.0.1:8000/api/doc/redoc/
```