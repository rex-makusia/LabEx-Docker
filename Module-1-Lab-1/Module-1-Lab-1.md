# Introduction

Welcome to your first Docker lab! In this lab, you'll take your first steps into the world of containerization by learning about Docker, 
a powerful platform for developing, shipping, and running applications.

Docker allows you to package an application with all of its dependencies into a standardized unit called a container. This makes it easier to deploy and run applications consistently across different environments.

The best way to learn Docker is by doing. Don't just read through this lab – try out each command in the LabEx environment! It's the perfect place to experiment and learn.

In this lab, you'll learn how to:

- Understand basic Docker concepts
- Run your first Docker container
- Use essential Docker commands
- Explore Docker Hub

Tips: This Lab is part of the Docker Skill Tree, a structured knowledge system. After each step, the system verifies your actions, awarding skill points for correct responses 💡. Review your accumulated points by visiting the Docker Skill Tree after completing the lab.

# Understanding Docker Concepts
Before we start using Docker, let's familiarize ourselves with some key concepts. Don't worry if they seem complex at first - we'll see them in action soon!

1. **Container**: A lightweight, standalone, and executable package that includes everything needed to run a piece of software.

2. **Image**: Think of this as a template or blueprint for containers. It contains all the instructions needed to create a container.

3. **Docker Hub**: Like Github but for Docker images - it's where you can find and share container images.

4. **Docker Engine**: The core technology that runs and manages containers on your machine.



This diagram shows that:

<img width="704" height="410" alt="image" src="https://github.com/user-attachments/assets/ee1faa47-7968-4a26-9014-b45c695e2f67" />

- The Docker Engine runs containers
- Images are used to create containers
- Docker Hub stores images
- The Docker Engine can pull images from Docker Hub and push images to Docker Hub

# Running Your First Container
Now that we understand the basic concepts, let's run our first Docker container using the ```hello-world``` image. 
This simple image is designed to verify that your Docker installation is working correctly and to introduce you to the basics of Docker

To run the container, use the following commmand in your terminal:
```sh
docker run hello-world

Hello from Docker!
This message shows that your installation appears to be working correctly.

To generate this message, Docker took the following steps:
 1. The Docker client contacted the Docker daemon.
 2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
    (amd64)
 3. The Docker daemon created a new container from that image which runs the
    executable that produces the output you are currently reading.
 4. The Docker daemon streamed that output to the Docker client, which sent it
    to your terminal.

To try something more ambitious, you can run an Ubuntu container with:
 $ docker run -it ubuntu bash

Share images, automate workflows, and more with a free Docker ID:
 https://hub.docker.com/

For more examples and ideas, visit:
 https://docs.docker.com/get-started/

```
Let's break down what this command does:

1. ```docker```: This is the command to interact with the Docker Engine
2. ```run```: This subcommand tells Docker to create and start a new container.
3. ```hello-world```: This is the name of image we want to run

# Understanding Docker Images
Now that we've run our first container, let's explore Docker images in more detail. 
Remember, an image is like a blueprint or a template for a container. It contains all the instructions needed to create a container.

To see the images available on your local system, use the following command:
```sh
docker images
```

Let's break down what each column means:

- REPOSITORY: The name of the image. In this case, it's "hello-world".
- TAG: The version of the image. "latest" is the default tag if you don't specify one.
- IMAGE ID: A unique identifier for the image. This is useful when you need to refer to a specific image.
- CREATED: When the image was created. This helps you know if you have the most recent version.
- SIZE: The size of the image on disk. Docker images are designed to be lightweight, which is why the hello-world image is only 13.3kB.
  
The ```hello-world``` image is now stored locally on your system.
This means that if you run ```docker run hello-world``` again, Docker won't need to download the image from Docker Hub. It will use the local copy, making the process faster.

If you don't see the hello-world image, don't worry! It might have been automatically removed to save space. You can always pull it again by running ```docker pull hello-world```.

# Exploring Docker Hub
Docker Hub is a cloud-based registry service where Docker users and organizations can store and distribute their Docker images. It's like a GitHub for Docker images, serving as a central repository where you can find, share, and manage Docker images.

Let's explore Docker Hub:

1. Open your local web browser and go to [Docker Hub](https://hub.docker.com)
2. In the search bar at the top, type "hello-world" and press Enter
3. You'll see a list of images. Look for the official "hello-world" image (it should have an "Official Image" badge)
4. Click on the "hello-world" image to view its details

On the image page, you can see:

- A description of the image
- Usage instructions
- The number of pulls (downloads) the image has
- Tags (versions) available

Docker Hub is where Docker looks for images when you run a docker run command and the image isn't available locally. 
This is why you were able to run the hello-world container even though you hadn't explicitly downloaded the image beforehand.

Some key points about Docker Hub:

1. **Official Images**: These are curated by Docker and are typically well-maintained and documented. They're a good choice for beginners.

2. **Tags**: Images can have multiple versions, called tags. For example, you might see tags like "latest", "1.0", "2.1", etc. When you don't specify a tag (like we did with docker run hello-world), Docker assumes you want the "latest" tag.

3. **Pull Command**: On each image's page, you'll see a "Pull Command". This is what you'd use to manually download the image without running a container. For example: docker pull hello-world

4. **Dockerfile**: Many images on Docker Hub will have a link to their Dockerfile, which is the script used to build the image. This can be helpful if you want to understand how the image was created.

Exploring Docker Hub and understanding how to find and use images is a crucial skill in working with Docker. 
As you progress, you'll likely find yourself frequently searching Docker Hub for images that suit your needs.
