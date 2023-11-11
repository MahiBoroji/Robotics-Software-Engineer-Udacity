## Overview
Project 1 of [Udacity Robotics Software Engineer Nanodegree Program.](https://www.udacity.com/course/robotics-software-engineer--nd209)


![Screenshot (1508)](https://github.com/MahiBoroji/Robotics-Software-Engineer-Udacity/assets/123837389/3d0d7713-1840-4f49-8c69-e4fe6af87708)



## Directory Structure

```c++
├── model                          # Model files 
│   ├── Building
│   │   ├── Building.config
│   │   ├── Building.sdf
│   ├── robot
│   │   ├── model.config
│   │   ├── model.sdf
|   ├── Shelf                      # Static Models in Gazebo
|   ├── table                      
├── script                         # Gazebo World plugin C++ script      
│   ├── welcome.cpp
├── world                          # Gazebo main World containing models 
│   ├── MyWorld
├── Build                          # Build My World Project 
└── CMakeLists.txt                 # Link libraries 
```

- MyWorld: Gazebo world file.
- Building: Building structure by Building Editor of Gazebo.
- robot: A robot built by Model Editor of Gazebo.
- welcome.cpp: Gazebo world plugin C++ script.
- CMakeLists.txt: File to link the C++ code to libraries.

## Run This Project

After cloning this repository, make a directory as build.
```c++
sudo mkdir build
cd build
```
In build directory, compile your code with
```c++
sudo cmake ../
make
```
Then,
```c++
export GAZEBO_PLUGIN_PATH=${GAZEBO_PLUGIN_PATH}:/home/workspace/Project1_World/build
```
go back to world in order to launch the world and plugins in gazebo.
```c++
cd ..
cd world
```
Then run the world file using this code.
```c++
gazebo MyWorld
