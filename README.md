# Earth-Mars Orbital Transfer

2D three-body simulation (Sun, Earth, Mars) of an Earth-to-Mars transfer trajectory written in Python for a Computational Physics course at the University of Granada.

## Overview

The spacecraft trajectory is integrated with a 4th-order Runge-Kutta (RK4) method in astronomical units (AU, solar masses, years). The notebook covers:

- **Trans-Mars injection ($\Delta V_1$):** Hohmann-like transfer velocity combined with Earth escape velocity from the edge of Earth's sphere of influence.
- **Launch window sensitivity:** Sweeps over Mars' initial phase angle ($\phi_0$) to find the minimum approach distance and viable capture windows ($< 0.05\ \text{AU}$).
- **Energy vs. time-of-flight trade-off:** Computes the insertion burn ($\Delta V_2$) and compares total $\Delta V$ against transit time across valid launch angles.
- **Outputs:** Generates trajectory animations (`.gif`), phase diagrams, and sensitivity/cost plots.

## Sample Results

![Mars Transfer Animation](figures/mars_mission_phi_0.790.gif)
![Launch Window Sensitivity](figures/initial_phase_sweep_inset.png)
![Energy vs Time of Flight](figures/energy_cost_analysis.png)

## Requirements

- Python 3
- `numpy`
- `matplotlib`
- `pillow` (only needed to export animations as GIF)

## Usage

Open `earth_mars_transfer.ipynb` in Jupyter Notebook or VS Code and run the cells sequentially.
