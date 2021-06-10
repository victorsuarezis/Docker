# Docker
Is a container, for get, install, and build images of the applications, without install a complete Virtual Machine.

Docker tiene un repositorio de Imagenes: DockerHub, de donde se pueden obtener las diferentes imagenes que necesitemos.

## Docker commands:
- Show docker version: `sudo docker -v`
- Show images: `sudo docker images`
- Obtener imagenes desde el Repositorio DockerHub: `sudo docker pull <image>`. Ejemplo: `sudo docker pull postgres:9.6.6-alpine`.
- `sudo docker run -d --name <image> -p <port:port> -e <variable> <image>`. Ejemlplo: `sudo docker run -d --name postgres -p 5432:5432 -e POSTGRES_PASSWORD=postgres postgres:9.6.6-alpine`.
- Show containers running: `sudo docker ps -a`
- Starting containers: `sudo docker start container`
- Stopping containers: `sudo docker stop container`
- Acceder a contenedor:  `docker exec -u USUARIO -i -t CONTAINER ID /bin/bash # o el nombre`
- Hacer un repaldo de una BD de otro contenedor: `pg_dump -h NOMBRE_CONTEDOR -p PUERTO --no-owner -U USUARIO NOMBRE_BD > /opt/ExpDat.dmp`
- Copiar Archivos desde contenedor Docker a Host
  - `docker cp CONTAINER_ID:PATH/FILE PATH_TO`

