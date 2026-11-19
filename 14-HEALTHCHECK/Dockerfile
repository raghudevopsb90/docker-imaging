FROM          docker.io/redhat/ubi10
RUN           dnf install nginx -y
EXPOSE        80
HEALTHCHECK   --interval=10s --timeout=3s --retries=3 \
              CMD curl -f http://localhost1/ || exit 1
ENTRYPOINT    ["nginx", "-g", "daemon off;"]
