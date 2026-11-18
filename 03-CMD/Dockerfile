FROM          docker.io/redhat/ubi10
RUN           dnf install nginx -y
CMD           ["nginx", "-g", "daemon off;"]

# CMD goes as argument to the ENTRYPOINT
# docker.io/redhat/ubi10 had entrypoint as "/bin/bash" and we provided cmd as ["nginx", "-g", "daemon off;"], So this will run as
# /bin/bash -c "nginx -g daemon off;"
