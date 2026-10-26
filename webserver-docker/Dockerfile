# Immagine di base
FROM nginx:alpine

# Metadati dell'immagine
LABEL maintainer="studente"
LABEL description="Webserver locale con Nginx"

# Directory di lavoro
WORKDIR /usr/share/nginx/html

# Copia la pagina HTML nel webserver
COPY html/ .

# Porta del servizio HTTP
EXPOSE 80

# Comando predefinito all'avvio del container
CMD ["nginx", "-g", "daemon off;"]
