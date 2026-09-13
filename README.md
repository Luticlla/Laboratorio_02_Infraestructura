# Laboratorio 02
Hoy utilizaremos docker compose para poder desplegar su trabajo. Servicio web y una base de datos
## Stack
- Minimal API
- Debe retornar un mensaje incluyendo mi nombre
- Docker  
- Base de datos PostgreSQL
# Indicaciones
## Comandos
```git init``` Para iniciar el repositorio

```git add . ``` agrega todos los cambios o el archivo creado y lo pone en espera para el commit

```git commit -m "" ``` Para hacer los commits convencionales

```git remote add origin https://github.com/Luticlla/Laboratorio_02_Infraestructura.git ``` vincula mi repo local a el repositorio que publique en github

```git pust -u origin master``` Una vez hecho el o los commits lo manda al repo

```docker compose up --build``` compila el archivo **docker-compose.yaml**

```docker ps``` nos enseña los contenedores activos y algunas de sus caracteristicas como el nombre

```docker logs busy_perlman``` muestra los logs del contenedor corriendo con ese nombre o identificador

```docker exec -ti busy_perlman /bin/sh``` nos permite ejecutar comandos en el contenedor, como por ejemplo descargar nano

```docker run -d --rm -p 3001:3000 nmatsui/hello-world-api``` nos permite ejecutar el contenedor docker


## Configuración por entorno
# Creditos
- Richard Valentin Ticlla Cordova **NRC:285870**
# Evidencia
# Referencias
- Referencia de los commits convencionales 
    - https://www.conventionalcommits.org/en/v1.0.0/
    - Use este enlace para profundizar acerca del significado de los commits, por ejemplo, chore no entendia que hacia. https://dev.to/achamorro_dev/conventional-commits-que-es-y-por-que-deberias-empezar-a-utilizarlo-23an
- Referencia para los volumenes
    - https://docs.docker.com/engine/storage/volumes/
- Referencia para 

# Tipos de redes en Docker
# Tipos de volumenes en Docker

# ETC