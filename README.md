ICA-Infrastructure as a Code

   Infrastructure as Code (IaC) is the management of infrastructure (networks, virtual machines, load balancers, and connection topology) in a descriptive model, using the same    versioning as DevOps team uses for source code. Like the principle that the same source code generates the same binary, an IaC model generates the same environment every        time it is applied. IaC is a key DevOps practice and is used in conjunction with continuous delivery.
  
CI/CD

Networking

Cloud Networking

Software Engineering

Namespaces are a feature of the Linux kernel that partitions kernel resources such that one set of processes sees one set of resources while another set of processes sees a different set of resources. 

Example:
  We have two people with the same first name Mahbub Hasan and  Mahbub Hassan but we can differentiate them on the basis of their surname Hasan and Hassan. So you can think        surname as a namespace.

In Linux, namespaces are used to provide isolation for objects from other objects. So that anything will happen in namespaces will remain in that particular namespace and doesn’t affect other objects of other namespaces. For example: - we can have the same type of objects in different namespaces as they are isolated from each other.

Docker uses this namespace technology to provide the isolated workspace called the container. When you run a container, Docker creates a set of namespaces for that container.
These namespace provide a layer of isolation. Each aspect of a container runs in a separate namespace and its access is limited to that namespace.

Docker engine uses namespace such as the following on Linux:

1.	Mount (MNT): Controls mount points. When new namespaces are created the current mounts are copied to a new namespace.
2.	Process ID (PID): Provides processes with process IDs from other namespaces.
3.	Interprocess Communication (IPC): Prevents processes in different IPC namespaces from forming SHM functions.
4.	Network (NET): Virtualizes network stack.
5.	UNIX Time Sharing (UTS): This allows a system to have different host and domain names for various processes.

Socket Binding

Socket binding is the process of binding a socket to a network address within the system and an address is the combination of an IP address and a port number when a socket is bound the server can accept client connections.

![alt text](https://github.com/palash319/ideawu/blob/main/Socket_server.png?raw=true)

Host Namespace: 

      File Namespace: 
      Network Namespace:
      

ARP (Address Resolution Protocol):
1.	ARP (Address Resolution Protocol) is a network protocol used to find out the hardware (MAC) address of a device from an IP address. 
2.	It is used when a device wants to communicate with some other device on a local network.
3.	IP datagram contains IP addresses, but the physical interface hardware on the host or router need an addressing scheme (Physical Addressing) of a particular network to send a packet. 
4.	So we need to translate the IP address to link level physical address.
5.	Each host to maintain a table of address pairs i.e., Mapping of IP address to Physical Address. 
6.	This can be achieved by
	
        •	Manually uploading the table entries (by administrator) 
        
        •	Dynamically build the table having the IP Address to Physical address mappings. – ARP approach.
        
7.	The goal of ARP is to enable each host on a network to build up a mapping between IP addresses and Physical addresses. 
8.	The set of mappings or table stored in the host is called as ARP cache or ARP table.
9.	If a host want to send an IP datagram to a host on the same physical network,

    •	It first checks for a mapping in a cache.
    
    •	If no mapping is found, it invokes the ARP. 
    
    •	ARP broadcasts the ARP query (it contains target IP address) onto the network. 
    
    •	A host with that IP address sends a response message that contains the physical address of that host to the originator.
    
    •	When a sender broadcasts the ARP query, each host on the network can learn the physical address of the sender from the query message and update or add the mapping into the       table.

![alt text](https://github.com/palash319/ideawu/blob/main/arp.jpg?raw=true)
