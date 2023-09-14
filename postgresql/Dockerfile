# Use a imagem oficial do PostgreSQL como base
FROM postgres:latest

# Variáveis de ambiente para configurar o PostgreSQL
ENV POSTGRES_DB=postgres
ENV POSTGRES_USER=postgres
ENV POSTGRES_PASSWORD=postgres

# Porta em que o PostgreSQL irá ouvir (padrão é 5432)
EXPOSE 5432

## comandos docker
## docker build -t postgres-server-img .
## docker run -d --name postgres-server-container -p 5432:5432 postgres-server-img
## docker stop postgres-server-container

## apagar todos os containers da maquina
##docker stop $(docker ps -aq)
##docker rm $(docker ps -aq)

## apagar todas as imagens da maquina
#docker rmi $(docker images -aq)

