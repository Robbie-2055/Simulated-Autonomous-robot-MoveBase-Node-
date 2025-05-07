# Simulated-Autonomous-robot-MoveBase-Node-
This project implements an autonomous mobile robot navigation system using the ROS Navigation Stack.
A simulated TurtleBot3 robot navigates safely and efficiently from a start to a goal location on a 2D 
map using AMCL for localization, A* for global path planning, and DWA for obstacle avoidance.

The system Integrates:
* Gmapping for mapping
* AMCL for localisation
* A* for flobal path planning
* DWA (Dynamic Window Approach) for obstacle avoidance

## Key features
1. **Mapping**
   - Manually teleoperate the robot around the environment to craete a map using gmappng
   - Save the generated map after navigation

    ![1629887603284](https://github.com/user-attachments/assets/5bcdd4c2-d55e-489a-b6ea-8a6af38cb9fc)


2. **Localisation**
   - The AMCL node was utilised to estimate the robots's position and orientation on a staic map

    <img width="300" alt="Picture2" src="https://github.com/user-attachments/assets/3cb64c47-13b2-46df-9b57-76711de26896" />


3. **Navigation**
   - In Rviz, the target gaol pose was set using the 2D goal pose tool
   - The Move_base node computed the path using the A* and sent velocity commands via the DWA
   - The robot then followed the path while avoiding dynamically avoiding obstacles

   ![Picture3](https://github.com/user-attachments/assets/4650b9e2-ccb4-422d-821b-8770609302af)


## Evaluation

The navigation system was tested in simulation, and the robot successfully reached its goals by computing optimal paths using the A* algorithm. The DWA planner handled real-time obstacle avoidance effectively.

   ![Picture1](https://github.com/user-attachments/assets/9203f09a-8194-493b-9cc9-e28471940484)


## Acknowledgements
* This project was developed with the help of the simulation tools provided by The Construct – an online platform for learning and developing robotics applications using ROS in simulation. I was able to run my ROS project using this online platform even using my windows PC.
* Prior to developing this project, I as able tak on the ROS navigation course on the construct which gave me a base understanding of navigation in ROS 1.

## Future developments
As ROS 1 approaches its end-of-life, the next major step will be to transition this project to ROS 2 and implement navigation using the Nav2 stack. Additional goals include:

* Enhancing path planning and localization with ROS 2 features
* Integrating real-time obstacle avoidance with improved simulation fidelity
* Exploring behavior trees and lifecycle management in Nav2


