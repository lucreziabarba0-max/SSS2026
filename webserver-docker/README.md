# Webserver Docker (nginx:alpine)

Immagine Docker che parte da `nginx:alpine` e serve una pagina HTML statica.

## Build, tag e run

```bash
docker build -t webserver-docker:v1 .
docker tag webserver-docker:v1 webserver-docker:latest
docker run -d --name mio-web -p 8080:80 webserver-docker:v1
```

Pagina su http://localhost:8080

## Comandi docker CLI provati

| Comando | Cosa fa |
|---|---|
| `docker images` | elenca le immagini |
| `docker ps` / `docker ps -a` | container attivi / tutti |
| `docker logs mio-web` | log di nginx |
| `docker inspect mio-web` | dettagli JSON del container |
| `docker top mio-web` | processi nel container |
| `docker stats --no-stream` | uso di CPU e RAM |
| `docker history webserver-docker:v1` | layer dell'immagine |
| `docker exec -it mio-web sh` | shell nel container |
| `docker cp mio-web:/etc/nginx/nginx.conf .` | copia file dal container |
| `docker diff mio-web` | modifiche al filesystem |
| `docker stop / start / restart mio-web` | ciclo di vita |
| `docker pause / unpause mio-web` | sospende / riprende |
| `docker rename mio-web mio-web2` | rinomina il container |
| `docker pull alpine` | scarica un'immagine |
| `docker tag alpine alpine:prova` | aggiunge un tag |
| `docker rmi alpine:prova` | elimina un'immagine/tag |
| `docker rm -f mio-web` | elimina un container |
| `docker login` / `docker push` | accesso e push su Docker Hub |

## Docker Hub

```bash
docker run -d -p 8080:80 lucreziabarba/webserver-docker:v1
```