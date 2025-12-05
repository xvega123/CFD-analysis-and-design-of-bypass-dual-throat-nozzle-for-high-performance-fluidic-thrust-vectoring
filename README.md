# CFD Analysis and Design of Bypass Dual Throat Nozzle (BDTN) via XAI & Optimization

> **Research Overview & Supplementary Material**
> 
> *This repository serves as an archive for the research methodology and key findings presented in our paper on fluidic thrust vectoring optimization.*

---

## Abstract
This project investigates the design optimization of a **Bypass Dual Throat Nozzle (BDTN)** to maximize high-performance fluidic thrust vectoring. 

By integrating **Computational Fluid Dynamics (CFD)** with **Explainable AI (SHAP)** and **Gaussian Process Regression (GPR)**, we established a robust framework that reconciles the trade-off between thrust efficiency ($C_f$) and flow deflection angle ($\delta$). The study successfully identifies optimal geometric parameters that significantly enhance vectoring capabilities without compromising thrust performance.

**Paper Reference:**
> **C. Park**, W. Lee, S. Choi, "CFD analysis and design of bypass dual throat nozzle for high-performance fluidic thrust vectoring," *Advances in Engineering Software*, Vol. 201, 103827, 2025.

---

## Key Methodologies

### 1. Parametric CFD Simulation
* **Solver:** ANSYS Fluent (Compressible RANS, Realizable $k-\epsilon$ model).
* **Validation:** Verified against experimental data for NPR 3 conditions.
* **Design Space:** 8 geometric parameters ($\theta_1, \theta_2, \theta_3, \theta_4, d_2, d_3, d_4, l_1$) were analyzed using Latin Hypercube Sampling (LHS).

### 2. Explainable AI (XAI) with SHAP
We applied **SHAP (SHapley Additive exPlanations)** values to quantify the sensitivity of geometric parameters.
* **Insight:** The analysis revealed that the upstream and downstream throat heights ($d_2, d_3$) are the most critical factors influencing both thrust and vectoring performance.

### 3. Surrogate-Based Optimization
* **Modeling:** A Multivariate Gaussian Process Regression (GPR) model was trained to predict nozzle performance.
* **Optimization:** Used a Multi-Objective Genetic Algorithm (NSGA-II) to derive the **Pareto Front**, identifying optimal designs that balance conflicting objectives.

---

## Key Findings
The data-driven optimization process yielded design candidates with superior performance compared to the baseline geometry:

* **Deflection Angle ($\delta$):** Improved by up to **12.83%** (Max $\approx 31.04^\circ$).
* **Thrust Efficiency ($C_f$):** Maintained or slightly improved (+0.7%) relative to the baseline.

| Metric | Baseline | Optimized (Max Angle) | Improvement |
| :--- | :---: | :---: | :---: |
| Deflection Angle ($\delta$) | $\approx 27.5$° | **31.04°** | **+12.83%** |
| Thrust Ratio ($C_f$) | 0.975 | **0.973** | Comparable |

*[Insert Figure: Pareto Front or Mach Number Contours from the paper here]*

---

## Citation
For more details, please refer to our published work:

```bibtex
@article{PARK2025103827,
title = {CFD analysis and design of bypass dual throat nozzle for high-performance fluidic thrust vectoring},
journal = {Advances in Engineering Software},
volume = {201},
pages = {103827},
year = {2025},
issn = {0965-9978},
doi = {https://doi.org/10.1016/j.advengsoft.2024.103827},
url = {https://www.sciencedirect.com/science/article/pii/S0965997824002345},
author = {Chanho Park and Woochan Lee and Seongim Choi},
keywords = {Bypass dual throat nozzle, Sensitivity analysis, Data-driven optimization},
}

## Code Availability
The source code for this project is available upon request. Please contact the author via email for access.
