# Tropical Thermodynamics & Static Stability

---

## Lecture 1: Atmospheric Composition & Vertical Structure

### 1.1 Composition and Mean Molecular Weight

- Dry air is a mixture, by volume, of  
  \[
    X_{N_2}\approx0.7808,\quad
    X_{O_2}\approx0.2095,\quad
    X_{Ar}\approx0.0093,
    \quad\text{(plus ~0–4% H₂O by volume).}
  \]
- Universal gas constant: \(R_u = 8.314462618\,\mathrm{J\,mol^{-1}K^{-1}}\).  
- Mean molecular weight of dry air:
  \[
    M_d = \sum_i X_i\,M_i
         = 0.7808\,(28.0134) + 0.2095\,(31.9988)
           + 0.0093\,(39.948) \approx 28.9647\ \mathrm{g/mol}.
  \]
- Dry-air gas constant:
  \[
    R_d = \frac{R_u}{M_d/1000}
        \approx \frac{8.314}{0.0289647}
        \approx 287.05\ \mathrm{J\,kg^{-1}K^{-1}}.
  \]

### 1.2 Hydrostatic Balance

- Vertical force balance in a stationary atmosphere:
  \[
    dp = -\rho\,g\,dz.
  \]
- Ideal-gas law for dry air:
  \[
    p = \rho\,R_d\,T
    \quad\Longrightarrow\quad
    \rho = \frac{p}{R_d\,T}.
  \]
- Substitute into hydrostatic:
  \[
    \frac{dp}{dz} = -\frac{p}{R_d\,T}\,g
    \quad\Longrightarrow\quad
    \frac{dp}{p} = -\frac{g}{R_d\,T}\,dz.
  \]
- **Isothermal layer** (\(T=\) constant):
  \[
    \int_{p_0}^{p(z)}\!\frac{dp'}{p'}
    = -\frac{g}{R_d\,T}\int_0^z dz'
    \quad\Longrightarrow\quad
    p(z)=p_0\,\exp\!\Bigl(-\tfrac{z}{H}\Bigr),
  \]
  where the **scale height** is
  \[
    H = \frac{R_d\,T}{g}
      \approx \frac{287\,T}{9.81}\ \mathrm{m}.
  \]

### 1.3 Density Profile

- Since \(\rho=p/(R_dT)\), for isothermal:
  \[
    \rho(z)=\rho_0\,e^{-z/H}.
  \]
- **Example:**  
  - Tropics: \(T\approx300\,\mathrm K\) → \(H\approx8.78\ \mathrm{km}\).  
  - Poles: \(T\approx250\,\mathrm K\) → \(H\approx7.30\ \mathrm{km}\).  

---

## Lecture 2: Thermodynamic Processes & Lapse Rates

### 2.1 First Law of Thermodynamics for a Parcel

- First law per unit mass:
  \[
    dQ = c_p\,dT - \alpha\,dp,
    \quad
    \alpha = \frac{1}{\rho}.
  \]
- **Dry adiabatic** (\(dQ=0\)):
  \[
    c_p\,dT = \alpha\,dp
    = \frac{1}{\rho}\,dp
    = R_d\,T\;\frac{dp}{p},
  \]
  using \(dp/p = d\rho/\rho + dT/T\).  But directly:
  \[
    \frac{dT}{dz}
    = -\frac{g}{c_p}
    \quad\Longrightarrow\quad
    \Gamma_d = -\frac{dT}{dz}
             = \frac{g}{c_p}
             \approx \frac{9.81}{1005}
             \approx 9.8\ \mathrm{K\,km^{-1}}.
  \]

### 2.2 Moist (Saturated) Adiabatic Lapse Rate

- When saturated, latent heating enters:
  \[
    dQ = L_v\,dq_s
        = c_p\,dT - \alpha\,dp.
  \]
- Using Clapeyron relation for saturation mixing ratio \(q_s\) and rearranging (see e.g. Emanuel 1994):
  \[
    \Gamma_m
    = -\frac{dT}{dz}
    = \frac{g}{c_p}
      \frac{1 + \dfrac{L_v\,q_s}{R_d\,T}}
           {1 + \dfrac{L_v^2\,q_s}{c_p\,R_v\,T^2}}.
  \]
- Typical values in tropics:  
  \(\Gamma_m\approx4\)–6 K km⁻¹ (vs. dry 9.8 K km⁻¹).

### 2.3 Virtual Temperature Correction

- Virtual temperature \(T_v\) accounts for moisture:
  \[
    T_v = T\,(1 + 0.61\,q),
    \quad
    \rho = \frac{p}{R_d\,T_v}.
  \]
- Buoyancy of a parcel:
  \[
    b = g\,\frac{T_v' - T_v}{T_v}.
  \]

---

## Lecture 3: Potential Temperature, Static Stability & Brunt–Väisälä

### 3.1 Potential Temperature \(\theta\)

- Defined as temperature a parcel would have if brought adiabatically to reference pressure \(p_0\) (usually 1000 hPa):
  \[
    \theta = T
      \Bigl(\frac{p_0}{p}\Bigr)^{R_d/c_p}.
  \]
- From dry adiabat \(dQ=0\), one shows \(d\ln\theta=0\).

### 3.2 Equivalent Potential Temperature \(\theta_e\)

- Adds latent heat of moisture:
  \[
    \theta_e \approx \theta
      \exp\!\Bigl(\frac{L_v\,r_s}{c_p\,T}\Bigr),
  \]
  where \(r_s\) is saturation mixing ratio at \((p,T)\).

### 3.3 Static Stability and Brunt–Väisälä Frequency

- Define stability via vertical gradient of \(\theta\):
  \[
    N^2
    = \frac{g}{\theta}\frac{d\theta}{dz}.
  \]
- Interpretation:
  - \(N^2>0\): stable (parcel displaced returns).  
  - \(N^2<0\): unstable (convective overturning).  
- Typical values:  
  - Tropical troposphere: \(N\sim0.01\)–0.02 s⁻¹.  
  - Stratosphere: \(N\sim0.02\)–0.05 s⁻¹.

---
