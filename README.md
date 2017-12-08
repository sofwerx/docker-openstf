# docker-openstf

This is the docker-compose.yml for a stand-alone OpenSTF service.

- https://github.com/openstf/stf
- https://github.com/openstf/stf/blob/master/doc/DEPLOYMENT.md

# Running:

    export IP_ADDRESS=$(ip addr show dev $(netstat -rn  | grep -e ^0.0.0.0 | awk '{print $8}') | grep 'inet ' | cut -d/ -f1 | awk '{print $2}')
    docker-compose up -d

# If installing on Ubuntu 17.10, docker will have to be installed via the following script.

    curl https://raw.githubusercontent.com/sofwerx/docker-openstf/master/ubuntu17.10-docker-install.sh |sh
