# path_planning
As a part of Zenith 2022, Tech Club conducted a series of workshops about using ROS and Gazebo to simulate path planning algorithms on a turtlebot.

## Installation

<details>
<summary>Docker</summary>
  
### Requirements

- **OS:** Any system that supports [Docker](https://docs.docker.com/get-docker) should work (Linux, Windows, macOS).

### Pre-built Docker Image

The easiest way to try out this project is by using a pre-built Docker image that can be pulled from [Docker Hub](https://hub.docker.com/repository/docker/shankrith/path_planning).

```bash
docker pull shankrith/path_planning:0.1
```

For running of the container, you can use the included [docker/run.bash](docker/run.bash) script that is included with this repo.

```bash
<path_planning_dir>/docker/run.bash shankrith/path_planning:0.1
```
</details>

<details>
<summary>Local Installation</summary>
  
  ### Requirements
  - **OS:** Ubuntu 20.04 (Focal)
    - Others might work, but they were not tested. 
  
  ### Dependencies
  These are the primary dependencies of this repository
  1. ROS [Noetic](http://wiki.ros.org/noetic/Installation/Ubuntu)
  2. Turtlebot packages
     * [Turtlebot Core](https://github.com/ROBOTIS-GIT/turtlebot3) Packages
     * [Turtlebot Msgs](https://github.com/ROBOTIS-GIT/turtlebot3_msgs) package
     * [Turtlebot Simulation](https://github.com/ROBOTIS-GIT/turtlebot3_simulations) package
</details>
