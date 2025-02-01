# Homework 1 - Network Dynamics and Learning

## Introduction

This report presents solutions to three exercises related to network dynamics and optimization, leveraging computational tools such as **NetworkX**, **NumPy**, **Matplotlib**, **CVXPY**, and **SciPy**. Each exercise focuses on different aspects of network analysis, including **maximum flow problems, shortest path computations, capacity allocation, and equilibrium analysis**.

- **Exercise 1** explores network flow capacity and optimization, analyzing the **minimum cut problem** and the impact of **additional capacity allocation** on network throughput.
- **Exercise 2** formulates a **matching problem** using a flow-based approach, extending it to scenarios with multiple resource allocations.
- **Exercise 3** examines a **traffic network**, incorporating shortest path computations, **maximum flow calculations**, **social optimal flow**, and **Wardrop equilibrium** analysis, along with toll-based traffic control strategies.

Throughout this report, numerical simulations and visualizations are employed to illustrate key findings. The **Python programming language** is used for all computational tasks, ensuring reproducibility and clarity. The **CVXPY library** plays a crucial role in solving **optimization problems**, while **NetworkX** facilitates network graph analysis. Figures and plots generated with **Matplotlib** provide visual insights into the problem solutions.

## Installation

To set up the project, ensure that you have Python installed (preferably Python 3.8 or later). Clone the repository and install the required dependencies:

```bash
git clone hhttps://github.com/taha-kms/Network-Dynamics-and-Learning.git
cd hw1
pip install -r requirements.txt
```

## File Structure
```bash
homework1/
│── ex1/                    # Exercise 1 solutions and code
│── ex2/                    # Exercise 2 solutions and code
│── ex3/                    # Exercise 3 solutions and code
│── data/                   # Data files (traffic.mat, capacities.mat, etc.)
│── homework1_report.pdf    # The report file
|── hw1_en_2024 (33806901).PDF
│── requirements.txt        # Dependencies
│── README.md               # Project documentation
```