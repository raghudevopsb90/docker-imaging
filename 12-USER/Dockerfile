FROM          docker.io/redhat/ubi10
RUN           dnf install nginx -y
COPY          nginx.conf /etc/nginx/nginx.conf
USER          nginx
EXPOSE        8080
ENTRYPOINT    ["nginx", "-g", "daemon off;"]
