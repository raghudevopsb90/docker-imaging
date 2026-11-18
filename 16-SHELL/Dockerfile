FROM          docker.io/redhat/ubi10
SHELL         ["/bin/bash", "-o", "pipefail", "-c"]
RUN           dnf install nginx -y
WORKDIR       /usr/share/nginx/html
RUN           curl -fsSL https://raw.githubusercontent.com/raghudevopsb90/roboshop-microservices/main/00-overview.md | sed 's/raghudevopsb89/raghudevopsb90/g' > overview.txt
EXPOSE        80
ENTRYPOINT    ["nginx", "-g", "daemon off;"]
