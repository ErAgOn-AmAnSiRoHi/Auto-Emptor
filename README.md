<h1 align="center">Hi 👋, I'm Aman Sirohi</h1>
<h3 align="center">Student at Amrita Vishwa Vidyapeetham, Coimbatore🌟.</h3>
<h3 align="center">Academic Porgramme: B.Tech in AIE (Artificial Intelligence Engineering)</h3>
<br>
<br>

<h2 align="center">21AIE213 - ROS</h2>
<h2 align="center">SEMESTER-4 [TERM PROJECT]</h2>
<h2 align="center">Batch-A Group-1</h2>
<br>
<br>
<h1 align="center"> Auto-Emptor - Your Own Shop Dog</h1>
<br>

<h4 align="center">Our project might not be upto the real-life implementations as of now, but it has scope for huge improvements and can make the future lives much better.</h4> 
  <h4 align="center">What is it about!?</h4>
Well, our project is consisting of a Mobile Robot (2 Left-Right Wheels and 1 Caster Wheel) which is capable of roaming around in a maze type environment while avoiding collisions with any obstacles.</h5>
  <h4 align="center">So, that's it!? It is a decent implementation but not very useful in itself as it is!</h4>
But our Robot has a Camera and it is capable enough to go to the Billing Counter, scan the QR Code which corresponds to a Payment Gateway (considering modern days advancement in the usage of Online Payments and UPIs) and return the QR Code as it is, in an Output Window and also the decoded message (which is the payment link in our case) in the terminal/shell running the relevant script. All this can be achieved by the user and that too through the comfort of their home.</h4>
<br>
<br>
<h4 align="center">Our Project is performed by the utilization of ROS2 [ver:Humble Hawksbill] and Gazebo, primarily. Other than that, we have utilized OpenCV, cv_bridge, Pyzbar and RVIZ2 for our Project Work.</h4>
<br>

## Group Members
* Aman Sirohi [CB.EN.U4AIE21003]
* Vikhyat Bansal [CB.EN.U4AIE21076]
* Rakhil ML [CB.EN.U4AIE21048]
* R Sriviswa [CB.EB.U4AIE21046]

<br>
<br>
  
## Contents
* [Spawner Package](https://github.com/ErAgOn-AmAnSiRoHi/Auto-Emptor/tree/main/warehouse_robot_spawner_pkg)
* [Controller Package](https://github.com/ErAgOn-AmAnSiRoHi/Auto-Emptor/tree/main/warehouse_robot_controller_pkg)

* [QR-CODE MODEL](https://github.com/ErAgOn-AmAnSiRoHi/Auto-Emptor/tree/main/QR_Code_Model/texture)

* [PPT](https://github.com/ErAgOn-AmAnSiRoHi/Auto-Emptor/blob/main/ROS_TEAM_1_BATCH_A_END_TERM.pptx)

<br>
<br>

## Tools and Libraries
* Gazebo
  > ```sudo apt install ros-$ROS_DISTRO-gazebo-ros-pkgs```
* OpenCV
  > ```sudo apt-get install libopencv-dev python3-opencv```
* PyZBar
  > ```pip install pyzbar```
* cv_bridge
  > ```sudo apt-get install ros-$ROS_DISTRO-vision-opencv```   
  >    ```sudo apt-get install ros-$ROS_DISTRO-cv-bridge```

<br>
<br>

## How to Run
* After creating the desired packages, go to the ros workspace directory.
* There, do ```colcon build``` or ```colcon build --packages-select <pkg_name>``` if you want to build a specific package instead of all the packages in the workspace.
* Now, being in the workspace directory, do ```source install/setup.bash```
* Now, in a terminal window, simply type ```ros2 launch <pkg_name> <launch_file_name>```
* * So, in our case, since we have two packages, you will have to start two terminals and initially run:   
  > ```ros2 launch warehouse_robot_spawner_pkg gazebo_world.launch.py```   
* *  After the Gazebo simulation has started successfully, we need to run:   
  > ```ros2 launch warehouse_robot_controller_pkg controller_estimator.launch.py```   
* *  Then in one more terminal window, we need to run:   
  > ```ros2 run warehouse_robot_spawner_pkg decode_qr```
* *  One can also start another script which gives Real-Time Camera Feed in a separate CV Window [Make sure to open another terminal window]:
  > ```ros2 run warehouse_robot_spawner_pkg camera_read```
<br>
<br>

## Simulation Video (Basic Layout of a Mart)
https://amritavishwavidyapeetham-my.sharepoint.com/:v:/g/personal/cb_en_u4aie21003_cb_students_amrita_edu/EaNcJRI3JM1JioUTcdLq7oMBysudWm0ew7rwrRGFZMmaBg?e=qW20nr   
<br>
* * * Better Layout of the Mart (with Human Models added as extra obstacles and extra models for decoration sake)   
https://amritavishwavidyapeetham-my.sharepoint.com/:v:/g/personal/cb_en_u4aie21003_cb_students_amrita_edu/EZjKWvG0IzVNvWs4TzDx7ggB86gl3PUX3uX1kzanuVWfxQ?e=KH0Rgi
