# devops using Dockers

## Pre-requisites
 * Docker MUST be installed.
 * Virtualbox MUST be installed.

## Create three docker machines and a swarm inside these.

 To create the swarm, we need at least two machines. One is the Leader and the others are worker.
 For the sake of this document, I will create three machines:
 * One Leader machine, and
 * Two Worker machines.

### 1. Create Machines
 Run this command on the host machine. Run three times in total, once for each machine on the host.
 I named the machines like _manager1_, _worker1_ and _worker2_.
 > "docker-machine create --driver <virtualization-software> <machine-name>"

 ![](https://github.com/umair3/devops/blob/master/docker-machine%20create%20--driver%20%3Cvitualization-software%3E%20%3Cmachine-name%3E.png?raw=true)

### 1. docker-machine ls
 ![](https://github.com/umair3/devops/blob/master/docker-machine%20ls.png?raw=true)

### 3. docker-machine ssh
 ![](https://github.com/umair3/devops/blob/master/docker-machine%20ssh%20%3Cmachine-name%3E.png?raw=true)
### 4. docker-machine stop
 ![](https://github.com/umair3/devops/blob/master/docker-machine%20stop%20%3Cmachine-name%3E.png?raw=true)
### 5. docker-machine rm
 ![](https://github.com/umair3/devops/blob/master/docker-machine%20rm%20%3Cmachine-name%3E.png?raw=true)

### 6. docker swarm init
 ![](https://github.com/umair3/devops/blob/master/docker%20swarm%20init%20--advertise-addr%20%3Cmachine-ip%3E.png?raw=true)
### 7. docker swarm join
 ![](https://github.com/umair3/devops/blob/master/docker%20swarm%20join%20--token%20%3Ctoken%3E%20%3Cip:port%3E.png?raw=true)
### 8. docker swarm leave
 ![](https://github.com/umair3/devops/blob/master/docker%20swarm%20leave.png?raw=true)

### 9. docker service create
 ![](https://github.com/umair3/devops/blob/master/docker%20service%20create%20--replicas%20%3Cint%3E%20-p%20%3Cport:port%3E%20--name%20%3Cservice-name%3E%20image.png?raw=true)
### 10. docker service ps
 ![](https://github.com/umair3/devops/blob/master/docker%20service%20ps%20%3Cservice-name%3E.png?raw=true)
### 11. docker service rm
 ![](https://github.com/umair3/devops/blob/master/docker%20service%20rm%20%3Cservice-name%3E.png?raw=true)

### 12. docker info
 ![](https://raw.githubusercontent.com/umair3/devops/master/docker%20info.png)
### 13. docker node ls
 ![](https://github.com/umair3/devops/blob/master/docker%20node%20ls%20(all%20nodes%20created).png?raw=true)
### 14. docker inspect
 ![](https://raw.githubusercontent.com/umair3/devops/master/docker%20node%20inspect%20%3Cnode-name%3E.png)

### 15. docker node update
 ![](https://github.com/umair3/devops/blob/master/docker%20node%20update%20--image%20%3Cimage:version%3E%20%3Cservice-name%3E.png?raw=true)

### 16. docker service scale
 ![](https://github.com/umair3/devops/blob/master/docker%20service%20scale%20%3Cservice-name=int%3E.png?raw=true)