# Docker

- [Docker in Production: A History of Failure](https://thehftguy.com/2016/11/01/docker-in-production-an-history-of-failure/)

# Storage

- [DOCKER : STORAGE PATTERNS FOR PERSISTENCE](https://kvaes.wordpress.com/2016/02/11/docker-storage-patterns-for-persistence/)

# Tools

- [Portworx](https://portworx.com/) - The Solution for Stateful Containers in Production. Designed for DevOps.
- [REX-Ray](https://rexray.thecodeteam.com) - the leading container storage orchestration engine enabling persistence for cloud native workloads
- [Sysdig](https://www.sysdig.org/install/) - 
- [Docker-Sync](http://docker-sync.io/)

# Service Discovery

- [Docker Service Registration and Discovery](https://www.slideshare.net/m_richardson/docker-service-registration-and-discovery?next_slideshow=1)
- [Docker cluster with swarm, consul, registrator and consul-template](https://www.slideshare.net/JulienMaitrehenry/swarm-49613398)

# Docker Terms:

1. Docker Machine
2. Docker Engine
3. Docker Swarm
4. Docker Compose
5. Docker Daemon
6. Docker CLI
7. Docker Stack

# Docker Swam:

1. Cluster
2. Node
3. Manager/Worker
4. Service
5. SwamKit
6. Routing Mesh
7. Raft Consensus Algorithm
8. Service Discovery
9. Load Balancing
 
### [Docker Registry](https://docs.docker.com/registry/):

Create or modify `/etc/docker/daemon.json`

	{ "insecure-registries":["<local-registry-ip>:5000"] }
	
Restart docker daemon

	sudo service docker restart

```
docker service create `
  --detach=false `
  --name=registry `
  --publish=2727:5000 `
  --constraint=node.role==manager `
  --mount=type=bind,src=/mnt/registry,dst=/var/lib/registry `
  registry:2
```

# Docker Host

https://www.safaribooksonline.com/library/view/docker-compose-in/100000006A0437/000601.html

https://www.safaribooksonline.com/library/view/restful-web-services/9781788294638/video4_7.html

https://www.safaribooksonline.com/library/view/event-driven-microservices/9781491944165/video239923.html

https://docs.microsoft.com/en-us/vsts/build-release/concepts/definitions/build/variables?tabs=powershell

https://blogs.msdn.microsoft.com/jcorioland/2016/08/19/build-push-and-run-docker-images-with-visual-studio-team-services/

https://github.com/Microsoft/VSTS-Docker-Preview

https://marketplace.visualstudio.com/items?itemName=ms-vscs-rm.docker
