>>> Basic Docker Commands

1.  docker run <imageNAME>				- start a container
2.  docker ps 						- list running containers and show basic info about them(ID, name; etc)
3.  docker ps -a					- list all running and previously stopped or exited containers
4.  docker stop	<ContainerID/NAME>			- stop a container
5.  docker rm <ContainerID/NAME>			- remove a stopped/exited container
6.  docker images					- list images
7.  docker rmi <imageNAME>				- remove image (Delete all dependent container to remove image.)
8.  docker pull <imageNAME>				- download image and store on host
9.  docker run <imageNAME> sleep <time in sec>		- appending sleep command on an image
10. docker exec <ContainerID/NAME> cat <link to dir>	- executea a command in a docker container (in this case, to print the contents of a file)
11. docker run -d <imageNAME>				- to run container in background mode (detach)
12. docker attach <ContainerID/NAME>			- to attach back to a running container (for ContainerID we can use first few characters)
