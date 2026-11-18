ARG           BASE_TAG=latest
FROM          docker.io/redhat/ubi10:${BASE_TAG}
ARG           APP_VERSION=1.0
RUN           dnf install nginx -y
WORKDIR       /usr/share/nginx/html
RUN           echo "<h1>RoboShop version ${APP_VERSION}</h1>" > index.html
EXPOSE        80
ENTRYPOINT    ["nginx", "-g", "daemon off;"]
