# Docker Swarm

- [Docker and Swarm Mode – Part 1](https://lostechies.com/gabrielschenker/2016/09/05/docker-and-swarm-mode-part-1/)
- [Comparing Swarm, Swarmkit and Swarm Mode](https://sreeninet.wordpress.com/2016/07/14/comparing-swarm-swarmkit-and-swarm-mode/)

### [Networks](https://docs.docker.com/engine/swarm/networking/):

[Docker Reference Architecture: Designing Scalable, Portable Docker Container Networks](https://success.docker.com/article/Docker_Reference_Architecture-_Designing_Scalable,_Portable_Docker_Container_Networks)

A Docker swarm generates two different kinds of traffic:

 - **Control and management plane traffic:** This includes swarm management messages, such as requests to join or leave the swarm. This   traffic is always encrypted.
 - **Application data plane traffic:** This includes container traffic and traffic to and from external clients.
 
 The following three network concepts are important to swarm services:
 
 - **Overlay networks** manage communications among the Docker daemons participating in the swarm. You can create overlay networks, in the same way as user-defined networks for standalone containers.
 - **The ingress network** is a special overlay network that facilitates load balancing among a service’s nodes. 
 - **The docker_gwbridge** is a bridge network that connects the overlay networks (including the ingress network) to an individual Docker daemon’s physical network.

```
  TCP port 2377 for cluster management communications
  TCP and UDP port 7946 for communication among nodes
  UDP port 4789 for overlay network traffic
```

# CLI:

```
docker swarm promote/demote nodename
docker node update --vailability drain/pause/active nodename
```	

### Swarm Init

```
docker-machine create --driver vmwarevsphere `
     --vmwarevsphere-vcenter 192.168.9.10 `
     --vmwarevsphere-datastore Esx1-LocalDatastore `
     --vmwarevsphere-network User-Network `
     --vmwarevsphere-username=docker `
     --vmwarevsphere-password=Pa!!w0rd `
     manager1

For ($i=1; $i -le 2; $i++){
    docker-machine create --driver vmwarevsphere `
         --vmwarevsphere-vcenter 192.168.9.10 `
         --vmwarevsphere-datastore Esx1-LocalDatastore `
         --vmwarevsphere-network User-Network `
         --vmwarevsphere-username=docker `
         --vmwarevsphere-password=Pa!!w0rd `
         worker$i
}

& "C:\Program Files\Docker\Docker\Resources\bin\docker-machine.exe" env manager1 | Invoke-Expression

$manager_ip = docker-machine ip manager1
docker swarm init --advertise-addr $manager_ip 

$worker_joion_token = docker swarm join-token -q worker
For ($i=1; $i -le 2; $i++){
    $worker_ip = docker-machine ip worker$i
    docker-machine ssh worker$i "docker swarm join --token $worker_joion_token --advertise-addr $worker_ip ${manager_ip}:2377"
}

docker service create `
  --name=visualizer `
  --publish=8080:8080/tcp `
  --constraint=node.role==manager `
  --mount=type=bind,src=/var/run/docker.sock,dst=/var/run/docker.sock `
  dockersamples/visualizer

docker service create `
  --detach=false `
  --name=registry `
  --publish=2727:5000 `
  --constraint=node.role==manager `
  --mount=type=bind,src=/mnt/registry,dst=/var/lib/registry `
  registry:2
```

### Create Docker Machine on ESXi

```
docker-machine create --driver vmwarevsphere `
     --vmwarevsphere-vcenter <ip> `
     --vmwarevsphere-datastore Esx1-LocalDatastore `
     --vmwarevsphere-network User-Network `
     --vmwarevsphere-username=docker `
     --vmwarevsphere-password=**** `
     manager1
```

### Tutorials:

https://docs.docker.com/engine/swarm/stack-deploy/

https://blog.nimbleci.com/2016/09/14/docker-stacks-and-why-we-need-them/

https://docs.microsoft.com/en-us/virtualization/windowscontainers/manage-containers/swarm-mode

https://www.safaribooksonline.com/library/view/ansible-2-for/9781786465719/video1_4.html


### Swarm Playbooks

https://github.com/nextrevision/ansible-swarm-playbook

https://github.com/atosatto/ansible-dockerswarm/blob/master/tasks/swarm_cluster.yml


# Swarm vs kubernetes

https://platform9.com/blog/compare-kubernetes-vs-docker-swarm/

https://platform9.com/blog/kubernetes-docker-swarm-compared/

https://www.upcloud.com/blog/docker-swarm-vs-kubernetes/
