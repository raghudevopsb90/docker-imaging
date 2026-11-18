FROM          docker.io/redhat/ubi10
RUN           dnf install nginx -y
RUN           ls -l
RUN           uname -a

## RUN all commands at once.
RUN           dnf install nginx -y ; ls -l ; uname -a

RUN           dnf install nginx -y && ls -l && uname -a  # This is the right way, Because any command fails the it stops there only

# Run provide all commands in one shot is a preferred approach to save layers of docker
