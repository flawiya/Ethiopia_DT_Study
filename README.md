Ethiopia Agricultural Drought Reanalysis (2000 - 2025)
High-Resolution District-Level Drought Monitoring for Parametric Insurance
📌 Project Objective
This study provides a high-resolution (ADM2/District level) agricultural drought analysis for Ethiopia, specifically focusing on the Kiremt rains (June–September) which support the critical Meher harvest. The goal is to develop and validate the Agricultural Reanalysis Index (ARI)—a multi-indicator tool designed to reduce "Basis Risk" in parametric insurance by integrating atmospheric demand, soil moisture supply, and thermal stress.
🛠 Methodology & Indices
The analysis processes 25 years of climate and satellite data to calculate five distinct drought dimensions:
1. Standardized Precipitation Index (SPI-3)
Data: CHIRPS (5km resolution).
Method: Fits 3-month rolling rainfall to a Gamma Distribution.
Key Feature: Includes the Thom Adjustment to handle "Zero-Rain" months in arid regions like Afar, ensuring mathematical validity in probability scores.
2. Standardized Precipitation Evapotranspiration Index (SPEI-3)
Data: CHIRPS (Rainfall) - ERA5-Land (PET).
Method: Measures Climatic Water Balance (D=P−PET) fitted to a Log-Logistic (Fisk) Distribution.
Significance: Identifies "Flash Droughts" driven by extreme heat rather than just rainfall deficits.
3. Standardized Soil Index (SSI-3)
Data: ERA5-Land Root-zone soil moisture (7–28 cm).
Method: Standardizes the actual water available to plant roots against historical baselines.
Insight: Used to identify the 1-2 month lag between atmospheric drought and physical agricultural impact.
4. Satellite Health Indices (VCI, TCI, VHI)
VCI (Vegetation Condition Index): Normalizes NDVI greenness.
TCI (Thermal Condition Index): Measures Land Surface Temperature (LST) stress.
VHI (Vegetation Health Index): A 50/50 blend of moisture and temperature stress.
5. Agricultural Reanalysis Index (ARI) - The "Master" Trigger
The study evolves through three integrated iterations:
IADI: 0.4 × SPEI + 0.6 × SSI (Balanced Atmosphere/Soil).
IASI: 0.2 × SPEI + 0.3 × SSI + −0.5 × TCI_Z (Heavily weighted for thermal stress).
ARI (Final): Rolling3M(0.2×SPEI+0.5×SSI_Root+0.3×TCI_Z).
📈 Key Findings & Results
1. Heat is the Primary Driver
Correlation analysis reveals that Land Surface Temperature (LST) has a significantly stronger negative impact on plant health (-0.79) than rainfall has a positive impact (0.57). This justifies the high weight given to thermal stress in the ARI.
2. Validation via ROC Analysis
Indices were tested against "Ground Truth" disaster years (2002, 2009, 2011, 2015, 2021, 2022).
ARI Accuracy (AUC): 0.798
SPI Accuracy (AUC): 0.769
Insight: The ARI provides a 3% accuracy gain over traditional rainfall-only models, significantly reducing the risk of insurance "misses."
3. Moral Hazard vs. Basis Risk
While satellite indices (VCI) show the highest correlation with crop death, they carry Moral Hazard (cannot distinguish between drought and poor farming).
The ARI is identified as the superior insurance trigger because it measures the Weather Driver (Environmental Stress) rather than the Biological Outcome, making it fraud-resistant.
🖥️ Outputs Included
The analysis generates the following visualizations and datasets:
Temporal Drought Matrix (Heatmap): A year-by-district breakdown of SPI-3 for September.
Water Balance "Scissors" Plot: Visualizing the deficit between Precipitation and PET.
Consolidated ROC Curve: Comparing the predictive power of all indices.
SSI vs SPEI Lag Plot: Showing how soil moisture follows atmospheric trends.
Interactive Folium Map: A multi-layer HTML map allowing spatial toggling of ARI, SPI, SPEI, and VHI across Ethiopia.
🚀 Technical Requirements
Language: Python 3.x
Libraries: geopandas, pandas, scipy (for Gamma/Fisk fitting), matplotlib, seaborn, sklearn (for ROC/AUC), folium.
Data Structure: Requires a master_df.csv containing columns for precip_mm, pet_mm, soil_7_28cm, ndvi, and lst_c.
📚 References
Vicente-Serrano et al. (2010): SPEI Methodology.
Funk et al. (2015): CHIRPS Data Usage.
Thom (1966): Gamma distribution adjustments for zero-rainfall.
Vroege et al. (2021): Satellite support for crop insurance.
