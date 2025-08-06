# Tropical Thermodynamics & Static Stability

---

## Lecture 1: Atmospheric Composition & Vertical Structure

### 1.1 Composition and Mean Molecular Weight

- Dry air is a mixture, by volume, of  

  $$
  X_{N_2} \approx 0.7808,\quad
  X_{O_2} \approx 0.2095,\quad
  X_{Ar} \approx 0.0093,\quad
  \text{(plus ~0–4% H₂O by volume).}
  $$

- Universal gas constant:  

  $$
  R_u = 8.314462618\,\mathrm{J\,mol^{-1}K^{-1}}
  $$

- Mean molecular weight of dry air:

  $$
  M_d = \sum_i X_i\,M_i
      = 0.7808\,(28.0134) + 0.2095\,(31.9988) + 0.0093\,(39.948)
      \approx 28.9647\,\mathrm{g/mol}
  $$

- Dry-air gas constant:

  $$
  R_d = \frac{R_u}{M_d/1000}
      \approx \frac{8.314}{0.0289647}
      \approx 287.05\,\mathrm{J\,kg^{-1}K^{-1}}
  $$

---

### 1.2 Hydrostatic Balance

- Vertical force balance in a stationary atmosphere:

  $$
  dp = -\rho\,g\,dz
  $$

- Ideal-gas law for dry air:

  $$
  p = \rho\,R_d\,T
  \quad \Rightarrow \quad
  \rho = \frac{p}{R_d\,T}
  $$

- Substitute into hydrostatic balance:

  $$
  \frac{dp}{dz} = -\frac{p}{R_d\,T}\,g
  \quad \Rightarrow \quad
  \frac{dp}{p} = -\frac{g}{R_d\,T}\,dz
  $$

- **Isothermal layer** ($T = \text{const}$):

  $$
  \int_{p_0}^{p(z)} \frac{dp'}{p'} = -\frac{g}{R_d\,T} \int_0^z dz'
  \quad \Rightarrow \quad
  p(z) = p_0\,\exp\left(-\frac{z}{H}\right)
  $$

- Scale height:

  $$
  H = \frac{R_d\,T}{g} \approx \frac{287\,T}{9.81} \ \mathrm{m}
  $$

---

### 1.3 Density Profile

- From ideal gas:

  $$
  \rho(z) = \frac{p(z)}{R_d\,T} = \rho_0\,e^{-z/H}
  $$

- **Examples:**
  - Tropics ($T \approx 300$ K): $H \approx 8.78$ km  
  - Poles ($T \approx 250$ K): $H \approx 7.30$ km

---

## Lecture 2: Thermodynamic Processes & Lapse Rates

### 2.1 First Law of Thermodynamics for a Parcel

- First law per unit mass:

  $$
  dQ = c_p\,dT - \alpha\,dp,
  \quad \alpha = \frac{1}{\rho}
  $$

- **Dry adiabatic process** ($dQ = 0$):

  $$
  c_p\,dT = \frac{1}{\rho}\,dp = R_d\,T\,\frac{dp}{p}
  $$

- Leading to the dry adiabatic lapse rate:

  $$
  \frac{dT}{dz} = -\frac{g}{c_p}
  \quad \Rightarrow \quad
  \Gamma_d = -\frac{dT}{dz} = \frac{g}{c_p} \approx \frac{9.81}{1005} \approx 9.8\,\mathrm{K\,km^{-1}}
  $$

---

### 2.2 Moist (Saturated) Adiabatic Lapse Rate

- In saturated conditions (latent heating):

  $$
  dQ = L_v\,dq_s = c_p\,dT - \alpha\,dp
  $$

- The moist adiabatic lapse rate is:

  $$
  \Gamma_m = -\frac{dT}{dz}
           = \frac{g}{c_p}
             \cdot \frac{1 + \frac{L_v\,q_s}{R_d\,T}}{1 + \frac{L_v^2\,q_s}{c_p\,R_v\,T^2}}
  $$

- **Typical values in the tropics**:  
  $\Gamma_m \approx 4$–6 K km⁻¹

---

### 2.3 Virtual Temperature Correction

- Virtual temperature:

  $$
  T_v = T\,(1 + 0.61\,q)
  $$

- Modified ideal gas law:

  $$
  \rho = \frac{p}{R_d\,T_v}
  $$

- Buoyancy of a parcel:

  $$
  b = g\,\frac{T_v' - T_v}{T_v}
  $$

---

## Lecture 3: Potential Temperature, Static Stability & Brunt–Väisälä

### 3.1 Potential Temperature $\theta$

- Defined as:

  $$
  \theta = T\,\left(\frac{p_0}{p}\right)^{R_d/c_p}
  $$

- In dry adiabatic motion ($dQ=0$), $\theta$ is conserved:

  $$
  d\ln \theta = 0
  $$

---

### 3.2 Equivalent Potential Temperature $\theta_e$

- Includes moisture effect:

  $$
  \theta_e \approx \theta\,\exp\left(\frac{L_v\,r_s}{c_p\,T}\right)
  $$

---

### 3.3 Static Stability and Brunt–Väisälä Frequency

- Defined as:

  $$
  N^2 = \frac{g}{\theta}\,\frac{d\theta}{dz}
  $$

- Interpretation:
  - $N^2 > 0$: stable (parcel oscillates)
  - $N^2 < 0$: unstable (parcel rises or sinks)

- **Typical values**:
  - Tropical troposphere: $N \sim 0.01$–0.02 s⁻¹  
  - Stratosphere: $N \sim 0.02$–0.05 s⁻¹

---
