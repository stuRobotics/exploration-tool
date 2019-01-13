# exploration-tool
This pkg contain some tools which will be used in exploration.

Functions:  
***Recording exploration trajectory  
Recording exploration length and time*** 

  
### How to run this project?

1.Clone it into your working space and use compile it:
```Bash
cd ~/XX_ws
catkin_make
```
2.Then add it to the source:
```Bash
source ~/XX_ws/devel/setup.bash
```
3.You can test the code without any simulation environment:
```
roslaunch trajectory trajectory_test.launch
```
4.You can also use the tool in real exploration:
```
roslaunch trajectory trajectory.launch
```

### Notice
#### 1.About name  
The topic name of odometory should be **/odom**.  
If not, please remap the real topic name to **/odom**.  
#### 2.About time  
The timer will start when this node runs, so please add it into launch file of your exploration launch file.
