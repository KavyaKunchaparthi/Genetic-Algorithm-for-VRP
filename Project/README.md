# Genetic Algorithm for Vehicle Routing Problem (VRP) 🚚🧬

A Python-based implementation of a **Genetic Algorithm (GA)** for solving the **Vehicle Routing Problem (VRP)** using the **DEAP evolutionary computation framework**. The project searches for efficient routes for multiple vehicles while minimizing total travel distance and penalizing imbalance between vehicle routes.

## 📌 Project Overview

The **Vehicle Routing Problem (VRP)** is a classical optimization problem in **Operations Research and Supply Chain Management**. The objective is to determine efficient routes for a fleet of vehicles serving multiple locations from a common depot.

In this project:

- 20 customer locations are randomly generated.
- A single depot is located at `(0, 0)`.
- 4 vehicles are used to serve the locations.
- A Genetic Algorithm is used to search for improved routing solutions.
- Candidate solutions are evaluated based on total travel distance and route balance.
- Matplotlib is used to visualize the resulting routes and fitness evolution.

The complete implementation is provided in a **Jupyter Notebook**.

## 🎯 Objectives

- Optimize routes for multiple vehicles.
- Minimize the total travel distance.
- Evaluate candidate solutions using a multi-objective fitness function.
- Reduce imbalance between vehicle route distances.
- Apply evolutionary operators to improve solutions over multiple generations.
- Visualize optimized routes and the evolution of fitness values.

## 🧬 Genetic Algorithm Approach

The project follows an evolutionary optimization process:

1. Generate an initial population of candidate routing solutions.
2. Represent each solution as a permutation of the customer locations.
3. Evaluate each candidate using the VRP fitness function.
4. Select better-performing individuals.
5. Apply crossover to generate new solutions.
6. Apply mutation to introduce variation.
7. Evaluate the new population.
8. Repeat the process over multiple generations.
9. Store the best solution using a Hall of Fame.
10. Visualize the resulting vehicle routes.

### Fitness Function

Each candidate solution is evaluated using two objectives:

- **Total travel distance** across all vehicles.
- **Route imbalance penalty**, calculated using the standard deviation of the individual vehicle route distances.

Both objectives are minimized.

## ⚙️ Genetic Algorithm Configuration

| Parameter | Value |
|---|---:|
| Number of locations | 20 |
| Number of vehicles | 4 |
| Depot | `(0, 0)` |
| Population size | 300 |
| Number of generations | 300 |
| Selection | Tournament Selection |
| Crossover | Partial-Mapped Crossover (PMX) |
| Mutation | Shuffle Index Mutation |
| Mutation probability per index | 0.05 |

The locations are randomly generated within the range `[-100, 100]` for both X and Y coordinates.

## 🛠️ Technologies Used

- **Python**
- **DEAP** – Evolutionary computation and Genetic Algorithm implementation
- **NumPy** – Numerical calculations and distance computation
- **Matplotlib** – Route and fitness visualization
- **Jupyter Notebook** – Interactive development and execution

## 📊 Results & Visualization

The notebook produces visualizations for analyzing the routing solution and optimization process.

### Optimized Routes

![Optimized Routes](images/optimized_routes.jpg)

*Visualization of the routes assigned to the vehicles.*

### Fitness Evolution

![Fitness Evolution](images/fitness_evolution.png)

*Fitness statistics across generations during the Genetic Algorithm optimization.*

## 📂 Project Structure

```text
Genetic-Algorithm-for-VRP/
│
├── Project/
│   ├── README.md
│   ├── requirements.txt
│   ├── vehicleRoutingProblem-Solution.ipynb
│   │
│   └── images/
│       ├── fitness_evolution.png
│       └── optimized_routes.jpg
│
└── .gitignore
