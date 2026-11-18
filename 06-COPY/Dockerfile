FROM          docker.io/redhat/ubi10
RUN           dnf install nginx -y
COPY          index.html /usr/share/nginx/html/index.html
EXPOSE        80
ENTRYPOINT    ["nginx", "-g", "daemon off;"]
