FROM          docker.io/redhat/ubi10
RUN           dnf install nginx -y
WORKDIR       /usr/share/nginx/html
ONBUILD COPY  . .
EXPOSE        80
ENTRYPOINT    ["nginx", "-g", "daemon off;"]
