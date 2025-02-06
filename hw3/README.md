# Epidemic Simulation and Graph Coloring using Distributed Learning


1. **Exercise 1** - Simulating the spread of an epidemic on different graph structures.
2. **Exercise 2** - Solving graph coloring problems using a distributed learning algorithm.

Each exercise demonstrates the use of graph-based models and probabilistic approaches to solve real-world problems.

---

## Exercise 1: Epidemic Simulation on Graphs

### **Problem Description**
This example simulates the spread of an epidemic on two different types of networks:
- **k-Regular Graph** (Uniform connectivity)
- **Preferential Attachment Graph** (Heterogeneous connectivity)

The simulations model the transmission of an infectious disease using variations of the **SIR (Susceptible-Infected-Recovered) model**, incorporating:
- Infection rate (**β**)
- Recovery rate (**ρ**)
- Vaccination strategies (**SIRV model** in later simulations)

The simulations run for **15 weeks** with **100 iterations** for statistical robustness.

### **1.1 Epidemic on a k-Regular Graph**
- A **symmetric k-regular graph** is generated with:
  - **500 nodes**
  - **Each node connected to 6 neighbors (k = 6)**
- Disease parameters:
  - **Infection probability (β) = 0.25**
  - **Recovery probability (ρ) = 0.6**
- Initially, **10 randomly selected individuals** are infected.
- The simulation tracks:
  - **New infections per week**
  - **Total susceptible, infected, and recovered individuals over time**
- **Observations**:
  - Infections peak around **Week 2-3**.
  - By **Week 15**, **72.9% remain susceptible**, **26.3% recover**, and **only 0.7% remain infected**.

### **1.2 Epidemic on a Preferential Attachment Graph**
- A **random network** is generated using a **preferential attachment model**.
- Unlike the k-regular graph, this network has **high-degree nodes ("super-spreaders")**.
- The simulation uses:
  - **β = 0.3**
  - **ρ = 0.7**
- **Observations**:
  - Faster spread due to high-degree nodes.
  - **Only 21.1% remain uninfected**, while **78.9% recover**.

### **1.3 Epidemic with Vaccination (SIRV Model)**
- Introduces **vaccination** to control the spread.
- **Vaccination schedule:** Vacc(t) = [0, 5, 15, 25, 35, 45, 55, 60, 60, 60, 60, 60, 60, 60, 60]

- By Week 8, **60% of the population is vaccinated**.
- **Observations**:
- Vaccination **significantly reduces infections**.
- **Only 0.7% of the population remains susceptible**.
- **56% get vaccinated, 43.2% recover**.

### **1.4 Estimating Epidemic Parameters from Real Data**
- Uses a **gradient-based search algorithm** to estimate:
- **Average degree (k)**
- **Infection rate (β)**
- **Recovery rate (ρ)**
- Parameters estimated from **real H1N1 pandemic data in Sweden**:
- **k = 13**, **β = 0.105**, **ρ = 0.395**
- **Comparison with real data**:
- Model closely matches **true infection trends**, peaking around **Weeks 5-7**.

---

## Example 2: Graph Coloring using Distributed Learning

### **Problem Description**
This example applies **distributed learning** to solve **graph coloring problems**, including:
1. **Graph coloring for conflict-free assignment.**
2. **Wi-Fi channel assignment to minimize interference.**

Each problem is approached with a **probabilistic learning algorithm** that updates node states iteratively.

### **2.a Distributed Graph Coloring on a Line Graph**
- **Problem:** Assign **two colors (Red, Green)** to **10 nodes** in a **line graph** such that no two adjacent nodes share the same color.
- **Solution Approach:**
- Uses **a distributed probabilistic algorithm** where each node updates its color based on local conflicts.
- **Potential function U(t)** measures conflicts in the graph.
- **Observations:**
- Initially, **U(0) = 7** (all nodes same color).
- After **20 iterations**, **U(t) = 0**, meaning a conflict-free coloring is achieved.

### **2.b Wi-Fi Channel Assignment using Graph Coloring**
- **Problem:** Assign **8 different Wi-Fi channels** to routers while minimizing interference.
- **Graph Model:**
- Nodes = **Wi-Fi routers**
- Edges = **Interference links**
- **Cost Function:**
- **Severe interference (same channel) → Highest cost**
- **Mild interference (adjacent channels) → Medium cost**
- **No interference → Zero cost**
- **Solution Approach:**
- A distributed learning algorithm iteratively updates channel assignments.
- **Observations:**
- Initially, high interference.
- Over **600 iterations**, interference is **minimized**.
- **Final assignments ensure low-interference Wi-Fi network**.

---

## Results

- **Epidemic Simulations:**
- Epidemic dynamics visualized through **plots of susceptible, infected, and recovered individuals**.
- Comparisons between **different graph structures and vaccination strategies**.
- **Real-world pandemic data validation**.

- **Graph Coloring:**
- **Potential function plots** demonstrate successful convergence to optimal coloring.
- **Final graph visualizations** for color assignments.

---

## Installation

To set up the project, ensure that you have Python installed (preferably Python 3.8 or later). Clone the repository and install the required dependencies:

```bash
git clone hhttps://github.com/taha-kms/Network-Dynamics-and-Learning.git
cd hw2
pip install -r requirements.txt
```
---

## File Structure
```bash
homework1/
│── ex1/                    # Exercise 1 solutions and code
│── ex2/                    # Exercise 2 solutions and code
│── homework3_report.pdf    # The report file
│── hw-3-2024_en.pdf
│── requirements.txt        # Dependencies
│── README.md               # Project documentation
```