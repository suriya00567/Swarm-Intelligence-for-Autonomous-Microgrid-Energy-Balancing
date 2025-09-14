# Renewable Energy Storage Optimization using Particle Swarm Optimization (PSO)

This project investigates the application of **Particle Swarm Optimization (PSO)** to minimize the mismatch between renewable energy generation and consumption by optimizing energy storage utilization.

## Overview

* **Objective:** Reduce mismatch between energy production and consumption.
* **Approach:** Apply PSO to optimize storage dispatch across multiple nodes.
* **Dataset:** Includes energy generation, consumption, storage capacity, and efficiency.
* **Evaluation Metrics:**

  * Absolute mismatch (L1 error)
  * Squared mismatch (L2 error)

## Results

* **Baseline absolute mismatch:** \~33.52M MWh
* **Optimized mismatch:** reduced by \~14,930 MWh (0.045% improvement)
* **Squared mismatch:** no significant improvement due to dominance of large imbalances
* **Key Insight:** PSO converges stably, but the small storage capacity (\~4% of demand scale) limits improvement.

## Visualizations

* Generation vs. Consumption trends
* Baseline vs. Optimized mismatch comparison
* Per-node improvements after optimization

## Future Work

* Evaluate larger storage capacity scenarios
* Explore alternative optimization algorithms (Genetic Algorithms, Ant Colony Optimization, Differential Evolution)
* Introduce cost and reliability-based objectives
* Extend to temporal (multi-period) optimization

## Tools and Technologies

* Python
* NumPy, Pandas, Matplotlib
* PySwarms

This project investigates the use of Particle Swarm Optimization (PSO) to address one of the fundamental challenges in renewable energy systems: the mismatch between energy generation and consumption. Renewable sources such as solar and wind are inherently intermittent, creating periods of surplus production and deficit consumption. Energy storage systems are introduced to mitigate these imbalances, but their limited capacity requires intelligent allocation strategies to maximize effectiveness.

The objective of this work is to optimize the utilization of storage capacity across multiple nodes using PSO, a population-based stochastic optimization technique inspired by the social behavior of birds and fish. Each particle in the swarm represents a candidate allocation of storage across the network. Through iterative updates based on cognitive and social learning factors, the swarm converges toward solutions that minimize system-wide mismatch.

The dataset includes values for generation, consumption, storage capacity, and storage efficiency. The optimization was tested on a sample of 200 nodes. Two evaluation metrics were considered: absolute mismatch (L1 error) and squared mismatch (L2 error). Absolute mismatch captures total imbalance, while squared mismatch penalizes extreme deviations more heavily.

Results indicate that PSO reduced the absolute mismatch from 33.52 million MWh to 33.51 million MWh, representing an improvement of approximately 14,930 MWh (0.045%). Squared mismatch, however, did not show improvement, as large imbalances dominate this metric and overshadow the small corrections achievable with limited storage. These outcomes demonstrate that while PSO successfully converges and identifies feasible improvements, the impact is constrained by the relatively small storage capacity (approximately 4% of average generation and load).

The findings highlight two important insights: first, optimization techniques such as PSO are effective tools for storage dispatch problems; second, system-level improvements require adequate storage scale. Future work may involve scaling up storage capacity, experimenting with alternative optimization algorithms (e.g., Genetic Algorithms, Ant Colony Optimization), incorporating cost or reliability objectives, and extending the framework to temporal optimization across multiple periods.

Overall, this project provides a proof-of-concept demonstration of applying swarm intelligence to renewable energy optimization, with practical insights into the constraints and opportunities of real-world deployment.
