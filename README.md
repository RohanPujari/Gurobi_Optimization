# Gurobi Optimization – Exploring the Capacitated Vehicle Routing Problem (CVRP)

This repository is a hands-on exploration of optimization using **Gurobi Optimizer**, focused on understanding and modeling the **Capacitated Vehicle Routing Problem (CVRP)**.

The intention of this project is learning and experimentation rather than building a fully optimized or production-ready system. The work here reflects my attempt to understand how real-world routing problems can be translated into mathematical models and solved using a professional optimization solver.

---

## Project Overview

The Capacitated Vehicle Routing Problem (CVRP) is a classic optimization problem in operations research. In this problem:

- There is a depot where vehicles start and end their routes  
- A set of customers, each with a known demand  
- A fleet of vehicles, each with limited carrying capacity  
- The objective is to serve all customers exactly once while minimizing total travel distance  

This problem appears in many real-world applications such as logistics, supply chain planning, and delivery routing.

---

## Dataset Used

The project uses instances from the **SVRP-Bench** dataset, which provides realistic vehicle routing benchmarks.

From the dataset, I worked with:
- Customer and depot locations represented as 2D coordinates  
- Demand values for each customer  
- Vehicle capacity information  
- Fleet size for each routing instance  

The focus was primarily on **small CVRP instances** to make the modeling process easier to reason about and debug.

---

## What I Implemented

The core of this project is the formulation of a CVRP model using Gurobi. The work includes:

- Loading and inspecting SVRP-Bench data using Python  
- Converting raw dataset fields into solver-friendly structures  
- Computing distance matrices from location coordinates  
- Defining decision variables to represent vehicle routing choices  
- Formulating an objective function to minimize total travel distance  
- Adding core constraints such as:
  - Each customer must be visited exactly once  
  - Vehicles must respect capacity limits  
  - Routes must start and end at the depot  

Rather than optimizing solver performance, the emphasis was on understanding how each modeling decision affects feasibility and correctness.

---

## Challenges Encountered

A significant part of this project involved debugging and refining the model. Some of the challenges I faced include:

- Handling indexing errors when working with multi-dimensional decision variables  
- Dealing with shape mismatches in dataset fields such as demands and vehicle capacities  
- Correctly identifying and handling the depot within the dataset  
- Defining helper variables to track vehicle load without violating constraints  

Resolving these issues required iterating on the model, reshaping data structures, and rethinking how constraints were expressed.

---

## Scope and Limitations

This project intentionally stays within a limited scope:

- Only small problem instances were explored  
- Solver parameter tuning was not performed  
- Advanced heuristics and performance optimizations were not included  
- The focus was on model formulation rather than scalability  

The goal was clarity and correctness, not speed or large-scale optimization.

---

## Why This Project

Optimization problems often sound abstract until you try to implement one. This project helped me better understand:

- How real-world decisions translate into mathematical constraints  
- Why careful data handling matters in optimization models  
- How solvers like Gurobi approach complex decision problems  

It served as a practical introduction to optimization modeling and solver-based thinking.

---

## Potential Next Steps

Some natural extensions to this work could include:

- Scaling the model to larger CVRP instances  
- Adding solver tuning and performance improvements  
- Supporting multi-depot routing scenarios  
- Introducing time windows or stochastic elements  
- Improving visualization of optimized routes  

---

## Finally:

This repository reflects a learning journey into mathematical optimization using Gurobi. It captures both the progress made and the challenges encountered while building a CVRP model from real benchmark data. The project is intended to be approachable for anyone interested in understanding how optimization works in practice.
