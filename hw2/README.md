# Homework 2 - Network Dynamics and Learning

## Introduction

This repository contains solutions to the second homework assignment for the **Network Dynamics and Learning** course. The assignment explores **random walks, opinion dynamics, and network simulations** using computational tools such as **NumPy**, **Matplotlib**, and **Python-based simulation methods**. The exercises involve both **single-particle and multi-particle simulations**, analyzing transition dynamics and steady-state behaviors.

- **Problem 1** investigates a **single-particle continuous-time random walk** on a given network. The simulation is used to compute **return times, hitting times, and opinion dynamics** based on the **French-DeGroot model**.
- **Problem 2** extends the previous problem by considering **multiple particles moving simultaneously** in the network. It compares two perspectives: 
  - The **particle perspective**, where individual particle trajectories are tracked.
  - The **node perspective**, where the number of particles at each node is analyzed over time.
- **Problem 3** introduces an **open network model**, where particles enter and leave the system. The simulation is performed under two scenarios:
  - **Proportional rate movement**, where transition rates depend on the number of particles at a node.
  - **Fixed rate movement**, where nodes pass along particles at a constant rate.
  
The report accompanying this code presents detailed explanations, theoretical derivations, and comparisons between analytical expectations and simulation results.


## Installation

To set up the project, ensure that you have Python installed (preferably Python 3.8 or later). Clone the repository and install the required dependencies:

```bash
git clone hhttps://github.com/taha-kms/Network-Dynamics-and-Learning.git
cd hw2
pip install -r requirements.txt
```

## File Structure
```bash
homework1/
│── ex1/                    # Exercise 1 solutions and code
│── ex2/                    # Exercise 2 solutions and code
│── ex3/                    # Exercise 3 solutions and code
│── homework2_report.pdf    # The report file
│── hw-2-2024_en.pdf
│── requirements.txt        # Dependencies
│── README.md               # Project documentation
```