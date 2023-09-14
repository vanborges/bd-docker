## Como utilizar o postgresql no laboratório

- Inicialmente precisamos remover todos os containers e images da máquina do laboratório. Isso deverá ser feito apenas no começo da disciplina.

  Para a execução de todos os containers
  ```shell
  docker stop $(docker ps -aq)
  ```
  Remove todos os containers
  ```shell
  docker rm $(docker ps -aq)
  ```
  Remove todas as imagens. Certifique-se de que você realmente deseja remover todas as imagens, pois isso pode excluir imagens que são usadas por outros projetos ou aulas.
  ```shell
  docker rmi $(docker images -aq)
  ```

- Agora precisamos subir um novo container com um servidor do postgreSQL. Para isso, iremos via terminal acessar o diretório que está o arquivo Dockerfile e executar os seguintes comandos:

  Criação da imagem postgres-server-img
  ```shell
  docker build -t postgres-server-img .
  ```
  Criar e executar um container docker a partir da imagem postgres-server-img
  ```shell
  docker run -d --name postgres-server-container -p 5432:5432 postgres-server-img
  ```
  Pronto! Agora tempos um container que podemos acessar o servidor PostgreSQL por qualquer interface cliente.

- Nosso proximo passo é abrir o pgadmin instalado em cada máquina e configurar um novo server que se conecte a esse container que acabamos de criar.
  - Abra o pgadmin
  - Register new server
    - Na aba connection coloque: localhost
    - Login: postgres
    - Senha: postgres
    - Porta: 5432
   
- Por fim, ao final da aula pare a execução do container
  ```shell
  docker stop postgres-server-container
  ```
- Sempre ao começo de cada aula, inicie novamente a execução
  ```shell
  docker start postgres-server-container
  ```