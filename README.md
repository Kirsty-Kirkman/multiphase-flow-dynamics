# Porous Media Flow Dynamics: Buckley-Leverett & Spontaneous Imbibition Solver

This repository contains a comprehensive suite of computational models designed to simulate multiphase flow in porous media. The project focuses on two fundamental phenomena in reservoir engineering and subsurface hydrology:

- **Buckley-Leverett displacement** (viscous-dominated)
- **Spontaneous Imbibition** (capillary-driven)

---

# Project Overview

The solvers simulate fluid transport under varying wettability conditions and phase combinations, providing critical insights into saturation front development and recovery efficiencies. These models are highly relevant for modern energy applications, including:

- Carbon Capture and Storage (CCS)
- Subsurface Hydrogen Storage
- Enhanced Oil Recovery (EOR)

---

# Key Features

## Buckley-Leverett Solver

- Analytical and numerical (Explicit Finite Difference) solutions
- Immiscible displacement across three distinct fluid-rock systems

## Spontaneous Imbibition Model

Capillary-driven flow modeling using similarity variables:

$$
\omega = \frac{x}{\sqrt{t}}
$$

Solves the non-linear diffusion equation.

## Wettability Profiles

Comparative analysis of:

- Water-wet systems
- Mixed-wet systems
- Gas-wet systems

Using specialized relative permeability models.

## Interactive Visualization

Detailed Jupyter notebooks demonstrating:

- Shock fronts
- Rarefaction waves
- Diffusive saturation profiles

---

# Detailed Case Studies

## Case 1: CO₂ Injection into an Aquifer (Primary Drainage)

Models the displacement of water by CO₂.

**Characteristics:**

- High CO₂ mobility
- Small shock front
- Significant rarefaction region

---

## Case 2: Water Displacing Hydrogen (Secondary Imbibition)

Models a strongly water-wet system.

**Characteristics:**

- All-shock behavior
- Water mobilizes after critical saturation

---

## Case 3: Mixed-Wet Scenario

Analyzes altered wettability systems.

**Characteristics:**

- Inflection in fractional flow
- Rarefaction + shock profile

---

# Repository Structure

```
/notebooks
│── 01_CO2_Injection_Primary_Drainage.ipynb
│── 02_Water_Hydrogen_Displacement.ipynb
│── 03_Water_CO2_Mixed_Wet_System.ipynb
│── 04_Spontaneous_Imbibition_Model.ipynb

/output
│── Plots
│── Comparisons
```

---

# Theoretical Background

## Buckley-Leverett Equation

$$
\frac{\partial S_w}{\partial t_D} +
\frac{df_w}{dS_w}
\frac{\partial S_w}{\partial x_D} = 0
$$

Shocks resolved with **Welge construction**.

## Spontaneous Imbibition

$$
S_w = \Phi(\omega),
\quad
\omega = \frac{x}{\sqrt{t}}
$$

---

# Requirements

- Python 3.x
- NumPy
- Matplotlib
- SciPy
- Jupyter

---

# Usage

## Clone

```bash
git clone https://github.com/Kirsty-Kirkman/multiphase-flow-dynamics.git
```

## Explore

Open notebooks in `/notebooks`.

## Run

Modify:
- viscosities
- rel perms

Observe saturation behaviour.

---

# References

Blunt (2017) *Multiphase Flow in Permeable Media*

Buckley & Leverett (1942)

---

# License

MIT License.
