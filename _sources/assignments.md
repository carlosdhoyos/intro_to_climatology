# Assignments

## Cycle 1: Tropical Thermodynamics & Static Stability

### Instructions
- **Teams:** Work in pairs.  
- **Topic Selection:** By **Day 1** of Cycle 1, choose **one** of the three state-of-the-art topics below. Sign up on the shared spreadsheet.  
- **Timeline:**  
  - **Day 1:** Topic sign-up & kickoff  
  - **Day 3:** Submit 1-page project proposal  
  - **Day 7:** Interim check-in (5 min stand-up)  
  - **Day 14:** Final deliverables due  
- **Starter Code:** Use the provided notebook template to download and plot IGRA2 and ERA5 data.  
- **Collaboration:** Track your work in Git (one repo per team).  

### Topic Options

1. **MJO Preconditioning of Low-Level θₑ**  
   - **Objective:** Quantify boundary-layer θₑ anomalies leading active/inactive MJO phases.  
   - **Key Tasks:**  
     1. Download IGRA2 soundings (Darwin & Gan Island) for four MJO events.  
     2. Compute θ and θₑ profiles, derive daily anomalies vs. 1981–2010 climatology.  
     3. Composite low-level θₑ anomalies against TRMM/IMERG precipitation.  

2. **Decadal Trends in Tropical Static Stability**  
   - **Objective:** Detect trends in lapse rate (850–500 hPa) and CAPE over the eastern tropical Pacific (1960–2020).  
   - **Key Tasks:**  
     1. Extract lapse rate and CAPE from IGRA2 and ERA5.  
     2. Perform linear regression + Mann–Kendall tests.  
     3. Map spatial patterns and relate to ENSO indices.  

3. **Climatology of the Tropopause Inversion Layer (TIL)**  
   - **Objective:** Characterize TIL strength in the tropics and its relation to upper-tropospheric humidity.  
   - **Key Tasks:**  
     1. Identify TIL base/top in IGRA2 profiles (200–100 hPa).  
     2. Compute inversion strength and correlate with MERRA-2 humidity at 300–200 hPa.  
     3. Compare Pacific vs. Atlantic seasonal cycles.  

### Data & Tools
- **IGRA2 POR files:**  
  - Darwin (94703099999):  
    https://www.ncei.noaa.gov/data/integrated-global-radiosonde-archive/access/data-por/94703099999.dat.gz  
  - Gan Island (48647099999):  
    https://www.ncei.noaa.gov/data/integrated-global-radiosonde-archive/access/data-por/48647099999.dat.gz  
- **ERA5 monthly climatology:**  
  - CDS API, variables: temperature, specific humidity (levels 1000–100 hPa), years 1981–2010.  
- **Precipitation:** TRMM 3B42 V7 or GPM IMERG for MJO composite (Cycles 1 topic 1).  
- **Indices:** Wheeler–Hendon RMM index (NOAA PSL) for MJO phases; NINO3.4 (NOAA PSD) for ENSO.  
- **Python packages:**  
  - `pandas`, `xarray`, `metpy`, `cdsapi`  
  - `matplotlib`, `cartopy`  
  - (optional) `siphon` for IGRA2 requests  

### Deliverables
- **Jupyter Notebook** (`.ipynb`):  
  - Data download & parsing  
  - Computation of thermodynamic variables (θ, θₑ, lapse rate, CAPE, TIL metrics)  
  - Plots: T–p profiles, θ/θₑ vertical profiles, anomaly composites, trend maps, etc.  
  - Inline markdown explaining each step  
- **Presentation** (5 min + 2 min Q&A in class Week 3):  
  1. **Introduction**  
  2. **Data & Methods** (brief)  
  3. **Results & Interpretation**  
  4. **Conclusions & Future Work**  
  5. **References** (consistent style)  
  - Slide deck (max 5 slides) summarizing your question, methods, and key findings  

### Be Prepared To
- **Defend** your methodological choices (data selection, QC flags, analysis window).  
- **Discuss** limitations and possible extensions (e.g., alternative datasets, other basins).  
- **Propose** follow-up analyses based on your results.  

### 1. MJO Preconditioning of Low-Level θₑ  
**Scientific importance:**  
- The Madden–Julian Oscillation (MJO) is the dominant mode of tropical intra-seasonal variability, driving bursts of deep convection that modulate global weather (e.g., monsoons, midlatitude teleconnections).  
- Low-level equivalent potential temperature (θₑ) in the boundary layer reflects the reservoir of moist static energy available to fuel convection. Quantifying how θₑ anomalies lead or lag convective bursts is key to improving MJO prediction.  

**State-of-the-art aspects:**  
- Recent studies employ high-resolution reanalyses and satellite composites to pinpoint the preconditioning signals preceding active MJO phases (e.g., timing and vertical structure of θₑ buildup) and link them to moisture–convection coupling.  
- Advances in machine-learning MJO forecasts increasingly use θₑ composites as input features, but fundamental understanding of the physical lead-time remains an open research frontier.  

**References:**  
- Wheeler, M. C., & Hendon, H. H. (2004). *An all-season real-time multivariate MJO index: Development of an index for monitoring and prediction.* **Monthly Weather Review**, 132(8), 1917–1932. :contentReference[oaicite:0]{index=0}  
- Benedict, J. J., & Randall, D. A. (2007). *Observed characteristics of the MJO relative to maximum rainfall.* **Journal of the Atmospheric Sciences**, 64(12), 2332–2354. :contentReference[oaicite:1]{index=1}  


### 2. Decadal Trends in Tropical Static Stability  
**Scientific importance:**  
- Static stability (lapse rate between ~850 hPa and 500 hPa) controls the depth and vigor of tropical convection, influencing precipitation patterns, hurricane intensity, and large-scale circulation.  
- Detecting trends in stability under global warming directly tests climate-model projections that predict a “stability increase” in the free troposphere, which could modulate tropical rainfall and extreme events.  

**State-of-the-art aspects:**  
- While reanalyses and radiosondes now span 60+ years, significant uncertainties remain in trend magnitude and statistical robustness (e.g., homogenization issues, QC of early soundings).  
- Cutting-edge research uses advanced trend-detection methods (Mann–Kendall tests, Bayesian change-point analysis) and composite approaches to separate anthropogenic signals from natural variability (ENSO, volcanic aerosols).  

**References:**  
- Sobel, A. H. (2002). *The ENSO signal in tropical tropospheric temperature.* **Journal of Climate**, 15(18), 2702–2715. :contentReference[oaicite:2]{index=2}  
- Grise, K. M. (2010). *A global survey of static stability in the stratosphere and lower troposphere.* **Journal of Climate**, 23(9), 2333–2349. :contentReference[oaicite:3]{index=3}  

### 3. Climatology of the Tropopause Inversion Layer (TIL)  
**Scientific importance:**  
- The Tropopause Inversion Layer—an increase in temperature just below the cold-point tropopause—modulates stratosphere–troposphere exchange and the vertical distribution of water vapor, a powerful greenhouse gas.  
- Understanding TIL variability is crucial for accurately representing upper-tropospheric humidity in climate models, which strongly affects radiative forcing and stratospheric water vapor sources.  

**State-of-the-art aspects:**  
- Recent satellite (e.g., MLS, SABER) and high-resolution reanalysis products enable global mapping of TIL strength and height with unprecedented vertical resolution.  
- Current research focuses on linking TIL variability to deep-convection overshoots, gravity-wave breaking, and lower-stratospheric humidity trends under climate change.  

**References:**  
- Birner, T., Sankey, D., & Shepherd, T. G. (2006). *The tropopause inversion layer in models and analyses.* **Geophysical Research Letters**, 33(14), L14804. doi:10.1029/2006GL026549 :contentReference[oaicite:4]{index=4}  
- Pan, L. L., & Munchak, L. A. (2011). *Relationship of cloud top to the tropopause and jet structure from CALIPSO data.* **Journal of Geophysical Research**, 116, D12201. doi:10.1029/2010JD015462 :contentReference[oaicite:5]{index=5}  
