# 5G-Wave-Propagation-Analysis
This project analyzes environmental and spatial factors influencing 5G signal strength (Received_Power_dBm).
## 📊 Dataset Overview
The analysis is based on the [5G Wave Channel Prediction Dataset](https://www.kaggle.com/datasets/zoya77/5g-wave-channel-prediction-dataset/data) from Kaggle.

It includes 1,000 samples of 5G wave propagation data:
- **Spatial Coordinates:** Tx/Rx positions (x, y, z)
- **Signal Metrics:** Distance, LOS/NLOS Flag, Shadowing (dB), Angle of Arrival/Departure
- **Environment:** Temperature, Humidity, and Blockage Events
- **Target Variable:** `Received_Power_dBm`

## 🚀 Key Findings
- **Dominant Features:** Distance and Shadowing are the primary drivers of path loss.
- **Model Evolution:**
  - Initial Random Forest: $R^2 = 0.9776$
  - Gradient Boosting (XGBoost): $R^2 = 0.9848$
  - **Pruned Model (Top 5 Features):** $R^2 = 0.9870$ | MAE: 0.3229 dBm
- **Insights:** Removing "noisy" features like Humidity and Temperature improved model robustness and reduced overfitting.

## 🛠️ Installation & Usage

### Local Setup
To run the analysis locally, clone the repo and install the dependencies:
```bash
git clone [https://github.com/aliallouf/5G-Wave-Propagation-Analysis.git](https://github.com/aliallouf/5G-Wave-Propagation-Analysis.git)
cd 5G-Wave-Propagation-Analysis
pip install -r requirements.txt
