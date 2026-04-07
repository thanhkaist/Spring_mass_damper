# Spring–Mass–Damper Control Simulation

This repository contains simple Python simulations of a **spring–mass–damper** system controlled with:

- a **PD controller** (`PD.py`)
- a **PID controller** (`PID.py`)

Both scripts numerically integrate the system dynamics using a 4th-order Runge–Kutta (RK4) solver and visualize the tracking error over time.

## Model Summary

The mechanical plant is modeled as:

$$
m\ddot{x} + c\dot{x} + kx = F
$$

where:

- `m` = mass (kg)
- `c` = damping coefficient (N·s/m)
- `k` = spring constant (N/m)
- `F` = control force (N)

Controller gains (`kp`, `ki`, `kd`) and simulation settings are currently defined directly in each script.

## Repository Structure

```text
.
├── PD.py   # PD control simulation
└── PID.py  # PID control simulation
```

## Requirements

- Python 3.8+
- NumPy
- Matplotlib

Install dependencies:

```bash
pip install numpy matplotlib
```

## Usage

From the repository root:

### Run PD simulation

```bash
python PD.py
```

### Run PID simulation

```bash
python PID.py
```

Each script opens a Matplotlib window showing the position error response versus time.

## Notes

- The scripts are designed for experimentation and educational use.
- To test different control behavior, modify gain values and simulation parameters in the corresponding file.
