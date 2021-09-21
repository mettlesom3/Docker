>> Why do you need Docker?

To avoid-
- Compatibility/Dependency issues
- Long setup time
- Different Dev/Test/Prod environment issues

>> What can it do?

- Containerize Applications
- Run each service with its own dependencies in separate containers

>> What are containers?

- Completely isolated environments(Own processes, services, mounts, and network interfaces)
- Share the same OS kernel
- Types are: LXC, LXD, LXCFS, etc
- Docker uses LXC

>> Setting up container environments is hard as they are very low-level. Docker offers a high-level tool with several powerful functionalities that make this task easier.

>> OS

- Consists of OS Kernel and a set of software

>> Sharing the Kernel

- Docker container share the underlying kernel of the host OS.
- Won't be able to run a Windows-based container on a Docker host with Linux on it as the Kernel is different, you will require Docker on a Windows server.
- Unlike Hypervisors, Docker is not meant to virtualize and run different operating systems and kernels on the same hardware.
- Main purpose of Docker is to package and containerize applications, ship them, and run them anywhere anytime as many times as you want.

>> Containers VS VMs

Containers-
- Hardware Infrastructure --> OS --> Docker --> Container(s) 
- Inside a Container -- Application, Libraries, and Dependencies.
- Low utilization of underlying resources, low disk space usage.
- Boots up faster.
- Docker has less isolation as more resources are shared between the containers like the kernel.

VMs-
- Hardware Infrastructure --> Hypervisor --> VM(s)
- Inside a VM -- OS, Application, Libraries, and Dependencies.
- Higher utilization of underlying resources, higher disk space usage.
- Boots up slower.
- VMs have complete isolation from each other.

>> Containers & VMs

- Large environments with thousands of application containers running on thousands of Docker hosts, often containers are provisioned on virtual Docker hosts.
- Hardware Infrastructure --> Hypervisor --> VMs(OS --> Docker --> Container(s))
- No need to create many VMs as each VM can run multiple application containers.

>> How is it done?

- There are lots of containerized versions of applications readily available.
- Most organizations have their products containerized and available in a public Docker repository called Docker Hub or Docker Store. For example- images of common OSs, databases, and other services and tools.

  Command- docker run name-of-the-image
  
>> Container VS Image

- An image is a package or a template, just like a VM template. It is used to create one or more containers.
- Containers are running instances of images that are isolated and have their own environments and set of processes.
- A lot of products have been dockerized already. In case we do not find what we are looking for, we can create our own image and push it to the Docker Hub repository making it available for the public.

>> Docker in DevOps

- With Docker, the Dev and Ops team work hand in hand to transform the guide(set of instructions for the application) into a Docker file with both of their requirements.
- This Docker file is used to create an image for their application. This image can run on any host with Docker installed on it. This image works the same way everywhere.

>> Installation - https://docs.docker.com/engine/install/ for info.