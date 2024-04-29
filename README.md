# TPDocker-GalvanSampieri

Para poder iniciar el proyecto, primero hay que buildear las imagenes con estos dos comandos:
docker build -t backend-image -f dockerfile-backend .
docker build -t frontend-image -f dockerfile-frontend .

Despues de esto, hay que crear una network con este comando
docker network create puente

NO CAMBIAR NINGUNO DE LOS NOMBRES, SINO NO VA A FUNCIONAR

Por ultimo hay que hacer este comando:
docker-compose up
