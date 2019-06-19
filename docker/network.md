## Networking Basic Commands

#### List all Docker network commands:
_docker network -h_

#### List all Docker networks on the host:
_docker network ls_

The following command will give you the complete network ID without truncating, this ID you can get by even inspecting the docker network as well
_docker network ls --no-trunc_

### Getting detailed info on a network:
_docker network inspect [NAME]_
### Creating a network:
_docker network create br00_
### Deleting a network:
_docker network rm [NAME]_
### Remove all unused networks:
_docker network prune_

## Adding and Removing containers to a network

### Create a container with no network:
_docker container run -d --name network-test -p 8081:80 nginx_
### Create a new network:
_docker network create networktest01_
###  the container to the bridge network:
_docker network connect networktest01 network-test_
### Inspect network-test to see the networks:
_docker container inspect network-test_
### Remove network-test03 from br01:
_docker network disconnect networktest01 network-test03_

## Creating a network and defining a Subnet and Gateway









