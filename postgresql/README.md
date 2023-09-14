### Como utilizar o postgresql no laboratório

## Inicialmente precisamos remover todos os containers e images da máquina do laboratório. Isso deverá ser feito apenas no começo da disciplina.

''''
docker stop $(docker ps -aq)
''''
''''
docker rm $(docker ps -aq)
''''
''''
docker rmi $(docker images -aq)
''''
