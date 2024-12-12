# Simulating an M/M/1 Queueing System with Python and SimPy

## Purpose
This project demonstrates how to simulate an $$\(M/M/1\)$$ queueing system using the **SimPy** library in Python. It provides an illustrative example for:
1. Using SimPy to model, simulate, and monitor a queueing system.
2. Comparing simulated performance metrics with theoretical values derived from queueing theory.

The project serves as an educational tool to learn about discrete-event simulation and queueing system analysis.

## Overview

### **What is an \(M/M/1\) Queue?**
An \(M/M/1\) queue is a single-server queue where:
- **Arrivals** follow a **Poisson process** (exponentially distributed interarrival times).
- **Service times** are exponentially distributed.
- There is a **single server**, and the queue operates on a **first-come, first-served** basis.

## Theoretical Formulas

For an $$\(M/M/1\)$$ queue with arrival rate $$\lambda$$ and service rate $$\mu$$, we have that the average waiting time and average queue size are given by:

$$
T_q = \frac{\lambda}{\mu (\mu - \lambda)}
$$

$$
L_q = \frac{\lambda^2}{\mu (\mu - \lambda)}
$$

The formulas assume the system operates under steady-state conditions $$\lambda < \mu$$, and they are well known in the queuing theory literature. We will use these formulas and compared them to the results obtained via simulation. 
