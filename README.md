# AgriRisk-Africa 🌽☀️
**Multi-Scalar Drought Reanalysis & Parametric Insurance Modeling**

## 📖 Introduction
Agriculture in Africa is over 90% rainfed, making it highly vulnerable to climate-driven shocks. This project provides a high-resolution drought monitoring pipeline that moves beyond simple rainfall tracking. By integrating **CHIRPS satellite rainfall**, **ERA5-Land reanalysis**, and **GEOGLAM crop calendars**, we calculate standardized indices to identify "Flash Droughts" and soil moisture deficits that lead to crop failure.

## 🎯 Objectives
The primary goal of this study is to reduce **Basis Risk** (the gap between index triggers and actual crop loss) in parametric insurance:
1.  **Multi-Scalar Monitoring**: Calculate SPI (Rainfall), SPEI (Water Balance), and SSI (Soil Moisture) at the district level (Admin 2).
2.  **Integrated Modeling**: Develop the **Agricultural Reanalysis Index (ARI)**—a weighted composite index ($20\% SPEI + 50\% SSI + 30\% TCI$).
3.  **Validation**: Use ROC (Receiver Operating Characteristic) analysis to test index accuracy against historical disaster years (EM-DAT).
4.  **Spatial Correlation**: Map teleconnections between districts to help insurers diversify their risk portfolios.
