# Docker Swarm

## Create a cluster

### VMWare Fusion

`docker-machine create --driver vmwarefusion jessievm1`

### Virtual Box

`docker-machine create --driver virtualbox jessievm1`
`docker-machine create --driver virtualbox jessievm2`

### Initialize the swarm and add nodes

To show docker-machine IP you can run `docker-machine ls`.

`docker-machine ssh myvm1 "docker swarm init --advertise-addr <myvm1 ip>"`

as you can see, the response `docker-swarm init` contains a pre-configured `docker-swarm join`

`docker swarm join --token SWMTKN-1-25oftcyd5qkdv68jq7128k2cm9e0bnvt4dbtbz1anyk3o2q0eg-d4lza4pd03jlerqmtuvh7p1d1 192.168.99.100:2377`

**Note**: If you lost the token you can run `docker swarm join-token mager` to see the abobe command to join.

Run `docker-machine ssh myvm1 "docker node ls"` on the manager to view the nodes in this swarm.

### Left the swarm

`docker-machine ssh jessievm2 "docker swarm leave"`

### Check if the port is open

`nc -vz 192.168.244.144 2377`

### Remove service

`docker service rm {service}`
