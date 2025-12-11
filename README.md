# Manipulator Robot – Inverse Kinematics and PID-Controlled Pick-and-Place (LEGO EV3)
As part of the Mechatronic System Laboratory at the University of Siegen, I developed a fully automated pick-and-place system using a 3-DOF LEGO Mindstorms EV3 manipulator controlled from MATLAB. The goal was to derive the inverse kinematics of the arm and implement robust behaviours for homing, picking, placing, and retracting a ball between three workstations (A, B, C).
A video demonstration of the task can be found on my Youtube Channel- at this link: https://www.youtube.com/watch?v=xFHLHVooJJU

---

## Key aspects:
* Derived closed-form inverse kinematics equations to map Cartesian target points to joint angles for the manipulator.
* Implemented a homing routine with touch sensors and motor encoders to establish a consistent mechanical zero position.
* Designed and tuned a discrete PID controller for joint motors B and C, including gear-ratio offsets, speed limits, and 1° position tolerance.
* Developed modular MATLAB scripts (`Homing`, `Inverse_Kinematics`, `Pick_Place_Behaviour`, `Gripper`, `UserInput`) for trajectory execution, gripper control, and optional user-defined waypoints in the workspace.
* Validated the system by repeatedly transporting the ball between stations A, B, and C with stable motion profiles and reproducible positioning.



## Scripts Overview

### 1. `Pick_Place_Behavior.m`

- **Description**: This script controls the gripper to hold and release a ball at different positions. Gripper behavior is determined by the position index.
- **Usage**: Provide the `rem` value (remainder) to decide whether the gripper will hold or release the ball based on the position index.

### 2. `Inverse_Kinematics.m`

- **Description**: This script calculates the inverse kinematics for predefined positions in the robot's workspace. It computes motor angles for precise motion.
- **Usage**: Run this script to perform the inverse kinematics calculations.

### 3. `Homing.m`

- **Description**: This script implements the homing behavior of the robot, ensuring it starts from a known position before pick-and-place operations.
- **Usage**: Execute this script to perform the robot homing sequence.

### 4. `UserInput.m`

- **Description**: This script allows users to input custom positions within the robot's workspace. It also adds an extra position at Platform B if the ball has been picked but not placed.
- **Usage**: Run this script to input desired positions and automatically add a placement position if needed.

## Getting Started

1. Clone this repository to your local machine.
2. Ensure you have MATLAB installed.
3. Open MATLAB and run the desired scripts according to your task requirements.
4. Follow the usage instructions provided for each script.

## Notes

- Carefully review the script descriptions and usage instructions to understand their functionality.
- Ensure that your robot and hardware setup are compatible with these scripts.
- Customize the scripts and parameters as needed to suit your specific robot system.

Feel free to reach out with any questions or issues you encounter while using these scripts.
Enjoy your robot pick-and-place automation!

