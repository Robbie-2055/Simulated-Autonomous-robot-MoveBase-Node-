# Simulated-Autonomous-robot-MoveBase-Node-
This project implements an autonomous mobile robot navigation system using the ROS Navigation Stack.
A simulated TurtleBot3 robot navigates safely and efficiently from a start to a goal location on a 2D 
map using AMCL for localization, A* for global path planning, and DWA for obstacle avoidance.

**Functionality**
1. **Mapping**
   - Manually teleoperate the robot around the environment to craete a map using gmappng
   - Save the generated map after navigation

![1629887603284](https://github.com/user-attachments/assets/5bcdd4c2-d55e-489a-b6ea-8a6af38cb9fc)


2. **Localisation**
   - The AMCL node was utilised to estimate the robots's position and orientation on a staic map

<img width="155" alt="Picture2" src="https://github.com/user-attachments/assets/3cb64c47-13b2-46df-9b57-76711de26896" />


3. **Navigation**
   - In Rviz, the target gaol pose was set using the 2D goal pose tool
   - The Move_base node computed the path using the A* and sent velocity commands via the DWA
   - The robot then followed the path while avoiding dynamically avoiding obstacles

![Picture3](https://github.com/user-attachments/assets/4650b9e2-ccb4-422d-821b-8770609302af)


**Evaluation**

A* algorithm provided optimal path and successfully navigated to the set target goal. as seen in the graph

![Picture1](https://github.com/user-attachments/assets/9203f09a-8194-493b-9cc9-e28471940484)

