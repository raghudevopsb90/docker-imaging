FROM          docker.io/redhat/ubi10
ENV           APP_NAME=roboshop \
              APP_ENV=dev
RUN           dnf install nginx -y
WORKDIR       /usr/share/nginx/html
RUN           echo "<h1>${APP_NAME} - ${APP_ENV}</h1>" > index.html
EXPOSE        80
ENTRYPOINT    ["nginx", "-g", "daemon off;"]
