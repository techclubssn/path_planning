# Docker on Windows (Extensive How -to Guide)

## Introduction

Welcome to your first step in ROS journey. This guide is meant for users with windows installation. Here we have used Windows 11. No errors must occur if the same is followed with Windows 10.

## Info on Docker

Docker is basically a software which allows users to mitigate different compatibility errors. It achieves this by virtualizing a OS for the application to be executed. We use docker in this course to allow seamless install experience.

## Installation

We will now begin installing Docker Desktop and pulling our course docker image.

It would be better if your PC had WSL2 support since it can be faster.

- [ ]  Use this website to download docker desktop: [https://docs.docker.com/desktop/windows/install/](https://docs.docker.com/desktop/windows/install/)

![Screenshot 2022-04-09 072948.png](https://github.com/techclubssn/path_planning/blob/master/Documentation/media/Screenshot_2022-04-09_072948.png?raw=true)

- [ ]  Install the downloaded file with administrator privileges.
- [ ]  (optional) follow the Interactive tutorial from the application for better understanding.

Now that we have completed our Docker desktop installation, it is time for us to pull our course image to start the course. 

- [ ] Start docker by opening the desktop app.

- [ ]  Open PowerShell by launching it via search

![Untitled](https://github.com/techclubssn/path_planning/blob/master/Documentation/media/Untitled.png?raw=true)

- [ ]  use the below command to start downloading the image

```powershell
docker pull shankrith/path_planning:0.1
```

![Untitled](https://github.com/techclubssn/path_planning/blob/master/Documentation/media/Untitled%201.png?raw=true)

Depending on your internet connection go have a tea break for it to complete download.

## **Set up Xlaunch**

1. Go to: [https://sourceforge.net/projects/vcxsrv/](https://sourceforge.net/projects/vcxsrv/) and click download.
2. Follow the default settings and install it

**Every time you need to use Docker do this:**

1. Open Xlaunch and check the settings
2. Most can stay at default, but ensure that:
    1. Native opengl is left unchecked
    2. Disable access control is checked
    

## **Running the container:**

### **First time when setting up:**

Open Docker Desktop and a Powershell window. In Powershell,

<insert content about pulling>

Next we have to run the container using this command:

```
docker run -it --name ros_turtlebot -e DISPLAY=host.docker.internal:0.0 -e LIBGL_ALWAYS_INDIRECT=0 shankrith/path_planning:0.1 bash
```

Now run 

```
roscore
```

to see if it works.

### **For subsequent uses:**

1. Open Docker Desktop and a Powershell window.
2. Open Powershell and run:

```
docker start ros_turtlebot
```

1. Next run:

```jsx
docker exec –it ros_turtlebot bash
```

1. For every additional terminal you open, it is sufficient to run the above command alone.

![Screenshot 2022-04-09 092130.png](https://github.com/techclubssn/path_planning/blob/master/Documentation/media/Screenshot_2022-04-09_092130.png?raw=true)

The ‘root@’ indicates that you’ve successfully entered your image.

Note: Make sure you check the setting in the Xlaunch app each time you open Docker (once every session)

You’re all set to start working, have fun!
Now we are ready to start our session on Sunday. 👍
