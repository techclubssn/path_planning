# Install and Setup Instructions for Linux

Tested on Ubuntu 20.04. Should work with other versions as well.

## Cloning Workshop Repository
Clone the repository using the command below.
```
git clone https://github.com/techclubssn/path_planning.git
```

## Installing Docker
Follow [this](https://www.simplilearn.com/tutorials/docker-tutorial/how-to-install-docker-on-ubuntu) link to install docker on ubuntu.

## Pulling Pre-built Docker Image

The easiest way to try out this project is by using a pre-built Docker image that can be pulled from [Docker Hub](https://hub.docker.com/repository/docker/shankrith/path_planning).

```
docker pull shankrith/path_planning:0.1
```
In case you get an error, try running the same command with sudo prepended to it.

## Running the container

For running of the container, you can use the included [docker/run.bash](https://github.com/techclubssn/path_planning/blob/master/docker/run.bash) script that is included with this repo.

```
./<path_planning_repo_dir>/docker/run.bash shankrith/path_planning:0.1
```
