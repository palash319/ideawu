ICA-Infrastructure as a Code

  -Infrastructure as Code (IaC) is the management of infrastructure (networks, virtual machines, load balancers, and connection topology) in a descriptive model, using the same    versioning as DevOps team uses for source code. Like the principle that the same source code generates the same binary, an IaC model generates the same environment every        time it is applied. IaC is a key DevOps practice and is used in conjunction with continuous delivery.
  
CI/CD

Networking

Cloud Networking

Software Engineering

Namespaces are a feature of the Linux kernel that partitions kernel resources such that one set of processes sees one set of resources while another set of processes sees a different set of resources. 

Example:
We have two people with the same first name Mahbub Hasan and  Mahbub Hassan but we can differentiate them on the basis of their surname Hasan and Hassan. So you can think surname as a namespace.

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
