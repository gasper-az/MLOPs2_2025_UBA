# Comandos de la clase

## Construir imagen de docker

docker build -t graphql-app .

## Levantar el contenedor

docker run -d --name graphql-server -p 8000:8000 graphql-app

## Para detener el servidor Docker más tarde:

docker stop graphql-server
docker rm graphql-server

# Alternativa

poetry self add poetry-plugin-export

poetry export --without-hashes --format=requirements.txt > requirements.txt 

Luego correr comandos de docker anteriores:

1. `sudo docker build -t fastapi-app .`
1. `sudo docker run -d -p 8000:8000 --name fastapi-container fastapi-app`

> Test it in `http://localhost:8000`

To delete these elements:

1. `sudo docker rm fastapi-container`
1. `sudo docker image rm fastapi-app`
