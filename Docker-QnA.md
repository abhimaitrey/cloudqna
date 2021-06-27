# Docker Questions

### What is the main difference between a VM and Docker?

Ans. 

### What is a docker daemon and how to start it manually?

Ans. 

The docker daemon can manually be started with the following command:

<code>$ dockerd </code>

Or

If you wish to configure the Docker daemon, then there are 2 options:

1. Use a JSON configuration file
2. Use flags when starting <code>dockerd</code>

### How do layers work in docker?

### What does docker compose do?

### Does docker containers are stateful?

Ans. 
Maintaining state in an app means finding a way to connect containers to stateful storage. For example, if you open up your weather app on your mobile device, it remembers your home city as the weather app maintains state. The only way to containerize applications that require state is to connect containers to stateful, persistent storage.

Containers were originally designed to be stateless and ephemeral (temporary). A stateless application is one that neither reads nor stores information about its state from one time that it is run to the next. A stateful application, on the other hand, can remember some things about its state each time it runs.

Docker and AWS are collaborating on making the right workloads more easily deployed as stateful containerized applications. 

source : https://www.docker.com/blog/deploy-stateful-docker-containers-with-amazon-ecs-with-amazon-efs/



