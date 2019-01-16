# exploration-tool
This pkg contain some tools which will be used in exploration.

Functions:  
***No.1 Recording exploration trajectory  
No.2 Recording exploration length and time  
No.3 Calculate exploration percentage*** 

  
### How to run this project?
#### A.basic  
1.Clone it into your working space and use compile it:
```Bash
cd ~/XX_ws
catkin_make
```
2.Then add it to the source:
```Bash
source ~/XX_ws/devel/setup.bash
```
#### B.trajectory and route length  
3.You can test the code without any simulation environment:
```
roslaunch trajectory trajectory_test.launch
```
You can see the circular trajectory in **rviz**.    

4.In another new terminal, run:
```
rostopic echo /route_topic
```
then You can see the total time and total path length at present in this terminal.  

5.You can also use the tool in real exploration:
```
roslaunch trajectory trajectory.launch
```
6.In rviz, create a visualization: Trajectory.  
Now you can see the trajectory of your exploration.  

7.In another new terminal, run:
```
rostopic echo /route_topic
```
then You can see the total time and total path length at present in this terminal.  

#### C.exploration percentage  
8.Modify .yaml file in directory ../explore_percent/map .  
You need to modify the path of image in the first line.   

9.You can test the code without any simulation environment:
```
roslaunch explore_percent Test.launch
```
Now you can see the given map in **rviz**.  

10.You can also use it in real exploration:
```
roslaunch explore_percent GetFullMap.launch
```
This node will read the given map file and publish it to topic **/full_map**.  
The pecentage of exploration will be publish to topic **/occpercent**.  

### Notice
#### 1.About name  
The topic name of odometory should be **/odom**.  
If not, please remap the real topic name to **/odom**.  

The topic name of map should be **/map**.  
If not, please remap the real topic name to **/map**.  
#### 2.About time  
The timer will start when this node runs, so please add it into launch file of your exploration launch file.
