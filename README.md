# Stochastic Queueing Systems: Performance Analysis & Simulation

This repository contains a comprehensive discrete-event simulation (DES) framework developed to model and analyze service systems (specifically bank queues). The project progresses from basic system modeling to advanced statistical decision-making.

## Academic Context & Language Note
These projects were originally developed for the **Introduction to Computational Engineering** undergraduate course. 
* To ensure global accessibility, this README and the repository structure are in **English**. 
* However, to comply with the original academic grading requirements, the internal source code variables, inline comments, chart axis labels, and the detailed PDF reports are written in **Turkish**. 

---

## Repository Structure

```text
stochastic-queueing-simulation/
│
├── project_1_single_server/
│   ├── bank_sim_p1.py          # M/M/1 Queue Simulation Code
│   └── report_p1.pdf           # Problem definition and modeling report
│
├── project_2_multi_server/
│   ├── bank_sim_p2.py          # M/M/1 vs. M/M/2 Comparison Code
│   └── report_p2.pdf           # Statistical decision making report
│
├── plots/                      # Visual outputs (boxplots, bar charts)
├── requirements.txt            # Project dependencies
└── README.md
`````


  
## Phase 1: Discrete Event Simulation (Single Server)

Located in Project 1 — Single Server. The objective of this phase is to model a real-world service system in a computer environment using a pure event-based algorithm.

    * System: Single bank teller (M/M/1 Queue).

    * Parameters: Exponentially distributed interarrival times (λ=5 min) and service times (μ=4 min).

    * Output: Calculates raw waiting times, queue lengths, and visualizes the distribution for 100 customers.

## Phase 2: Alternative System Comparison (Decision Support)

Located in Project 1 — Multi-Server. This phase evolves the simulation into a Decision Support System. It evaluates whether the high utilization and variance of a single-server system justify the investment in a second server.

    * System: Comparison between Single Teller (M/M/1) and Dual Teller (M/M/2) architectures sharing a common FIFO queue.

    * Methodology: 20 independent runs for 200 customers to ensure statistical reliability.

    * Key Performance Indicators (KPIs): Average waiting time, time spent in the system, queue length, and server utilization rate.

    * Conclusion: Demonstrates mathematically how adding a second server drastically reduces wait-time variance and stabilizes the system.

## Technologies Used

    * Python 3 (Core simulation logic built without external simulation frameworks like SimPy, demonstrating a deep understanding of event loops).

    * NumPy (Random variate generation from exponential distributions).

    * Pandas (Data structuring and tabular result formatting).

    * Matplotlib (Data visualization, boxplots, and performance comparisons).

## How to Run

**Clone the repository and install the required dependencies:**
* Bash

* git clone [https://github.com/your-username/stochastic-queueing-simulation.git](https://github.com/your-username/stochastic-queueing-simulation.git)
* cd stochastic-queueing-simulation
* pip install -r requirements.txt

Then, you can run the individual scripts located in their respective project folders.
