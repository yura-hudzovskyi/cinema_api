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

## Set environment variables 
#### Create .env file in the root directory (you can use .env.example as a template)
```
POSTGRES_HOST=db
POSTGRES_USER=postgres
POSTGRES_PASSWORD=secret
POSTGRES_NAME=postgres
SECRET_KEY=dajngosecretkey
```
You can generate a secret key in [this](https://djecrety.ir/) service.

### Clone the repository
```sh
$ git clone git@github.com:yura-hudzovskyi/cinema_api.git
$ cd cinema_api
```

## Local installation
```sh
$ python3 -m venv venv
$ source venv/bin/activate # for Linux
$ venv\Scripts\activate # for Windows
$ pip install -r requirements.txt
$ python manage.py migrate
$ python manage.py runserver
```

## Installation with docker-compose
- Make sure you have docker and docker-compose installed
- Run the following commands
```sh
$ docker-compose up --build
```

## To access the API pages you can use the following steps:
- Register a new user [http://127.0.0.1:8000/api/user/register/](http://127.0.0.1:8000/api/user/register/)
- Get a token [http://127.0.0.1:8000/api/user/token/](http://127.0.0.1:8000/api/user/token/)
- Use the token to access the API (ModHeader extension can be used for this)
## API Documentation
1. Swagger
```
http://127.0.0.1:8000/api/doc/swagger/
```
2. Redoc
```
http://127.0.0.1:8000/api/doc/redoc/
```