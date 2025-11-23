# 📊 Smart City IoT Sensors – Exploratory Data Analysis (EDA)

---

### 🧭 Project Overview  
This repository contains an Exploratory Data Analysis (EDA) of IoT sensor data collected for a **Smart City digital ecosystem** project.

> **Grant Reference:**  
> **BR24992852** – *“Intelligent models and methods of Smart City digital ecosystem for sustainable development and the citizens’ quality of life improvement.”*

The data consists of **measurements taken every 5 seconds for 7 days** using IoT sensors connected to an **ESP Arduino microcontroller**. The microcontroller transmitted data via HTTP to a local server, which saved each **day as a separate CSV file** (~17,280 records/day).

---

### 🧪 Sensors Used

| Sensor | Purpose |
|-------|---------|
| Temperature | Air temperature (°C) |
| Humidity | Relative humidity (%) |
| Light | Light intensity (arbitrary units) |
| pH | Acidity level |
| Electrical Conductivity (EC) | Water/medium conductivity |

📌 Each CSV contains **17,280 readings (5-second intervals)**.  
📌 Total dataset size: **~120,960 records across 7 days.**

---

## 📁 Project Structure

```text
smart-city-iot-eda/
├─ data/
│  ├─ sensor_data_2025-03-01.csv
│  ├─ sensor_data_2025-03-02.csv
│  ├─ sensor_data_2025-03-03.csv
│  ├─ sensor_data_2025-03-04.csv
│  ├─ sensor_data_2025-03-05.csv
│  ├─ sensor_data_2025-03-06.csv
│  └─ sensor_data_2025-03-07.csv
├─ figures/
│  ├─ temp_humidity_light_timeseries.png
│  ├─ temp_vs_humidity_scatter.png
│  ├─ sensor_correlation_heatmap.png
│  └─ light_day1_24h.png
├─ notebooks/
│  └─ 01_iot_sensors_eda.ipynb
├─ EDA_SmartCity_Report.pdf
└─ README.md
```

---

## 🚀 How to Run the Notebook

### Option 1 – **Jupyter Notebook (Anaconda / VS Code)**
```bash
git clone <your-repository-link>
cd smart-city-iot-eda
jupyter notebook notebooks/01_iot_sensors_eda.ipynb
```

### Option 2 – **Google Colab**
Upload the notebook and dataset, then modify:
```python
DATA_DIR = "."
# Change to "data" if CSV files are in a subfolder:
# DATA_DIR = "data"
```

---

## 🔍 EDA Tasks

We performed the following analysis:

✔️ Load & merge CSV files  
✔️ Add **date & hour** from timestamps  
✔️ Check **missing values**  
✔️ Compute **statistics (mean, min, max, variance)**  
✔️ Time-series: temp, humidity & light  
✔️ Investigate **day–night patterns (light sensor)**  
✔️ Scatter analysis: **temperature vs humidity**  
✔️ Correlation heatmap for all sensors  

---

## 📊 Sample Outputs

### 📈 1. Time-Series Trend  
![Time Series](figures/temp_humidity_light_timeseries.png)

### 🌞 2. Day–Night Light Cycle (Day 1)  
![DayLight](figures/light_day1_24h.png)

### 🔁 3. Temperature vs Humidity (Scatter)  
![Scatter](figures/temp_vs_humidity_scatter.png)

### 🔗 4. Correlation Heatmap  
![Heatmap](figures/sensor_correlation_heatmap.png)

---

## 🧠 Conclusion

| Finding | Conclusion |
|--------|-------------|
| Missing values | None found |
| Sensor ranges | Realistic & stable |
| Patterns | Weak or random |
| Correlations | Very low (independent sensors) |
| Dataset use | Good for **simulation & modeling** |

---

## 📌 Next Steps (Suggestions)

✔️ Forecast temperature using LSTM / Prophet  
✔️ Perform anomaly detection  
✔️ Compare with real-world data  
✔️ Simulate sensor faults for testing edge cases  
✔️ Deploy on Streamlit / Flask dashboard

---

## 📂 Project Files

📄 **EDA Notebook (Jupyter):**  
`notebooks/01_iot_sensors_eda.ipynb`

📘 **PDF Summary Report:**  
`EDA_SmartCity_Report.pdf`

---

## 👨‍💻 Author  
Project work completed as part of **Continuous Assessment**.  
Smart City IoT | Exploratory Data Analysis | Python | Data Science  

---

### ⭐ If this project helped you — make sure you star 🌟 the repo!
