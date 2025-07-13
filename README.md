# 🌬️ Wind Speed Analysis for Renewable Energy at Indian Airports

This project analyzes wind speed data from Indian airports to evaluate the feasibility of wind energy generation using statistical modeling techniques. With India aiming for net-zero carbon emissions by 2070, renewable energy integration at airports—especially wind energy as a supplement to solar—is an emerging necessity. This project explores the viability of using Savonius Vertical Axis Wind Turbines (VAWTs) by modeling wind speed distributions and estimating potential energy output.

---

## ❓ Why This Project?

India’s aviation sector is expanding rapidly, increasing its energy demands. While solar panels are already installed at several airports, their efficiency drops drastically during monsoon months. This motivated us to explore **wind energy as a consistent and complementary source**. Airports located near coastlines or open plains have favorable wind conditions. Inspired by Mumbai Airport’s hybrid SolarMill system, we aimed to evaluate wind energy’s potential using a statistical approach.

---

## 📂 From Where is the Data Taken?

- **Source**: METAR (Meteorological Aerodrome Reports) from **Iowa State University**
- **Time Frame**: 2017–2023
- **Airports**: 11 airports including Porbandar, Rajkot, Tuticorin, Chennai, Kolkata, etc.
- **Frequency**: Wind speed observations recorded every 30 seconds
- **Key Variables Used**: `valid` (timestamp), `sknt` (wind speed), `lat`, `lon`

---

## 📘 Project Description

We conducted a statistical analysis of wind speed data from 11 Indian airports. Based on average wind speed and skewness, three airports—**Porbandar**, **Rajkot**, and **Tuticorin**—were shortlisted. Wind speed distributions were modeled using **Weibull** and **Truncated Weibull Distributions**, and energy output was estimated. Finally, feasibility of **Savonius VAWTs** for airport-scale deployment was evaluated.

---

## 🎯 Objectives

1. Model wind speed using Weibull and Truncated Weibull distributions.
2. Estimate wind energy output using statistical distributions.
3. Evaluate the suitability of Savonius VAWTs at airports.
4. Suggest wind-based renewable energy as a supplement to solar.

---

## 🧹 Data Preprocessing

- Converted wind speed from knots to m/s
- Focused on monsoon months (June–September)
- Imputed missing values using **ARIMA modeling**
- Shortlisted airports with:
  - Mean wind speed > 3 m/s
  - Positive skewness in data

---

## 📊 Methodology

### 1. ARIMA Modeling
- Used to impute missing values by modeling seasonal and trend components
- Auto ARIMA (`auto.arima()`) was used for time series forecasting

### 2. Maximum Likelihood Estimation (MLE)
- Used to estimate shape (`k`) and scale (`c`) parameters for:
  - **Weibull Distribution**
  - **Truncated Weibull Distribution** (range: 3–10 m/s)

### 3. Goodness-of-Fit Testing
- **Kolmogorov–Smirnov (KS) Test**
- **Akaike Information Criterion (AIC)**

✅ *Truncated Weibull consistently provided better fits, especially for Porbandar.*

### 4. Mean Energy Density Estimation

**Used Formula:**

`P_D = 0.5 × ρ × c³ × Γ(1 + 3/k)`

Where:
- `ρ` = Air density (1.225 kg/m³)
- `c` = Scale parameter
- `k` = Shape parameter

This was extended to estimate power output using turbine area, efficiency, and time.

---

## ⚡ Key Findings

| Month     | Porbandar (kWh) | Rajkot (kWh) | Tuticorin (kWh) |
|-----------|------------------|---------------|------------------|
| June      | 86.3             | 58.9          | 40.0             |
| July      | 85.4             | 51.2          | 56.9             |
| August    | 64.1             | 44.7          | 40.1             |
| September | 39.0             | 25.3          | 17.6             |

> A 3-turbine setup at Porbandar could generate ~**259.2 kWh/month** from wind alone, similar to Mumbai’s SolarMill system.

---

## 🔋 Applications

- EV Charging Stations  
- Ground Support Equipment (GSE)  
- Runway and Perimeter Lighting  
- Backup Power Systems  
- Reduction in dependency on grid power

---

## ⚠️ Limitations

- Site-specific results may not generalize to other locations
- Only AIC and KS test were used for validation
- Real-world turbine placement, design, and infrastructure not fully modeled

---

## 🔭 Future Scope

- Explore alternate distributions: **Rayleigh**, **Gamma**, **Lognormal**
- Use **Wind Rose Diagrams** to optimize turbine placement based on directionality
- Analyze long-term wind shifts due to climate change

---

## 👥 Team

| Name             | Roll No. | SAP ID       |
|------------------|----------|--------------|
| Aayushi Fariya   | A018     | 86062400043  |
| Jainam Gada      | A019     | 86062400025  |
| Drishti Shah     | A064     | 86062400034  |
| Payal Shah       | A065     | 86062400040  |
| Harshita Warang  | A074     | 86062400031  |

**Project Supervisor**: Dr. Pradnya Khandeparkar  
Nilkamal School of Mathematics, Applied Statistics & Analytics  
SVKM’s NMIMS, Mumbai

---

## 📚 References

1. [Truncated Weibull Distribution – ScienceDirect](https://www.sciencedirect.com/science/article/pii/S235248472400307X)  
2. [Iowa State University METAR Dataset](https://mesonet.agron.iastate.edu/request/download.phtml)  
3. [SolarMill Hybrid System – ACI Asia-Pacific](https://www.aci-asiapac.aero/)  
4. [SUGAM Report – AAI India](https://www.aai.aero/sites/default/files/aaiupload/SUGAM__Web_Version.pdf)  
5. Various research articles from Springer, IEEE, ResearchGate

---
