# Event-Based Physical Risk Reporting

This repository contains the code and workflow used in the paper:

> **Beyond Single Company Climate Risk Disclosure: Event-Based Physical Risk Reporting**  
> *Environmental Research: Climate*, 2025.  
> DOI (paper): [10.1088/2752-5295/adf912](https://doi.org/10.1088/2752-5295/adf912)

---

## Main Analysis

The notebook **`company_analysis.ipynb`** reproduces the main results of the paper. It:  
1. Loads and processes the TC hazard event sets.  
2. Defines two fictional multinational companies with assets in multiple locations.  
3. Uses CLIMADA’s impact functions to estimate direct economic losses for each asset under each hazard event.  
4. Aggregates losses into **Event-Loss Tables (ELTs)**.  
5. Derives company-level and portfolio-level risk metrics (e.g., average annual loss, exceedance probability curves).  
6. Generates the figures and statistics reported in the paper.

---

## Hazard Event Sets

The tropical cyclone (TC) hazard event sets used in this work were generated with the **STORM** statistical model and processed into 2D wind fields at 150 arcsec (~4 km) resolution using the **Holland (2008)** parametric wind model in **CLIMADA**.  
The footprints represent maximum 1-minute sustained wind speeds (>34 knots) at each location over a storm’s lifetime.

Methodology details can be found in:  
- Kropf, C.M. *et al.* (2025). *A global probabilistic hazard dataset for tropical cyclones in present and future climates*. **Nature Climate Change**. [https://doi.org/10.xxxx/s41558-024-02194-w](https://doi.org/10.xxxx/s41558-024-02194-w)  
- Bloemendaal, N. *et al.* (2020). *A globally consistent local-scale probabilistic tropical cyclone hazard dataset*. **Sci. Data**. [https://doi.org/10.1038/s41597-020-0381-2](https://doi.org/10.1038/s41597-020-0381-2)  
- Bloemendaal, N. *et al.* (2022). *Impact of climate change on global tropical cyclone hazard*. **Sci. Adv.** [https://doi.org/10.1126/sciadv.abm8438](https://doi.org/10.1126/sciadv.abm8438)  
- Aznar-Siguan, G., Bresch, D.N. (2019). *CLIMADA: Probabilistic modelling of socio-economic impacts from natural hazards*. **Geosci. Model Dev.** [https://doi.org/10.5194/gmd-12-3085-2019](https://doi.org/10.5194/gmd-12-3085-2019)  
- CLIMADA Tropical Cyclone Module (2023). Zenodo. [https://doi.org/10.5281/zenodo.8383171](https://doi.org/10.5281/zenodo.8383171)

---

## Requirements

- Python ≥ 3.9  
- [CLIMADA](https://github.com/CLIMADA-project/climada_python) ≥ 4.1  
- [SALib](https://salib.readthedocs.io/) v1.4.5  
- NumPy, Pandas, Matplotlib, and other standard Python packages

---

## How to Reproduce the Paper’s Results

1. Clone this repository.  
2. Install dependencies (`pip install -r requirements.txt`).  
3. Download or generate the hazard event sets.  
4. Run `company_analysis.ipynb`.
