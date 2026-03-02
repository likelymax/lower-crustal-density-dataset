# Lower Crustal Density Lookup Tables  
## PIM-Based and CRUST1.0-Based Datasets

This repository provides the datasets accompanying:

Wang, Y. Russo, RM, Lin, Y (2025).
Lower crustal density: Method and uncertainty quantification.  
Bulletin of the Seismological Society of America.  
https://doi.org/10.1785/0220250233

These datasets support reproducible estimation of lower crustal density (ρ₁) and associated uncertainty using the methodology described in the paper.

---

# Dataset Overview

Two NetCDF datasets are included.

---

## 1. PIM-Based Dataset

**PIM = Parameter Inclusion Model**

The Parameter Inclusion Model (PIM) systematically samples a broad space of seismic and physical parameters at fixed intervals, including:

- Lower crustal P-wave velocity (alpha1)
- Lower crustal S-wave velocity (beta1)
- Upper mantle P-wave velocity (alpha2)
- Upper mantle S-wave velocity (beta2)
- Upper mantle density (rho2)
- Ray parameter (p)
- Ps/P amplitude ratio (ps_p)

The PIM dataset is theoretical and unconstrained. It does not impose restrictions from any specific Earth model and contains no embedded observational constraints. It provides a comprehensive parameter-space framework for evaluating method sensitivity, uncertainty behavior, and robustness.

File:
lcd_lookup_table_pim.nc

---

## 2. CRUST1.0-Based Lower Crustal Density Model

This dataset represents a physically constrained lower crustal density model generated using crustal velocity structure from CRUST1.0 (Laske et al., 2013).

CRUST1.0 is a global 1° crustal velocity model providing P-wave and S-wave velocities for layered crustal structure. In this dataset:

- Lower crustal velocities are extracted from CRUST1.0.
- These velocities are used within the density inversion framework described in Wang (2025).
- Lower crustal density (ρ₁) and associated uncertainty are computed accordingly.

Thus, this dataset represents a lower crustal density model derived from a globally averaged seismic velocity structure.

File:
lcd_lookup_table_crust1.nc

---

# File Format

Both datasets are provided in NetCDF (.nc) format.

Dimensions:
- alpha1
- beta1
- alpha2
- beta2
- p
- ps_p
- rho2

Variables:
- rho1 (g/cm³)
- uncertainty (g/cm³)

Data type:
- float32 with lossless compression

---

# Citation

If you use these datasets, please cite:

Wang, Y. Russo, RM, Lin, Y (2025).
Lower crustal density: Method and uncertainty quantification.  
Bulletin of the Seismological Society of America.  
https://doi.org/10.1785/0220250233

Dataset DOI (Zenodo): https://doi.org/10.5281/zenodo.18842173

---

# Version

Current release: v1.0.0 (2025)

This version corresponds to the datasets used in Wang (2025), BSSA.
