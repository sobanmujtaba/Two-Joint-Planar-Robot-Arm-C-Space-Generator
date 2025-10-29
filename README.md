# Two-Joint Planar Robot Arm C-Space Generator

This is an interactive web application designed to visualize and calculate the Configuration Space (C-Space) for a 2-link planar revolute robotic arm. This tool is fundamental for understanding motion planning and robotics kinematics, particularly in collision avoidance.

Key Features

Interactive Workspace: Users can draw arbitrary polygonal obstacles directly onto the workspace (the physical environment) using mouse clicks. Multiple obstacles are supported.

Dynamic Robot Kinematics: The lengths of Link 1 ($\text{L}_1$) and Link 2 ($\text{L}_2$) can be adjusted in real-time via dedicated sliders. This instantly changes the robot's dimensions and requires a recalculation of the forbidden C-Space region.

C-Space Mapping: The application calculates the corresponding C-Obstacle (the forbidden region) in the $\theta_1$-vs-$\theta_2$ plane. This calculation is performed using a high-resolution grid search ($100 \times 100$ configurations) combined with forward kinematics and a robust point-in-polygon collision detection algorithm.

Visualization: The Workspace shows the robot and the drawn obstacles, while the C-Space displays the full range of configurations ($\theta_1 \in [-\pi, \pi]$, $\theta_2 \in [-\pi, \pi]$) with the forbidden states marked in red.

Single-File Implementation: The entire application is contained within a single index.html file, using pure JavaScript, HTML5 Canvas, and Tailwind CSS for styling, ensuring easy deployment and review.

Technology Stack

HTML5 Canvas: Used for rendering both the physical workspace and the configuration space plot.

Pure JavaScript: Handles all application logic, including event listeners, kinematics calculations, and collision detection.

Tailwind CSS: Provides a modern, responsive, and aesthetically pleasing user interface.
