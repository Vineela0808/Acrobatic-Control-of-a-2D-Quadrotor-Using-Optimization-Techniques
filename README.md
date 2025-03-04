# Acrobatic-Control-of-a-2D-Quadrotor-Using-Optimization-Techniques
ROB 6323 Reinforcement Learning and Optimal Control for Robotics || Project - SQP &amp; MPC || Fall 2024
# 2D Quadrotor Acrobatic Control

This project focuses on controlling a **2D quadrotor** to perform **acrobatic maneuvers** using a **Sequential Quadratic Programming (SQP) solver**. The implementation is provided in a Jupyter Notebook.

## Table of Contents
- [Project Overview](#project-overview)
- [2D Quadrotor Model](#2d-quadrotor-model)
- [Installation](#installation)
- [Usage](#usage)
- [Dependencies](#dependencies)
- [Results](#results)
- [Contributors](#contributors)
- [License](#license)

## Project Overview
The goal of this project is to design a **controller for a 2D quadrotor** that enables it to perform acrobatic maneuvers efficiently. The controller is implemented using an **SQP solver**, optimizing control inputs for stable flight dynamics.

## 2D Quadrotor Model
The quadrotor's motion is governed by the following equations:

\[
\begin{align} 
\dot{p_x} &= v_x\\
m \dot{v}_x &= - (u_1 + u_2) \sin \theta \\ 
\dot{p_y} &= v_y\\
m \dot{v}_y &= (u_1 + u_2) \cos \theta  - m g\\
\dot{\theta} &= \omega\\
I \dot{\omega} &= r (u_1 - u_2) 
\end{align}
\]

where:
- \( p_x, p_y \) are the quadrotor's positions
- \( v_x, v_y \) are linear velocities
- \( \theta \) is the orientation
- \( \omega \) is the angular velocity
- \( u_1, u_2 \) are the forces from the rotors (control inputs)
- \( m \) is the mass, \( I \) is the moment of inertia

## Installation
To run the project, clone this repository and install the required dependencies:

```bash
git clone https://github.com/YOUR_GITHUB_USERNAME/quadrotor-sqp.git
cd quadrotor-sqp
pip install -r requirements.txt

