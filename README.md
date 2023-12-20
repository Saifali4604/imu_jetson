# imu_jetson

```
cd ~/catkin_ws/src
git clone https://github.com/Saifali4604/imu_jetson
cd ~/catkin_ws/
catkin_make
```

Open a new terminal window, and print the path to your new ROS package named mpu_6050_driver.

```
rospack find mpu_6050_driver
rosdep update
rosdep check mpu_6050_driver
```
You should see a message that says “All system dependencies have been satisfied.”

```
cd ~/catkin_ws/
roscore
rosrun mpu_6050_driver imu_node.py
rosrun mpu_6050_driver tf_broadcaster_imu.py
rostopic list
rostopic echo /imu/data
```

