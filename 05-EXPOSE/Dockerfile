FROM          docker.io/redhat/ubi10
RUN           dnf install nginx -y
EXPOSE        80
ENTRYPOINT    ["nginx", "-g", "daemon off;"]
