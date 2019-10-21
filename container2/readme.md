# CASE STUDY - CONTAINERIZATION USING DOCKER II

## Task1
1. To run change the content dynamically in the host machine need to bind mount the folder in host machine to /var/www/html in the apache2 container.
2. To do the task i reued the container I created for CONTAINERIZATION USING DOCKER I
3. To RUN container docker run -p 5000:80 -v /home/ubuntu/mount/:/var/www/html/ -d webapp
## Task2 
1. Task2 folder containe docker compose file which runs apache on port 91 and nginx on port 92
2. To RUN cd task2 && docker-compose up
## Task3
1. Initiate docker swarm on the mastr node by --advertise-addr option.
2. docker swarm init --advertise-addr public-ip. 
3. To enable communication between the container in the different nodes all nodes need to be join in the cluster by using --advertise-addr option.
4. docker swarm join --token token master-ip:master-port --advertise-addr slaveip.
5. open all the required ports in all nodes i.e 2377/tcp,7946/tcp,7946/udp,4789/udp.
6. create an overlay network. 
7. docker network create -d overlay my-network. 
8. create a service by nginx containers in master node.
9. docker service create --replicas 3 --network my-network --name my-web nginx. 
10. The screenshot of ping out put was in task3 folder.