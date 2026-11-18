FROM          docker.io/redhat/ubi10
RUN           dnf install nginx -y
VOLUME        /var/log/nginx
EXPOSE        80
ENTRYPOINT    ["nginx", "-g", "daemon off;"]
