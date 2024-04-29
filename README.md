# TPDocker-GalvanSampieri

## Como empezar

Para poder iniciar el proyecto, seguir estos pasos:

### 1. Buildear las imagenes Docker
Primero hay que buildear las imagenes con estos dos comandos:
- docker build -t backend-image -f dockerfile-backend .
- docker build -t frontend-image -f dockerfile-frontend .

### 2. Crear la network
Despues de esto, hay que crear una network con este comando
- docker network create puente

## NO CAMBIAR NINGUNO DE LOS NOMBRES, SINO NO VA A FUNCIONAR

### 3. Hacer el compose de todo
Por ultimo hay que hacer este comando:
- docker-compose up
