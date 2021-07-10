# Using Slam map to launch navigation
Launch the navigation of TurtleBot3 using slam map in ROS.

We alrady install the ROS and using SLAM with TurtleBot3 to create a map and save it. So after saving the map, we will use it to launch the navgation. which is the file of map we will use it in navigation is saved as map.yaml. 

<h2>Launch Simulation World :</h2>
The same Gazebo environment of the map will be used for Navigation. So, Run :

```
$ export TURTLEBOT3_MODEL=burger
$ roslaunch turtlebot3_gazebo turtlebot3_world.launch
```
**Note:** The TurtleBot3 Model I was chosen is TurtleBot3 Burger.

<h2>Run Navigation Node :</h2>
To launch the navigation node to make robot navigate, run this command:   

```
$ export TURTLEBOT3_MODEL=burger
$ roslaunch turtlebot3_navigation turtlebot3_navigation.launch map_file:=$HOME/map.yaml
```

<h2>2D Pose Estimate :</h2>
Here, we should use the Initial Pose Estimation button in the up bar in Rviz before navigation, which is used to locate the TurtleBot3 location on the map. Use it like this : <br> </br>

    
<image src = "https://user-images.githubusercontent.com/43522153/125178225-71ef3b80-e1eb-11eb-85ad-4e02472317b1.gif" width="700" />


<h2>2D Navigation Goal :</h2>
Here we should set the destination of the robot, using the 2D navigation goal button via determining the green arrow at the specific destination we want the robot to go to it. Which the start point of the arrow represents the x, y points and the end of the arrow represents the orientation.  After we do that, the TurtulBot3 will move.    <br></br>

The final result will be :  



https://user-images.githubusercontent.com/43522153/125178489-15415000-e1ee-11eb-8ed7-5d09c3d84b7d.mov



