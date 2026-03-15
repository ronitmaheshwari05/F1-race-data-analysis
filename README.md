# 🏎️ F1 Race Data Analysis

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1ep1UziIRLkcXlDRFoijqOU7eITT-xsvv)

![Python](https://img.shields.io/badge/Python-Data%20Analysis-blue?logo=python)
![FastF1](https://img.shields.io/badge/FastF1-API-red)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-lightgrey)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-green)
![License](https://img.shields.io/badge/License-MIT-green)
![CI](https://github.com/ronitmaheshwari05/f1-race-data-analysis/actions/workflows/run-notebook.yml/badge.svg)

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

Additionally, the project builds a **data-driven performance ranking model** to estimate the best performing driver based on race pace metrics.

---

# 📓 Notebook

Main notebook:

**F1 Race Data Analysis.ipynb**

You can run the notebook directly in **Google Colab**.

Click the **Open in Colab** badge above.

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
- GitHub Actions (CI Pipeline)

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

The notebook follows a standard **data science workflow**.

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

### 5️⃣ Feature Engineering

Driver performance metrics calculated include:

- Average lap time  
- Fastest lap  
- Lap time consistency  

Drivers with very few laps are filtered out to ensure reliable statistics.

### 6️⃣ Feature Normalization

Metrics are normalized so different performance indicators can be compared fairly.

### 7️⃣ Driver Performance Model

A weighted **performance score** is calculated using:

- Average lap time  
- Fastest lap  
- Lap consistency  

Drivers are ranked based on the final score to estimate the **best performing driver in the race**.

### 8️⃣ Visualization

The notebook generates charts such as:

- Fastest lap comparison  
- Driver consistency analysis  
- Tyre strategy visualization  
- Driver performance ranking  

---

# 📈 Example Visualization

The notebook generates charts such as:

**Fastest Lap Comparison – Australian Grand Prix**

These visualizations help compare driver performance and race pace.

---

# 🤖 Performance Model

The project includes a **data-driven driver ranking model**.

The model evaluates driver performance using:

- Average race pace  
- Fastest lap performance  
- Lap time consistency  

These metrics are combined into a **weighted performance score** ranking drivers by overall race performance.

---

# 🚀 Future Improvements

Possible improvements for this project:

- Lap time prediction using Machine Learning  
- Multi-race season analysis across a championship  
- Using qualifying data to improve predictions  
- Interactive dashboards using Plotly or Streamlit  
- Race strategy simulation models  

---

# 👨‍💻 Author

**Ronit Maheshwari**  
BTech CSE (AI & ML)  
JECRC University, Jaipur  

GitHub:  
https://github.com/ronitmaheshwari05

---

# ⭐ Support the Project

If you found this project useful, please consider giving it a **⭐ star on GitHub**.

Stars help the project reach more developers and data science learners.

---

# 🤝 Contributing

Contributions are welcome.

If you'd like to improve the project you can:

- Fix bugs  
- Improve visualizations  
- Add new analysis  
- Improve documentation  
- Extend the performance model  

### Steps to contribute

1. Fork the repository  
2. Create a new branch

```bash
git checkout -b feature-improvement
```

3. Commit your changes

```bash
git commit -m "Add new analysis feature"
```

4. Push the branch

```bash
git push origin feature-improvement
```

5. Open a Pull Request

---

# 🐞 Issues

If you find a bug or have suggestions for improvements, please open an **Issue**.

You can report:

- Bugs  
- Data errors  
- Visualization improvements  
- Feature requests  

---

# 📜 License

MIT License

Copyright (c) 2026 Ronit Maheshwari

Permission is hereby granted, free of charge, to any person obtaining a copy  
of this software and associated documentation files (the "Software"), to deal  
in the Software without restriction, including without limitation the rights  
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell  
copies of the Software, and to permit persons to whom the Software is furnished  
to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all  
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR  
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,  
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE  
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER  
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,  
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
