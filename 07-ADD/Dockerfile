FROM          docker.io/redhat/ubi10
RUN           dnf install nginx -y
ADD           site.tar.gz /usr/share/nginx/html/
ADD           https://raw.githubusercontent.com/raghudevopsb90/roboshop-microservices/main/artifacts/frontend-compiled.zip /tmp/
EXPOSE        80
ENTRYPOINT    ["nginx", "-g", "daemon off;"]
