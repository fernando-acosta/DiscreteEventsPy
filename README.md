# Simulating an M/M/1 Queueing System with Python and SimPy

## Purpose
This project demonstrates how to simulate an \(M/M/1\) queueing system using the **SimPy** library in Python. It provides an illustrative example for:
1. Using SimPy to model, simulate, and monitor a queueing system.
2. Comparing simulated performance metrics with theoretical values derived from queueing theory.

The project serves as an educational tool to learn about discrete-event simulation and queueing system analysis.

---

## Overview

### **What is an \(M/M/1\) Queue?**
An \(M/M/1\) queue is a single-server queue where:
- **Arrivals** follow a **Poisson process** (exponentially distributed interarrival times).
- **Service times** are exponentially distributed.
- There is a **single server**, and the queue operates on a **first-come, first-served** basis.

### **Simulation Workflow**
1. **Customer Arrival Process**:
   - Customers arrive at random intervals based on an exponential distribution.
2. **Customer Process**:
   - Each customer waits in the queue until the server is available.
   - Once served, the customer leaves the system.
3. **Queue Monitoring**:
   - The system logs the queue size and time whenever a customer arrives or departs.

---

## Features

### **Key Components**
1. **MonitoredResource**:
   - A subclass of SimPy's `Resource`, which tracks queue sizes during requests and releases.
2. **Customer Lifecycle**:
   - Simulates customer arrivals, waiting times, and service times.
3. **Metrics Comparison**:
   - Theoretical metrics:
     - Average waiting time (\( T_q \)).
     - Average queue size (\( L_q \)).
   - Simulated metrics based on the monitored data.

### **Visualization**
- A **step plot** shows how the queue size evolves over time.

---

## Theoretical Formulas

For an \(M/M/1\) queue with:
- **Arrival rate** (\( \lambda \)).
- **Service rate** (\( \mu \)).

1. **Average Waiting Time (\( T_q \))**:
   \[
   T_q = \frac{\lambda}{\mu (\mu - \lambda)}
   \]
   This represents the expected time a customer spends in the queue before service.

2. **Average Queue Size (\( L_q \))**:
   \[
   L_q = \frac{\lambda^2}{\mu (\mu - \lambda)}
   \]
   This represents the average number of customers waiting in the queue.

The formulas assume the system operates under steady-state conditions (\( \lambda < \mu \)).

---

## Installation and Usage

### **Requirements**
- Python 3.x
- Libraries:
  - NumPy
  - Matplotlib
  - SimPy

Install dependencies using:
```bash
pip install numpy matplotlib simpy
