# Lid_Driven_Cavity_CFD_in_Python


This repository contains a simple implementation of the **2D lid-driven cavity flow** using the **finite difference method** to solve the incompressible Navier-Stokes equations.

The lid-driven cavity is a classical problem in fluid dynamics where a square cavity has a moving top lid and stationary walls elsewhere. It’s a standard benchmark problem for testing CFD solvers.

---

## 🧠 What This Code Does

- Solves 2D incompressible Navier-Stokes equations
- Uses an iterative method (Jacobi) to solve the pressure Poisson equation
- Implements boundary conditions for a cavity with a moving lid
- Visualizes velocity and pressure fields

---

## 📁 File

- `PythonApplication4.py`  
  → Main Python script for the simulation

---

## ⚙️ Requirements

- Python 3.x
- NumPy
- Matplotlib




## 🧾 Simulation Parameters

- **Grid size**: 41 x 41  
- **Number of time steps**: 500  
- **Viscosity**: 0.1  
- **Lid velocity**: 1.0 (top boundary)  
- **Time step size and convergence criteria** are hardcoded for simplicity


## 🔧 Simulation Setup

The lid-driven cavity problem is set up with the following conditions:
- **Grid Setup**: A 2D square grid of size 41 x 41 is used to discretize the domain. The grid represents the fluid-filled cavity, where each grid point holds values for pressure, velocity components, and other variables.
- **Boundary Conditions**: 
  - The **top lid** (moving boundary) is set with a constant velocity of 1.0 units in the horizontal direction.
  - The **bottom**, **left**, and **right walls** are stationary (no-slip boundary conditions).
- **Fluid Properties**: The flow is incompressible and governed by the Navier-Stokes equations with a kinematic viscosity of 0.1.
- **Time Stepping**: The simulation runs for 500 time steps, and the time step size is determined based on the grid resolution and stability criteria.

## 🌊 Flow Physics

The **lid-driven cavity** is a classic problem in fluid dynamics, particularly in computational fluid dynamics (CFD). It involves the study of fluid flow inside a square cavity with a moving top boundary (lid), while the other boundaries are stationary. The key flow features include:

- **Vortex Formation**: As the moving lid drives the fluid, vortices form in the cavity, especially near the top corners. The interaction between these vortices and the boundary layers is a critical aspect of the flow behavior.
- **Incompressible Flow**: The flow is assumed to be incompressible, which means the fluid density does not change throughout the flow. This assumption simplifies the Navier-Stokes equations by eliminating the need for a continuity equation for density.
- **Boundary Layer Development**: Near the moving lid, a boundary layer develops where the velocity gradient is steepest. The solution requires resolving this boundary layer accurately, which is handled through the chosen numerical methods.

By simulating the lid-driven cavity flow, we can investigate important flow characteristics, such as vortex formation, velocity profiles, and pressure distributions, which are essential for validating CFD solvers.




## 📊 Output

- **2D quiver plot** of velocity vectors  
- **Contour plot** of the pressure field



## 📚 References

- [CFD Python – Prof. Lorena A. Barba](https://github.com/barbagroup/CFDPython)
- [Original GitHub Project](https://github.com/Ceyron/machine-learning-and-simulation)

