# Introduction
Welcome to the "Run Your First Container" challenge! You've already learned how to run the hello-world container. 
Now, let's take it a step further and run a different, interesting container. 
In this challenge, you'll use your newly acquired Docker skills to run a container that displays a fun message.

# Run a New Container
## Tasks
Your task is simple:

1. Run a Docker container based on the ```docker/getting-started``` image.

## Requirements
To complete this challenge, you must:

1. Use the ```docker run``` command to start the container.

2. Use the image ```docker/getting-started```.
   
Execute the command in the ```~/project``` directory.

```docker
labex:project/ $ docker images
REPOSITORY                    TAG       IMAGE ID       CREATED       SIZE
jenkins/jenkins               latest    ca7cca8fa4b0   2 years ago   466MB
hello-world                   latest    d2c94e258dcb   2 years ago   13.3kB
gcr.io/k8s-minikube/kicbase   v0.0.37   01c0ce65fff7   2 years ago   1.15GB
docker/getting-started        latest    3e4394f6b72f   2 years ago   47MB
labex:project/ $ docker run docker/getting-started 
/docker-entrypoint.sh: /docker-entrypoint.d/ is not empty, will attempt to perform configuration
/docker-entrypoint.sh: Looking for shell scripts in /docker-entrypoint.d/
/docker-entrypoint.sh: Launching /docker-entrypoint.d/10-listen-on-ipv6-by-default.sh
10-listen-on-ipv6-by-default.sh: info: Getting the checksum of /etc/nginx/conf.d/default.conf
10-listen-on-ipv6-by-default.sh: info: Enabled listen on IPv6 in /etc/nginx/conf.d/default.conf
/docker-entrypoint.sh: Launching /docker-entrypoint.d/20-envsubst-on-templates.sh
/docker-entrypoint.sh: Launching /docker-entrypoint.d/30-tune-worker-processes.sh
/docker-entrypoint.sh: Configuration complete; ready for start up
2025/08/02 05:36:37 [notice] 1#1: using the "epoll" event method
2025/08/02 05:36:37 [notice] 1#1: nginx/1.23.3
2025/08/02 05:36:37 [notice] 1#1: built by gcc 12.2.1 20220924 (Alpine 12.2.1_git20220924-r4) 
2025/08/02 05:36:37 [notice] 1#1: OS: Linux 5.15.0-56-generic
2025/08/02 05:36:37 [notice] 1#1: getrlimit(RLIMIT_NOFILE): 1048576:1048576
2025/08/02 05:36:37 [notice] 1#1: start worker processes
2025/08/02 05:36:37 [notice] 1#1: start worker process 30
2025/08/02 05:36:37 [notice] 1#1: start worker process 31
```
Verify the Docker process
```docker
Docker ps
CONTAINER ID   IMAGE                    COMMAND                  CREATED              STATUS              PORTS     NAMES
f31dd34e686b   docker/getting-started   "/docker-entrypoint.…"   About a minute ago   Up About a minute   80/tcp
```

# Summary
In this challenge, you've expanded your Docker skills by running a new container. 
You've used the ```docker run``` command to start a container from the ```docker/getting-started``` image, which displays some introductory information about Docker. 
This exercise reinforces your understanding of how to use Docker to run containers and introduces you to a new, informative Docker image. It's a great way to see how Docker can be used to quickly access and run pre-configured applications. 
Keep exploring different Docker images to continue expanding your containerization skills!
