Controlling Robot Arm:
sudo apt-get install ros-noetic-catkin

mkdir -p ~/catkin_ws/src

cd ~/catkin_ws/

catkin_make

cd ~/catkin_ws/src
 
git clone https://github.com/smart-methods/arduino_robot_arm.git 
 
cd ~/catkin_ws
 
rosdep install --from-paths src --ignore-src -r -y
 
sudo apt-get install ros-noetic-moveit
 
sudo apt-get install ros-noetic-joint-state-publisher ros-noetic-joint-state-publisher-gui
 
sudo apt-get install ros-noetic-gazebo-ros-control joint-state-publisher
 
sudo apt-get install ros-noetic-ros-controllers ros-noetic-ros-control
 
sudo nano ~/.bashrc
 
 
at the end of the (bashrc) file add the follwing line 
but change it to you name
 
source /home/njoudalnamlah/catkin_ws/devel/setup.bash
 
source ~/.bashrc
 
roslaunch robot_arm_pkg check_motors.launch
![Screenshot (147)](https://user-images.githubusercontent.com/110668653/183089788-a821436c-5d62-49eb-a539-20aa55420c9d.png)
