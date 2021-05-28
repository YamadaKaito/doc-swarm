Docker Image Setup
---
- build image: `docker build -t <image-name>:latest . --no-cache`
- create docker-compose-swarm.yml, only with latest image (without: container name, hostname, network, restart)



Docker Swarm Setup
---
[Master]
- `docker swarm init`
- copy entire join code

[Workers]
- `paste code`

[Master]
- check node is connected or not `docker node ls`



Deploy to Swarm
---
[Master or Workers]
- up services `docker stack deploy --compose-file <docker-compose-file> <stack-name>`
- checking services, is up or not `docker service ls` and `docker service ps <service-id>` and `<docker inspect <container-id>>`
- scale services `docker service scale <stack_name>_<service-name>=<scale-count>`
- down services `docker stack rm <stack-name>`
