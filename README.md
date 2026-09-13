# Laboratorio 02
Hoy utilizare docker compose para poder desplegar la actividad  02 del laboratorio del curso Infraestructura como Codigo.
## Stack
- Minimal API
- Debe retornar un mensaje incluyendo mi nombre
- Docker  
- Base de datos PostgreSQL
# Indicaciones
Para el laboratorio se debe tener descargado:
- Docker Desktop
- PostgreSQL
- Visual Studio Code u otro editor de codigo
- Git
## Comandos
```git init``` Para iniciar el repositorio

```git add . ``` agrega todos los cambios o el archivo creado y lo pone en espera para el commit

```git commit -m "" ``` Para hacer los commits convencionales

```git remote add origin https://github.com/Luticlla/Laboratorio_02_Infraestructura.git ``` vincula mi repo local a el repositorio que publique en github

```git pust -u origin master``` Una vez hecho el o los commits lo manda al repo

```docker compose up --build``` compila el archivo **docker-compose.yaml**

```docker ps``` nos enseña los contenedores activos y algunas de sus caracteristicas como el nombre

```docker logs busy_perlman``` muestra los logs del contenedor corriendo con ese nombre o identificador, este comando cambia segun el nombre que se le asigna al contener, en este caso busy_perlman

```docker exec -ti busy_perlman /bin/sh``` nos permite ejecutar comandos en el contenedor, como por ejemplo descargar nano, este comando cambia segun el nombre que se le asigna al contener, en este caso busy_perlman

```docker run -d --rm -p 3001:3000 nmatsui/hello-world-api``` nos permite ejecutar el contenedor docker

## Configuración por entorno
### Ejemeplos ara el cambio de  mensajes en la API 
MESSAGE_1="mensaje_1" 

MESSAGE_2="mensaje_2" 

MESSAGE_3="mensaje_3"
### Ejemplos Para la BD PotgreSQL
USUARIOPOSTGRESQL="usuario123"

CONTRASENAPOSTGRESQL="contra123"
# Evidencia
### Inicio del repositorio y commit inicial
![alt text](<Capturas/Screenshot 2026-09-12 173853.png>)

### Se construye las 3 intancias de la API localmente
![alt text](<Capturas/Screenshot 2026-09-12 204636.png>)
### La configuracion de PostgreSQL con las instancias funciona
![alt text](<Capturas/Screenshot 2026-09-12 221308.png>)
### Captura de docker-compose
![alt text](<Capturas/Screenshot 2026-09-12 225818.png>)

# Tipos de redes en Docker
### Segun documentacion de redes de Docker hay 6 tipos de redes
- **BRIDGE:** Red por defecto si no se especifica al momento de crear una red, funciona para comunicarse entre si dentro del host 
- **HOST:** Elimina el aislamiento de red entre contenedor y la maquina host, practicamente te usa como red
- **OVERLAY:** Conecta varios dockers entre si, permitiendo que contenedores y servicios se comuniquen entre distintas maquinas 
- **IPVLAN:** Le da al usuario control sobre direccionar entre IPV4 a IPV6 
- **MACVLAN:** Se le asigna direccion MAC a un contenedor.
- **NONE:** Aisla al contenedor del host y de otros contenedores.

# Tipos de volumenes en Docker
### Segun la documentacion de volumenes de Docker hay 2 tipos
- **Nombrado:** Volumen donde la persona encargada le asigna el nombre, es facil al momento de usarse entre contenedores.
- **Anonimo:** Docker le asigna un nombre aleatorio porque no se le asigno.
# Creditos
- Richard Valentin Ticlla Cordova **NRC:285870**

# Referencias
- Referencia de los commits convencionales 
    - https://www.conventionalcommits.org/en/v1.0.0/
    - Use este enlace para profundizar acerca del significado de los commits, por ejemplo, chore no entendia que hacia. https://dev.to/achamorro_dev/conventional-commits-que-es-y-por-que-deberias-empezar-a-utilizarlo-23an
- Referencia para los volumenes en Docker
    - https://docs.docker.com/engine/storage/volumes/
- Referencia para redes en Docker
    - https://docs.docker.com/engine/network/drivers/
- Referencia de la API que se utilizo
    - https://hub.docker.com/r/nmatsui/hello-world-api  