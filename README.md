# M/M/1 Queue Simulation Toolkit

A collection of Python scripts for simulating the classic **M/M/1 queue** – a single‑server queue with exponential inter‑arrival and service times.  
The project demonstrates both **theoretical** and **experimental** performance measures (L, Lq, W, Wq) and provides interactive visualisations.

##  Files

| File | Description |
|------|-------------|
| `MM1‑Simulation.py` | **Full PyQt5 GUI** with animated queue evolution, theoretical vs experimental comparison, convergence analysis, and distribution plots. |
| `MM1.py` | Alternative PyQt5 GUI focusing on detailed statistical tables, Little’s Law verification, and multiple distribution histograms. |
| `simulation.py` | Ultra‑simple console simulation that prints step‑by‑step event traces for a small number of clients. |
| `TPSimul.py` | Basic script that manually calculates waiting times using sorted arrival times. |

All scripts share the same core model but are written with different pedagogical goals – from a **quick demonstration** to a **full‑featured teaching tool**.

##  Features

- **Event‑driven simulation** using random exponential distributions.
- **Real‑time visualisation** of queue length evolution.
- **Side‑by‑side comparison** of theoretical formulas with experimental results.
- **Little’s Law verification** and error analysis.
- **Convergence analysis** showing how experimental values approach theory as the number of customers grows.
- Clean, modern GUI with multiple tabs and styling (in the main scripts).

##  Theoretical Background

The M/M/1 queue is governed by:

- Arrival rate **λ**, service rate **μ** (both Poisson processes)
- Utilisation **ρ = λ / μ** (must be < 1 for stability)

| Measure | Formula |
|---------|---------|
| Avg customers in system (L) | L = ρ / (1 - ρ) |
| Avg customers in queue (Lq) | Lq = ρ² / (1 - ρ) |
| Avg time in system (W) | W = 1 / (μ - λ) |
| Avg waiting time (Wq) | Wq = ρ / (μ - λ) |

##  Quick Start

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/MM1-Queue-Simulation-Toolkit.git
   cd MM1-Queue-Simulation-Toolkit
