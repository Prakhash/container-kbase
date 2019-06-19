Networking Basic Commands
List all Docker network commands:
docker network -h
List all Docker networks on the host:
docker network ls
The following command will give you the complete network ID without truncating, this ID you can get by even inspecting the docker network 

docker network ls --no-trunc
Getting detailed info on a network:
docker network inspect [NAME]
Creating a network:
docker network create br00
Deleting a network:
docker network rm [NAME]
Remove all unused networks:
docker network prune

Adding and Removing containers to a network
Create a container with no network:
docker container run -d --name network-test03 -p 8081:80 nginx
Create a new network:
docker network create br01
Add the container to the bridge network:
docker network connect br01 network-test03
Inspect network-test03 to see the networks:
docker container inspect network-test03
Remove network-test03 from br01:
docker network disconnect br01 network-test03

Creating a network and defining a Subnet and Gateway









