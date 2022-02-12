#How to Migrate Catkin Workspaces

##This is a quick guide for how to migrate Catkin workspaces. The process is fairly straightforward, as shown in [this forum post](https://answers.ros.org/question/193901/how-to-migrate-a-catkin-workspace/).

##Below is a written explanation as well as a short video showing the steps. Let's get started!

Here is the video:
![short video tut](https://github.com/JamesHolland181/ROS-Tutorials/blob/main/Migrating%20Catkin%20Workspace/2022-02-12_04-13-38.mp4)

First, Remove “devel/” and “build/” directories as well as the “CmakeLists.txt” file in the “src/” directory as shown below.

![directories to remove](https://github.com/JamesHolland181/ROS-Tutorials/blob/main/Migrating%20Catkin%20Workspace/directories%20to%20remove.png)
![cmakelist to remove](https://github.com/JamesHolland181/ROS-Tutorials/blob/main/Migrating%20Catkin%20Workspace/file%20to%20remove.png)

Next, relocate the target package(s) to the desired location.

![desired packages](https://github.com/JamesHolland181/ROS-Tutorials/blob/main/Migrating%20Catkin%20Workspace/workspace%20to%20move.png)
![target location](https://github.com/JamesHolland181/ROS-Tutorials/blob/main/Migrating%20Catkin%20Workspace/target%20location.png)

Finally, source your ROS distro ('source /opt/ros/DISTRO/setup.bash') and then run 'catkin_make' in the top directory.
