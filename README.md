# Docker-Tutorial
Docker Tutorial


**2. Docker Networking Tutorial:**

Docker will proivde 3 implicit drivers when we install Docker. They are bridge,host and null drivers. please use the below command.
<br>
docker network ls -- it gives the list of network drivers.
<br>
**2.1 Network Drivers:**
      Docker’s networking subsystem is pluggable, using drivers. Several drivers exist by default, and provide core networking            functionality:

   bridge, host , overlay, macvlan, none and Network plugins.

   Network plugins: You can install and use third-party network plugins with Docker. These plugins are available from Docker Hub or from  third-party vendors


   In terms of networking, a bridge network is a Link Layer device which forwards traffic between network segments. A bridge can be a  hardware device or a software device running within a host machine’s kernel.

In terms of Docker, a bridge network uses a software bridge which allows containers connected to the same bridge network to communicate, while providing isolation from containers which are not connected to that bridge network. The Docker bridge driver automatically installs rules in the host machine so that containers on different bridge networks cannot communicate directly with each other.

**2.1.1 Bridge Network:** It's a default network. Containers are communicted via ip address where all containers created with default bridge.
<br>
**Example:** **Container c1 and c2 created with default bridge network. Both are communicated via ip address and not communicated by container name.**
<br>
docker pull alpine -- pull the alpine image
<br>
docker run -ltd --name=alpine1 alpine
<br>
docker run -ltd --name=alpine2 alpine
<br>
<br>
docker attach alpine1 -- user can enter commands once it's executed. Please use the ping command.
<br>
ping 172.2.0.3 -- it gives the response
<br>
ping alpine2 -- it returns bad address 'alpine2'
