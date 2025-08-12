# Event-Based Physical Risk Reporting

This repository contains the code and workflow used in the paper:

> **Beyond Single Company Climate Risk Disclosure: Event-Based Physical Risk Reporting**  
> *Environmental Research: Climate*, 2025.  
> DOI (paper): [https://doi.org/10.5281/zenodo.16812730](https://doi.org/10.5281/zenodo.16812730)

---

## Main Analysis

The notebook **`company_analysis.ipynb`** reproduces the main results of the paper. It:  
1. Loads and processes the given TC hazard event sets.  
2. Defines two fictional multinational companies with assets in multiple locations.  
3. Uses CLIMADA’s impact functions to estimate direct economic losses for each asset under each hazard event.  
4. Aggregates losses into **Event-Loss Tables (ELTs)**.  
5. Derives company-level and portfolio-level risk metrics (e.g., average annual loss, exceedance probability curves).  
6. Generates the figures and statistics reported in the paper.

---

### Hazard Event Sets

The tropical cyclone (TC) hazard event sets used in this work were generated with the **STORM** statistical model and processed into 2D wind fields at 150 arcsec (~4 km) resolution using the **Holland (2008)** parametric wind with the Tropical Cyclone Module in **CLIMADA**.  
The footprints represent maximum 1-minute sustained wind speeds (>34 knots) at each location over a storm’s lifetime.

Some referrences:  
- Bloemendaal, N. *et al.* (2020). *Generation of a global synthetic tropical cyclone hazard dataset using STORM*. **Sci. Data**. [https://doi.org/10.1038/s41597-020-0381-2](https://doi.org/10.1038/s41597-020-0381-2)  
- Bloemendaal, N. *et al.* (2022). *Impact of climate change on global tropical cyclone hazard*. **Sci. Adv.** [https://doi.org/10.1126/sciadv.abm8438](https://doi.org/10.1126/sciadv.abm8438)  
- Aznar-Siguan, G., Bresch, D.N. (2019). *CLIMADA: Probabilistic modelling of socio-economic impacts from natural hazards*. **Geosci. Model Dev.** [https://doi.org/10.5194/gmd-12-3085-2019](https://doi.org/10.5194/gmd-12-3085-2019)  

---

### Requirements

- Python ≥ 3.9  
- [CLIMADA](https://github.com/CLIMADA-project/climada_python) ≥ 4.1  
- NumPy, Pandas, Matplotlib, and other standard Python packages
