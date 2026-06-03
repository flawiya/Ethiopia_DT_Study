# AgriRisk-Africa 🌽☀️
**Multi-Scalar Drought Reanalysis & Parametric Insurance Modeling**

AgriRisk-Africa is a specialized geospatial pipeline designed to quantify agricultural drought risk across African districts. By merging satellite rainfall (CHIRPS), climate reanalysis (ERA5-Land), and crop calendars (GEOGLAM), the system calculates high-resolution drought indices used to design parametric insurance payouts.

## 🚀 Key Features
*   **Multi-Scalar Indices**: Implementation of SPI (Precipitation), SPEI (Evapotranspiration), and SSI (Soil Moisture) using Gamma-CDF and Log-Logistic transformations.
*   **Risk Window Analysis**: Automatically filters data based on crop-specific growing seasons (e.g., Kiremt rains in Ethiopia).
*   **Insurance Modeling**: ROC Analysis to validate indices against historical disaster years (EM-DAT).
*   **Interactive Visualizations**: Animated drought maps (Plotly) and multi-layer district stress maps (Folium).
*   **Teleconnection Mapping**: District-to-district correlation matrices to understand synchronized drought risk.

## 📁 Repository Structure
*   `analysis/`: Main drought reanalysis scripts (Ethiopia & Africa-wide).
*   `utils/`: Geospatial pre-processing (GADM clipping, coordinate alignment).
*   `data/`: (Local only) Directory for GADM .gpkg, CHIRPS, and ERA5 CSVs.
*   `outputs/`: Generated HTML maps, correlation matrices, and CSV results.

## 🛠️ Installation
1. Clone the repo:
   ```bash
   git clone https://github.com/your-username/AgriRisk-Africa.git
   cd AgriRisk-Africa
