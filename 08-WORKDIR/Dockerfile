FROM          docker.io/redhat/ubi10
RUN           dnf install nginx unzip -y
ADD           https://raw.githubusercontent.com/raghudevopsb90/roboshop-microservices/main/artifacts/frontend-compiled.zip /tmp/
WORKDIR       /usr/share/nginx/html
RUN           rm -rf * && unzip /tmp/frontend-compiled.zip && rm -f /tmp/frontend-compiled.zip
EXPOSE        80
ENTRYPOINT    ["nginx", "-g", "daemon off;"]
