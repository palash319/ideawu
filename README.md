#**Keyword**

**ICA-Infrastructure as a Code**

   Infrastructure as Code (IaC) is the management of infrastructure (networks, virtual machines, load balancers, and connection topology) in a descriptive model, using the same    versioning as DevOps team uses for source code. Like the principle that the same source code generates the same binary, an IaC model generates the same environment every        time it is applied. IaC is a key DevOps practice and is used in conjunction with continuous delivery.
  
 **CI/CD**
 
 **Networking**
 
 **Cloud Networking**
 
 **Software Engineering**

#**Namespace**

Namespaces are a feature of the Linux kernel that partitions kernel resources such that one set of processes sees one set of resources while another set of processes sees a different set of resources. 

Example:
  We have two people with the same first name Mahbub Hasan and  Mahbub Hassan but we can differentiate them on the basis of their surname Hasan and Hassan. So you can think        surname as a namespace.

In Linux, namespaces are used to provide isolation for objects from other objects. So that anything will happen in namespaces will remain in that particular namespace and doesn’t affect other objects of other namespaces. For example: - we can have the same type of objects in different namespaces as they are isolated from each other.

Docker uses this namespace technology to provide the isolated workspace called the container. When you run a container, Docker creates a set of namespaces for that container.
These namespace provide a layer of isolation. Each aspect of a container runs in a separate namespace and its access is limited to that namespace.

Docker engine uses namespace such as the following on Linux:

	Mount (MNT): Controls mount points. When new namespaces are created the current mounts are copied to a new namespace.
	Process ID (PID): Provides processes with process IDs from other namespaces.
	Interprocess Communication (IPC): Prevents processes in different IPC namespaces from forming SHM functions.
	Network (NET): Virtualizes network stack.
	UNIX Time Sharing (UTS): This allows a system to have different host and domain names for various processes.

**Socket Binding**

Socket binding is the process of binding a socket to a network address within the system and an address is the combination of an IP address and a port number when a socket is bound the server can accept client connections.

![alt text](https://github.com/palash319/ideawu/blob/main/Socket_server.png?raw=true)

**Host Namespace:** 

      File Namespace: 
      Network Namespace:
      

**ARP (Address Resolution Protocol):**

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
		
	HardwareType (16 bit) - Specifies the type of physical network (eg. 1 – for Ethernet) 

	Protocol Type (16 bit) - Specifies the higher layer protocol. (Value is 2048 for IP)

	HLen (8 bit) - Hardware Address Length–Specifies the length of the link layer address (PhysicalAddress) 

	PLen (8 bit) - Protocol Address Length – Specifies the length of the higher layer protocol address (IP Address)

	Operation or opcode (16 bit) - specifies whether this is a request or a response. 

	Sender Hardware Address (48 bit) - specifies the link level layer or physical address of the sender. 

	Sender Protocol Address (32 bit) – Specifies the higher layer address (IP Address) of the sender.

	Target Hardware Address (48 bit) - specifies the link level layer or physical address of the target host. • Target Protocol Address (32 bit) - Specifies the higher layer address (IP Address) of the target host.

**CIDR:**

Classless inter-domain routing (CIDR) is a set of Internet protocol (IP) standards that is used to create unique identifiers for networks and individual devices. The IP addresses allow particular information packets to be sent to specific computers.

**Route Table**

A routing table is a set of rules, often viewed in table format that is used to determine where data packets traveling over an Internet Protocol (IP) network will be directed. All IP-enabled devices, including routers and switches, use routing tables. See below a Routing Table:

		 Destination      Subnet mask         Interface
		 128.75.43.0      255.255.255.0       Eth0
		 128.75.43.0      255.255.255.128     Eth1
		 192.12.17.5      255.255.255.255     Eth3
		 default                              Eth2
		 
The entry corresponding to the default gateway configuration is a network destination of 0.0.0.0 with a network mask (netmask) of 0.0.0.0. The Subnet Mask of default route is always 255.255.255.255 .



Each entry in the routing table consists of the following entries:

**Network ID:**
	The network ID or destination corresponding to the route.

**Subnet Mask:**
	The mask that is used to match a destination IP address to the network ID.

**Next Hop:**
	The IP address to which the packet is forwarded
	
**Outgoing Interface:**
	Outgoing interface the packet should go out to reach the destination network.

**Metric:**
	A common use of the metric is to indicate the minimum number of hops (routers crossed) to the network ID.
	
Routing table entries can be used to store the following types of routes:

	Directly Attached Network IDs
	Remote Network IDs
	Host Routes
	Default Route
	Destination


**OSI Model**

The OSI Model is a logical and conceptual model that defines network communication used by systems open to interconnection and communication with other systems. The Open System Interconnection (OSI Model) also defines a logical network and effectively describes computer packet transfer by using various layers of protocols.

![alt text](https://github.com/palash319/ideawu/blob/main/osi.png?raw=true)

**Loopback Address**

The loopback interface is a virtual interface. The only purpose of the loopback interface is to return the packets sent to it, i.e. whatever you send to it is received on the interface. It makes little sense to put a default route on the loopback interface, because the only place it can send packets to is the imaginary piece of wire that is looped from the output of the interface to the input. There is nothing that can change this behaviour of the loopback interface.

**MTU**

Maximum transmission unit (MTU) is the size of the largest protocol data unit (PDU) that can be communicated in a single network layer transaction. The MTU relates to, but is not identical to the maximum frame size that can be transported on the data link layer. Larger MTU is associated with reduced overhead. Smaller MTU values can reduce network delay.

**DNS**

**DNS Query**

**DNS Resolve**

**TcpDump**


