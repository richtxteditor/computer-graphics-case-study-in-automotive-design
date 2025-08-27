# Computer Graphics Case Study in Automotive Design

This repository contains two projects from a computer graphics course (AMAT 240, Fall 2022, taught by Dr. Song).

## Project 1: 2D Transformations of a Letter

This project focuses on the fundamentals of 2D computer graphics, including object definition, transformations, and rendering using Python with `numpy` and `matplotlib`.

### Objective
The goal was to define and draw a lowercase letter '''k''' and then apply various linear transformations to it.

### Implementation
1.  **Vertex Definition:** The vertices of the letter '''k''' are defined as a 2x11 numpy array.
2.  **Adjacency Matrix:** An 11x11 adjacency matrix is used to represent the connections between the vertices, defining the edges of the letter.
3.  **Rendering:** The letter is drawn by iterating through the adjacency matrix and plotting lines between connected vertices using `matplotlib`.
4.  **Transformations:**
    *   **Rotation:** The letter is rotated 45 degrees counter-clockwise.
    *   **Reflection:** The letter is reflected to create a backwards '''k'''.

## Project 2: 3D Automotive Design Case Study

This project is a case study on applying 3D transformations and perspective projection to render a 3D model of a car in a 2D space. The subject of the case study is a 1983 Toyota Corolla.

### Objective
To understand and implement 3D-to-2D perspective projection, as well as 3D transformations like rotation and scaling (zoom).

### Key Concepts
*   **Homogeneous Coordinates:** The 3D vertices of the car are represented in homogeneous coordinates (a 4D vector), which allows for translations to be represented as matrix multiplications.
*   **Data Matrix (D):** A 4x16 matrix containing the homogeneous coordinates of the 16 vertices of the car model.
*   **Adjacency Matrix (C):** A 16x16 matrix defining the connections between the vertices to form the wireframe model of the car.
*   **Perspective Projection:** A transformation that projects 3D points onto a 2D plane, creating a sense of depth. This is achieved by defining a center of projection (the viewer'''s eye) and a viewing plane.
*   **3D Transformations:**
    *   **Rotation:** The car model is rotated around the y-axis (yaw) and z-axis (roll).
    *   **Zooming (Scaling):** The car model is scaled uniformly to create a zoom effect.

### Implementation
The project involves a series of tasks implemented in a Jupyter Notebook (`project 2.ipynb`):
1.  **Plotting the 2D projection:** From different centers of projection.
2.  **Rotation then Projection:** Applying a 30° rotation about the y-axis and a 45° rotation about the z-axis before the perspective projection.
3.  **Zoom then Projection:** Applying a 150% zoom factor before the perspective projection.

All transformations are implemented using matrix multiplication on the homogeneous coordinates of the car'''s vertices. The final 2D images are rendered using `matplotlib`.
