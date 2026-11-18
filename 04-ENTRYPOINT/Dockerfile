FROM          docker.io/redhat/ubi10
RUN           dnf install nginx -y
# this runs as exec
ENTRYPOINT    ["nginx"]
CMD           ["-g", "daemon off;"]
