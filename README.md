# wall-climbing-gait

```markdown
# Hexapod Robot Simulation

This MATLAB project simulates the movements of a hexapod robot's legs, including roll, pitch, and yaw. The simulation includes visualization of the hexapod's leg movements and body positions.

## Table of Contents

1. [Introduction](#introduction)
2. [Project Structure](#project-structure)
3. [Dependencies](#dependencies)
4. [Usage](#usage)
    - [Example](#example)
5. [Functions](#functions)
    - [rpy](#rpyrpy)
    - [rp](#rprp)
    - [tripod](#tripodtripody1-y2-z1-z2-p)
    - [invk](#invkinvkx-y-z-a)
    - [plot_hexapod](#plot_hexapodplot1x11-y11-z11-x21-y21-z21-x31-y31-z31-x41-y41-z41-x51-y51-z51-x61-y61-z61-theta11-theta12-theta13-theta21-theta22-theta23-theta31-theta32-theta33-theta41-theta42-theta43-theta51-theta52-theta53-theta61-theta62-theta63)
6. [License](#license)

## Introduction

The hexapod robot simulation code aims to model the leg movements of a hexapod robot. The hexapod has six legs, each with three joints. The code includes functions to simulate various movements, such as rolling, pitching, yawing, and a tripod gait.

## Project Structure

The project consists of a single MATLAB script file:

- `hexapod_simulation.m`: The main script that initializes the hexapod dimensions, sets the roll, pitch, and yaw angles, and runs the simulation.

## Dependencies

This project requires MATLAB to run. No additional toolboxes are required.

## Usage

To run the simulation, open `hexapod_simulation.m` in MATLAB and execute the script. The script will visualize the hexapod's leg movements based on the specified roll, pitch, and yaw angles.

### Example

To simulate pitch motion:

```matlab
for i = 0:1:5
    pitch_motion = rp(0, pitch); pause(0.25)
    pitch_motion1 = rp(0, 0); pause(0.1)
end
```

## Functions

### rpy(roll_angle, pitch_angle, yaw_angle, z)
Calculates the positions and angles for the legs based on roll, pitch, yaw angles, and vertical translation.

### rp(roll_angle, pitch_angle)
Calculates the positions and angles for the legs based on roll and pitch angles.

### tripod(y1, y2, z1, z2, p)
Simulates a tripod gait, where the legs move in sets of three for stability.

### invk(x, y, z, a)
Performs inverse kinematics calculations to determine the joint angles for a given position.

### plot1 = plot_hexapod(x11, y11, z11, x21, y21, z21, x31, y31, z31, x41, y41, z41, x51, y51, z51, x61, y61, z61, theta11, theta12, theta13, theta21, theta22, theta23, theta31, theta32, theta33, theta41, theta42, theta43, theta51, theta52, theta53, theta61, theta62, theta63)
Plots the hexapod's legs and body positions based on the calculated joint angles.

### plot_leg(x, y, z, T1, T2, T3)
Plots a single leg of the hexapod based on the joint angles.

## License

This project is licensed under the MIT License.
```

This README file provides a detailed overview of the hexapod robot simulation project, including its structure, dependencies, usage, and functions. Adjust any specific details as needed for your project.
