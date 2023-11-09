# Use a imagem oficial do PostgreSQL como base
FROM postgres:latest

# Variáveis de ambiente para configurar o PostgreSQL
ENV POSTGRES_DB=postgres
ENV POSTGRES_USER=postgres
ENV POSTGRES_PASSWORD=postgres

# Porta em que o PostgreSQL irá ouvir (padrão é 5432)
EXPOSE 5432

## ---- comandos docker ----

### Este comando constrói uma imagem Docker usando o Dockerfile no diretório atual (.) e a marca como "postgres-server-img" usando a opção -t.
## docker build -t postgres-server-img .

### Este comando executa um container a partir da imagem criada anteriormente.
## docker run -d --name postgres-server-container -p 5432:5432 postgres-server-img

###Este comando para o container chamado "postgres-server-container".
## docker stop postgres-server-container

###Este comando inicializa o container chamado "postgres-server-container".
## docker start postgres-server-container
