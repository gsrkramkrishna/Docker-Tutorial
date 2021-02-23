# Docker-Tutorial
Docker Tutorial


**Docker Networking Tutorial:**

    **Network Drivers:**
Docker’s networking subsystem is pluggable, using drivers. Several drivers exist by default, and provide core networking functionality:

bridge, host , overlay, macvlan, none and Network plugins.

Network plugins: You can install and use third-party network plugins with Docker. These plugins are available from Docker Hub or from third-party vendors


In terms of networking, a bridge network is a Link Layer device which forwards traffic between network segments. A bridge can be a hardware device or a software device running within a host machine’s kernel.

There are 

In terms of Docker, a bridge network uses a software bridge which allows containers connected to the same bridge network to communicate, while providing isolation from containers which are not connected to that bridge network. The Docker bridge driver automatically installs rules in the host machine so that containers on different bridge networks cannot communicate directly with each other.
