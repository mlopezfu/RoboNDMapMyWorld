# RoboNd-Map my world
Robotics Engineer Nanodegree Program

---
## Basic Build Instructions
Create catkin workspace

mkdir -p catkin_ws/src

cd catkin_ws/src

catkin_init_workspace

clone this repo

cd ..

catkin_make

source devel/setup.bash


## Basic Instructions
Run world with command:

roslaunch my_robot world.launch

Then run, if you want mapping:

roslaunch my_robot mapping.launch

![alt text](mapping.png)

After mapping data about database can be reviewed with the following command:

rtabmap-databaseViewer ~/.ros/rtabmap.db

Since we have copied the data to the maps folder, you can go to maps folder and run

rtabmap-databaseViewer rtabmap.db

![alt text](viewer.png)

There can be seen that the number of loop closures is 31


If you want localization:

roslaunch my_robot localization.launch

![alt text](localization.png)

This will also run teleop, that will move robot with these commands.
<pre><span class="anchor" id="line-1-3"></span>Reading from the keyboard  and Publishing to Twist!
<span class="anchor" id="line-2-1"></span>---------------------------
<span class="anchor" id="line-3-1"></span>Moving around:
<span class="anchor" id="line-4-1"></span>   u    i    o
<span class="anchor" id="line-5-1"></span>   j    k    l
<span class="anchor" id="line-6-1"></span>   m    ,    .
<span class="anchor" id="line-7-1"></span>
<span class="anchor" id="line-8-1"></span>q/z : increase/decrease max speeds by 10%
<span class="anchor" id="line-9-1"></span>w/x : increase/decrease only linear speed by 10%
<span class="anchor" id="line-10-1"></span>e/c : increase/decrease only angular speed by 10%
<span class="anchor" id="line-11-1"></span>anything else : stop
<span class="anchor" id="line-12-1"></span>
<span class="anchor" id="line-13-1"></span>CTRL-C to quit</pre>

However, if you want run teleop in stand alone you have a launch for it:
roslaunch my_robot teleop.launch

