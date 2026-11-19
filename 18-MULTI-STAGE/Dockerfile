FROM          docker.io/redhat/ubi10 AS builder
RUN           curl -fsSL https://rpm.nodesource.com/setup_20.x | bash -
RUN           dnf install nodejs unzip -y
ADD           https://raw.githubusercontent.com/raghudevopsb90/roboshop-microservices/main/artifacts/frontend.zip /tmp/
WORKDIR       /app
RUN           unzip /tmp/frontend.zip
RUN           npm install && npm run build


#FROM          docker.io/redhat/ubi10
#RUN           dnf install nginx -y
#COPY          --from=builder /app/out/ /usr/share/nginx/html/
#EXPOSE        80
#ENTRYPOINT    ["nginx", "-g", "daemon off;"]
