# Minecraft Server Container Setup

This project will get you started with a working survival Minecraft server.

## Installation
This setup assumes that the host machine is visible on the network. This means firewall rules and Docker should be configured, which is outside the scope of this setup.

Clone the repo and cd into it:

`git clone https://github.com/eneudys101/minecraft-docker.git`

`cd minecraft-docker`

### Building the Docker Image

To build the docker image replace `<IMAGE_NAME>` with the desired name.

`docker build -t <IMAGE_NAME> .`

### Usage

Now that the image is built run the container. To run the container replace `<VOLUME_NAME>` with a desired name for the volume so that the configuration can be persistent per run. Also, replace `<IMAGE_NAME>` with the previouly selected name on the building step.

`docker run -d -p 25565:25565 -v <VOLUME_NAME>:/minecraft <IMAGE_NAME>`
