# 🏎️ F1 Race Data Analysis

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1ep1UziIRLkcXlDRFoijqOU7eITT-xsvv)

![Python](https://img.shields.io/badge/Python-Data%20Analysis-blue?logo=python)
![FastF1](https://img.shields.io/badge/FastF1-API-red)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-lightgrey)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-green)
![License](https://img.shields.io/badge/License-MIT-green)

---

# 📊 Formula 1 Race Data Analysis with FastF1

This project performs **Formula 1 race data analysis using Python and the FastF1 API**.

The notebook loads official **F1 timing and telemetry data** and performs exploratory data analysis (EDA) to understand race performance and driver behavior.

The analysis focuses on extracting insights from:

- Driver lap times  
- Fastest laps  
- Race pace comparison  
- Tyre strategies  
- Telemetry speed analysis  

---

# 📓 Notebook

Main notebook:

**F1 Race Data Analysis.ipynb**

You can run the notebook directly in **Google Colab**:

👉 Click the **Open in Colab** badge above.

---

# 🧰 Technologies Used

This project uses the following technologies:

- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  
- FastF1 API  
- Jupyter Notebook / Google Colab  

---

# 📂 Data Source

Race data is retrieved using the **FastF1 API**, which provides access to:

- Lap timing data  
- Telemetry data  
- Driver information  
- Session results  
- Race schedules  

The FastF1 library collects data from Formula 1 live timing services and presents it as **Pandas DataFrames for analysis**.

---

# 🔎 Analysis Workflow

The notebook follows a standard **data science workflow**:

### 1️⃣ Install Required Libraries

```python
!pip install fastf1 pandas numpy matplotlib seaborn
```

### 2️⃣ Import Libraries

```python
import fastf1
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
```

### 3️⃣ Load Race Data

```python
session = fastf1.get_session(2026, "Australia", "R")
session.load()
```

### 4️⃣ Data Cleaning

Convert lap time to seconds for analysis.

```python
laps["LapTime_sec"] = laps["LapTime"].dt.total_seconds()
```

### 5️⃣ Fastest Lap Analysis

Group data to find the fastest lap per driver.

### 6️⃣ Visualization

Generate charts such as:

- Fastest lap comparison
- Driver consistency plots
- Race pace visualization

---

# 📈 Example Visualization

The notebook generates charts like:

**Fastest Lap Comparison – Australian Grand Prix**

These visualizations help compare driver performance during the race.

---

# 🚀 Future Improvements

Possible improvements for this project:

- Lap time prediction using Machine Learning  
- Multi-race season analysis  
- Interactive dashboards using Plotly or Streamlit  
- Race strategy simulation  

---

# 👨‍💻 Author

**Ronit Maheshwari**  
BTech CSE (AI & ML)  
JECRC University, Jaipur  

---

# ⭐ Acknowledgements

Race data is provided by the **FastF1 API**, which gives access to official Formula 1 telemetry and timing data.

---

# 📜 License

This project is licensed under the **MIT License**.
