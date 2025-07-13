# Wind-Speed-Analysis-for-Renewable-Energy-at-Indian-Airports-Using-Statistical-techniques

This project analyzes wind speed data from Indian airports to evaluate the feasibility of renewable energy generation using statistical modeling.

📘 Overview
This research project investigates the feasibility of integrating wind energy systems at Indian airports, especially those located in coastal and open plain regions. With India aiming for net-zero carbon emissions by 2070, renewable energy sources like wind and solar become crucial. While solar has already seen significant adoption at airports, this study focuses on wind energy as a complementary and continuous power source—particularly useful during monsoon months when solar power is inconsistent.

The study applies statistical modeling using Weibull and Lower-Upper Truncated Weibull Distributions to analyze wind speed data and estimate potential power generation. The data spans over 7 years (2017–2023) and covers 11 airports, with 3 shortlisted based on wind speed and data quality: Porbandar, Rajkot, and Tuticorin.

🎯 Objectives
1.Model wind speed distributions using Weibull and Truncated Weibull distributions.

2.Evaluate the energy generation potential of wind at selected Indian airports.

3.Estimate power output using fitted distributions and energy density equations.

4.Assess the feasibility of Savonius Vertical Axis Wind Turbines (VAWT) for deployment.

📍 Data Collection & Preprocessing
Source: METAR (Meteorological Aerodrome Reports) from Iowa State University's Website.

Time Frame: 2017–2023 (7 years of daily wind speed data with records present for every 30 seconds timeframe).

Locations: 11 Indian airports (e.g., Porbandar, Rajkot, Tuticorin, Chennai, Kolkata).

#Preprocessing Steps:
Converted wind speed from knots to m/s.

Focused on monsoon months (June–September) where wind energy can supplement solar.

Imputed missing values using ARIMA modeling.

Filtered stations based on average wind speed (>3 m/s) and positive skewness.

📊 Methodology
1. 📈 ARIMA Modeling
Used to forecast and impute missing daily wind speed values by leveraging temporal seasonality and trends.

2. 🧮 Maximum Likelihood Estimation (MLE)
Used to estimate parameters (shape, scale) of:
Weibull Distribution
Truncated Weibull Distribution (limits: 3 m/s ≤ WS ≤ 10 m/s)

3. ✅ Goodness-of-Fit Tests
Kolmogorov-Smirnov (KS) Test: Compared empirical and theoretical CDFs.
Akaike Information Criterion (AIC): Lower AIC indicates a better fitting model.
✅ Finding: Truncated Weibull Distribution consistently outperformed the standard Weibull model across most months and airports, particularly for Porbandar.

4. ⚡ Mean Energy Density
Calculated using Mean energy density formula.


🔋 Energy Use Cases:
Ground Support Equipment (GSE)
EV charging stations
Runway and external lighting
Backup power systems

⚠️ Limitations
Results are airport-specific; further validation needed for generalization.
Site-specific turbine design, height, and positioning constraints must be assessed.
Only AIC and KS test used for model evaluation—other statistical tests could strengthen conclusions.

🔭 Future Scope
Explore alternate distributions (Gamma, Rayleigh, Lognormal) for better wind speed modeling.
Use wind rose diagrams for optimizing turbine placement.
Consider long-term wind pattern shifts due to climate change.
