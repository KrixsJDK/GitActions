
![Participantes](https://github.com/Byotony/logospng/blob/main/PNG/Participantes%20WHITE.png)

| Antony Palacios | Gustavo Rodriguez | Cristhopher Alcivar | Diego Flores | Ian Velez | Isaac Joviric |
| ------ | ------ | ------ | ------ |  ------ | ------ |
|<p align="center"><a href="https://github.com/byotony"><img src="https://github.com/Byotony/logospng/blob/main/PNG/Byonetta.png" text-align="center" width="100" height="100"/></a></p>|<p align="center"><a href="https://github.com/gusrsl"><img src="https://github.com/Byotony/logospng/blob/main/PNG/gustavo.png" align="center" width="100" height="100"/></a></p>|<p align="center"><a href="https://github.com/krixsjdk"><img src="https://github.com/Byotony/logospng/blob/main/PNG/alcivar.png" align="center" width="100" height="100"/></a></p>|<p align="center"><a href="https://github.com/diegoflores16"><img src="https://github.com/Byotony/logospng/blob/main/PNG/diego.png" align="center" width="100" height="100"/></a></p>|<p align="center"><a href="https://github.com/e1313326363"><img src="https://github.com/Byotony/logospng/blob/main/PNG/ian.png" align="center" width="100" height="100"/></a></p>|<p align="center"><a href="https://github.com/IsaacJ95"><img src="https://github.com/Byotony/logospng/blob/main/PNG/chepo.png" align="center" width="100" height="100"/></a></p>|

# Dockerización de Aplicación NestJS y GitHub Actions

## Descripción
Este repositorio demuestra cómo Dockerizar una aplicación NestJS y configurar un flujo de trabajo en GitHub Actions para construir y desplegar contenedores de Docker.

## Pasos por seguir

### 1. Crear Repositorio

Crea un repositorio público o privado en GitHub. [Enlace al Repositorio](https://github.com/KrixsJDK/GitActions.git)
![Alt text](img/image.png)

### 2. Preparar el Código Fuente

Luego solo realizamos el commit del código a utilizar
![Alt text](img/image-1.png)

### 4. Configurar Secrets en GitHub

Crea los secrets DOCKER_USER y DOCKER_PASSWORD en la sección de Secrets de tu repositorio en GitHub.
![Alt text](img/image-2.png)
![Alt text](img/image-3.png)
![Alt text](img/image-4.png)


### 5. Configurar Token de Docker Hub

Utiliza tu usuario y clave (token) de Docker Hub para llenar los secrets DOCKER_USER y DOCKER_PASSWORD.
Crea un Token en Docker (con el nombre Github-Actions) y copia este Token generado en el secret DOCKER_PASSWORD.
![Alt text](img/image-5.png)
![Alt text](img/image-6.png)
![Alt text](img/image-7.png)
![Alt text](img/image-8.png)
![Alt text](img/image-9.png)


#### 6. Dockerizar la Aplicación

Dockeriza tu aplicación NestJS (preferiblemente un servicio REST o GraphQL sin dependencias).
![Alt text](img/image-10.png)
![Alt text](img/image-11.png)

#### 7. Verificar Construcción y Funcionamiento

Asegúrate de que la imagen puede ser compilada con el siguiente comando:
bash
docker login
docker build -t byotony/webhooks:latest .
Verifica el funcionamiento de la aplicación.
![Alt text](img/image-12.png)
![Alt text](img/image-13.png)

Tambien hacemos el push

![Alt text](img/image-14.png)

Y ya para terminar hacemos el commit para que se hagan los builds automáticamente cuando realizemos un commit nuevo al repositorio.

![Alt text](img/image-15.png)
![Alt text](img/image-16.png)

### 8. Crear Action Docker Image
Configura un flujo de trabajo en GitHub Actions para generar la imagen Docker utilizando el archivo docker-image.yml.

![Alt text](img/image-17.png)


# Evidencias

Ya tenemos el actions creado para realizar builds automáticos.
![Alt text](img/image-18.png)
![Alt text](img/image-19.png)
![Alt text](img/image-20.png)

Ahora lo progamos realizando un commit nuevo a nuestro repositorio
![Alt text](img/image-21.png)

Y cuando lo guardamos, se estará gerenando un build nuevo automáticamente.
![Alt text](img/image-22.png)

Proceso de build.
![Alt text](img/image-23.png)

Build terminado, proceso sin errores. 
![Alt text](img/image-24.png)