# 🌫️ Machine-Learning-Classification-for-Jakarta-Air-Pollution-Monitoring
Random Forest classification model to predict air quality categories in DKI Jakarta using PySpark, with ETL, preprocessing, EDA, model evaluation, and visualization.
A complete Machine Learning pipeline using **PySpark** and **Random Forest Classifier** to predict **air quality categories** in DKI Jakarta.  

Source code is based on the uploaded file:  
➡️ `perkiraan_tingkat_polusi_dki_jakarta_dengan_random_forest_classifier.py` :contentReference[oaicite:1]{index=1}

---

## 📌 Project Overview

Air pollution in urban cities like Jakarta is influenced by multiple environmental variables.  
This project builds a **classification model** that predicts whether a day’s air quality is:

- **Aman (Good)**
- **Sedang (Moderate)**
- **Tidak Sehat (Unhealthy)**

The model uses pollutant indicators such as **PM10, PM2.5, SO₂, CO, O₃, NO₂**, and **location-based one-hot encoding**.



## 🧪 Dataset

Dataset dimuat dari Google Drive dalam format `.csv`, berisi kolom:

- `tanggal` — Date  
- `location` — Wilayah pengukuran  
- `pm10`, `pm25`, `so2`, `co`, `o3`, `no2` — Pollutant values  
- `max` — Maximum pollutant indicator  
- `quality` — Generated label (`aman`, `sedang`, `tidak sehat`)

Data undergoes transformation including:
- Null removal  
- Type casting  
- Date conversion  
- Label classification based on numeric ranges  
- Saving processed dataset to Parquet format


## 🧼 ETL & Data Cleaning

Main steps:

- Drop missing values  
- Convert `tanggal` into proper date format  
- Convert all pollutant columns into numeric columns  
- Create `quality` label using UDF based on `max` values  
- Save cleaned data for further use  

