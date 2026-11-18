FROM          docker.io/redhat/ubi10
LABEL         maintainer="Raghu K" \
              app="roboshop-frontend" \
              org.opencontainers.image.source="https://github.com/raghudevopsb90/docker-imaging"
RUN           dnf install nginx -y
EXPOSE        80
ENTRYPOINT    ["nginx", "-g", "daemon off;"]
