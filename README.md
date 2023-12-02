
![Participantes](https://github.com/Byotony/logospng/blob/main/PNG/Participantes%20WHITE.png)

| Antony Palacios | Gustavo Rodriguez | Cristhopher Alcivar | Diego Flores | Ian Velez | Isaac Joviric |
| ------ | ------ | ------ | ------ |  ------ | ------ |
|<p align="center"><a href="https://github.com/byotony"><img src="https://github.com/Byotony/logospng/blob/main/PNG/Byonetta.png" text-align="center" width="100" height="100"/></a></p>|<p align="center"><a href="https://github.com/gusrsl"><img src="https://github.com/Byotony/logospng/blob/main/PNG/gustavo.png" align="center" width="100" height="100"/></a></p>|<p align="center"><a href="https://github.com/krixsjdk"><img src="https://github.com/Byotony/logospng/blob/main/PNG/alcivar.png" align="center" width="100" height="100"/></a></p>|<p align="center"><a href="https://github.com/diegoflores16"><img src="https://github.com/Byotony/logospng/blob/main/PNG/diego.png" align="center" width="100" height="100"/></a></p>|<p align="center"><a href="https://github.com/e1313326363"><img src="https://github.com/Byotony/logospng/blob/main/PNG/ian.png" align="center" width="100" height="100"/></a></p>|<p align="center"><a href="https://github.com/IsaacJ95"><img src="https://github.com/Byotony/logospng/blob/main/PNG/chepo.png" align="center" width="100" height="100"/></a></p>|

# GraphQL

## Pasos de la clases
Lo primero con nuestra parte del proyecto grupal selecionaremos nuestra seccion correspondiente, en este caso historial, 
en la cual nos guiaremos con la estrctura hecha de ejemplo, adapatada a nuestra seccion quedaria de la siguiente manera:

### En la carpeta DTO aplicada a nuestra seccion quedaria de esta manera
### create_historial_m
![Alt text](img/image.png)

### index 
![Alt text](img/image-1.png)

### update-historial_m
![Alt text](img/image-2.png)


### En la carpeta entities aplicada a nuestra seccion quedaria de esta manera
### historial_m.entity
![Alt text](img/image-3.png)

### En la carpeta historial en los archivos generados por graphql aplicaremos la estructura correspondiente
### historial_m.module
Quedaria de la siguiente manera:

![Alt text](img/image-4.png)

### historial_m.resolver
Quedaria de la siguiente manera:

![Alt text](img/image-5.png)

### historial_m.service
Quedaria de la siguiente manera:
![Alt text](img/image-6.png)

### por ultimo nos conectamos con la base de Datos en Postgres
La cual cpn nuestro datos quedaria asi:
![Alt text](img/image-7.png)

## Pasos Adicionales.
Agregar una clase (entidad) adicional y un atributo que permita relacionar (Uno a Muchos) su entidad con la nueva. Adicionalmente compruebe en la consulta que el objeto vinculado es cargado de forma sistemática. (Este punto solo debe ser desarrollado y evidenciado si no logra culminar la actividad en clases)

### Para esto creamos la relacion enfermedades a historial.
![Alt text](img/image-8.png)

### En la carpeta DTO aplicada a nuestra seccion quedaria de esta manera
### create_enfermedad
![Alt text](img/image-9.png)

### update-enfermedad
![Alt text](img/image-10.png)

### En la carpeta entities aplicada a nuestra seccion quedaria de esta manera
### enfermedad.entity
![Alt text](img/image-11.png)

### En la carpeta enfermedades en los archivos generados por graphql aplicaremos la estructura correspondiente
### enfermedad.module
Quedaria de la siguiente manera:

![Alt text](img/image-12.png)

### enfermedad.resolver
Quedaria de la siguiente manera:

![Alt text](img/image-13.png)

### enfermedad.service
Quedaria de la siguiente manera:

![Alt text](img/image-14.png)


## Prueba de Funcionamiento Completo.

### Creacion de Mutuacion
![Alt text](img/image-15.png)

### Creacion de Query
![Alt text](img/image-16.png)

### Cambio de Estado
#### Primero selecionamos el id que deseamos cambiar con remove
![Alt text](img/image-17.png)

#### Despues vemos el cambio exitoso con el query
![Alt text](img/image-18.png)