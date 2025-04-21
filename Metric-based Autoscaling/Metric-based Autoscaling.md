# What is VCN ? What are the parts involved in it?
Ans. A Virtual Cloud Network ( VCN ) is a private, isolated virtual network which allows you to launch your resources in a secure, customizable network environment.
A VCN resides in a single OCI Region.

> **Subnet :** A subnet is simply a subdivision in a VCN Where you place your resources. You can set a subnet to exist it either in a single Availability Domain or in entire region.

> **Public Subnet :** Instances have public IPs and can access internet.

> **Private Subnet :** Instances donot have public IPs , generally more secure.

> **Route Tables :** Defines how the traffic should be directed within the VCN or outside of it. Each subnet associated with one route table.

>  **Internet Gateway :** Provides the public internet access to the resources in the public subnet

>  **NAT Gateway  :** Enables outbound internet access to instances in a private subnet without exposing them to inbound internet traffic.

>  **Security Lists :** Acts like a firewall at subnet level. Defines stateless ingress and egress rules.

>  **Network Security Groups :** Like virtual firewalls, applied to individual resources rather than subnets. Allows fine grained control over traffic


# What is a Load Balancer ? 
Ans : A Load Balancer is a system that distributes the incoming traffic across multiple backend servers. Its main job is to ensure that no single server is overwhelmed by traffic.

# Purpose of Load Balancer :

> Distribute Traffic Efficiently across multiple backend servers.

> If one server goes down, then it routes traffic to remaining healthy servers by ensuring fault tolerance and high availabiliy.

> Easily add more servers if the traffic is high by using load balancer.

# Parts of Load Balancer :

> **Listener:** Listens on specific Ip address or ports

> **Routing Algorithm:** Decides how to route traffic to backend servers.

> **Health Checks :** Continously checks if backend servers are alive and healthy.

>  **Backend Pools :** group of backend servers that serves actual application content.


# What is Auto Scaling ? 
Ans : Autoscaling is a Cloud computing feature that adjusts the number of servers based on traffic load of the system.

# Purpose of Auto Scaling :

> If traffic spikes , autoscaling adds more servers.

> If traffic drops, autoscaling reduces the servers.

> Keeps your apps running smoothly by launching new instances if one fails.
