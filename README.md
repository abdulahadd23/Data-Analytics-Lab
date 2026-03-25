# 📊 Data Analytics Lab — Spring 2026

A hands-on laboratory project covering the full data analytics workflow in Python — from initial environment configuration through numerical computing, data wrangling, and a complete visualization portfolio. Each module builds on the previous one, progressing from foundational skills to real-world analytical techniques.

---

## 📁 Repository Layout

```
Data-Analytics-Lab/
│
├── lab 1/                        # Module 1: Setup & Foundations
│   └── Lab_01_Environment_Setup.ipynb
│
├── lab 2/                        # Module 2: Python for Data Processing
│   └── Lab_02_Python_Fundamentals.ipynb
│
├── lab 3/                        # Module 3: Numerical Computing
│   └── Lab_03_NumPy_Computing.ipynb
│
├── lab 4/                        # Module 4: Data Exploration & Cleaning
│   └── Lab_04_Pandas_Data_Wrangling.ipynb
│
├── lab 5/                        # Module 5: Visualization Portfolio
│   └── Lab_05_Visualization_Portfolio.ipynb
│
├── .gitignore
└── README.md                     # Project Documentation
```

---

## 🔧 Module 1: Environment Setup & Foundations (Lab 1)

The opening module establishes a fully configured development environment for data science work.

### 🔹 Setup Tasks

- **Anaconda Distribution:** Installation and verification of Python, `conda`, and Jupyter Notebook
  - Verification: `python --version`, `conda --version`
- **Google Colab:** Alternative cloud-based execution without local installation
- **Library Stack:** Installation of core analytics libraries

| Library | Purpose |
|---------|---------|
| **Pandas** | Tabular data manipulation and analysis |
| **NumPy** | High-performance numerical computation |
| **Matplotlib** | Static, animated, and interactive plotting |
| **Seaborn** | Statistical data visualization layer on Matplotlib |

### 🔹 First Notebook

- Arithmetic, string, list, and dictionary operations in Python
- Industry use case survey across healthcare, finance, retail, manufacturing, education, and transportation
- Bar chart visualization of analytics adoption rates by sector
- GitHub repository initialization and first commit

---

## 🐍 Module 2: Python Data Structures & File I/O (Lab 2)

This module covers the Python fundamentals needed for professional data processing pipelines.

### 🔹 Core Topics

- **Data Structures:** Working with Lists, Dictionaries, Tuples, and Sets for organized data storage
- **Functional Programming:** Writing modular, reusable functions for grade classification, statistical analysis, and data validation
- **File I/O Operations:** Reading and writing across multiple formats
  - CSV: Sales transaction records with `csv.DictReader` / `csv.writer`
  - JSON: Structured student records with `json.load()` / `json.dump()`
  - Plain Text: Lab report generation and text analysis
- **List Comprehensions:** Efficient one-liner transformations with performance benchmarking against traditional loops
- **Error Handling:** `try-except` blocks, custom exceptions (`DataValidationError`), safe type conversion patterns

### 🔹 Exercise Dataset
Student grades and product sales records (CSV + JSON)

---

## 🔢 Module 3: Numerical Computing with NumPy (Lab 3)

High-performance numerical computing applied to simulated financial market data from the Pakistan Stock Exchange.

### 🔹 Practical Tasks

1. **Array Creation:** Building and inspecting 1D, 2D, and 3D arrays with `np.zeros`, `np.ones`, `np.eye`, `np.linspace`, `np.arange`
2. **Indexing & Reshaping:** Slicing, Boolean indexing, transpose, `ravel()`, and multi-dimensional reshaping
3. **Broadcasting:** Element-wise operations between arrays of different shapes — row and column vector broadcasting
4. **Statistical Analysis:** Mean, median, standard deviation, percentiles, IQR, Sharpe ratio, and maximum drawdown computed across 5 simulated stock tickers (OGDC, HBL, PSO, LUCK, ENGRO)
5. **Linear Algebra:** Dot product, matrix multiplication, determinant, inverse, eigenvalues, and solving linear systems with `np.linalg.solve`
6. **Random Sampling:** Uniform, normal, Poisson distributions + Monte Carlo estimation of π using 1M random points

### 🔹 Performance Benchmark
Side-by-side comparison of pure Python loops vs. NumPy vectorized operations across array sizes from 1K to 1M elements, demonstrating 10–50x speedups.

### 🔹 Dataset
252-day simulated stock price time series for 5 PSX-listed companies

---

## 🧹 Module 4: Data Exploration & Cleaning (Lab 4)

Practical data wrangling using Pandas on the Titanic passenger dataset — covering the full pipeline from raw data to analysis-ready output.

### 🔹 Exploration Workflow

- **Loading:** Importing the same dataset from CSV, Excel, and JSON to demonstrate format flexibility
- **Inspection:** `head()`, `tail()`, `info()`, `describe()`, `shape`, `dtypes`, `nunique()`
- **Missing Data Audit:** Column-level null counts and percentage breakdown

### 🔹 Cleaning & Transformation

- **Boolean Filtering:** Isolating passenger subsets — survived females in 1st class, seniors over 50, top 5% fare passengers, survived children under 18
- **Sorting:** Single-column and multi-column sorts with `sort_values()` and within-group ranking using `groupby().rank()`
- **Missing Value Handling:**
  - Age: Median imputation grouped by passenger class
  - Embarked: Mode imputation
- **Feature Engineering:** Creating derived columns
  - `FamilySize` = SibSp + Parch + 1
  - `IsAlone` = binary flag for solo travelers
  - `AgeGroup` = categorical bins (Child, Teen, Young Adult, Adult, Senior)
  - `FarePerPerson` = Fare / FamilySize

### 🔹 Key Insight
Survival rate analysis grouped by class and sex, revealing strong class/gender survival disparities consistent with historical records.

### 🔹 Dataset
Titanic passenger manifest — 891 records with survival, class, age, fare, and embarkation data

---

## 📈 Module 5: Data Visualization Portfolio (Lab 5)

A comprehensive visualization portfolio featuring **12 distinct chart types** built on simulated COVID-19 pandemic data across 5 countries over 365 days.

### 🔹 Chart Catalog

| # | Chart Type | Technique Demonstrated |
|---|-----------|----------------------|
| 1 | **Line Plot** | 7-day rolling average for time series smoothing |
| 2 | **Horizontal Bar** | Country-level case totals with value annotations |
| 3 | **Histogram** | Distribution shape analysis with mean/median markers |
| 4 | **Scatter Plot** | Cases vs. deaths correlation with regression trend line |
| 5 | **Box Plot** | Quartile distribution comparison across countries |
| 6 | **Violin Plot** | Monthly density distribution for Pakistan |
| 7 | **Heatmap** | Correlation matrix with triangular masking |
| 8 | **Area Chart** | Cumulative case growth with fill shading |
| 9 | **Pie + Donut** | Proportional case share (two variants) |
| 10 | **Stacked Bar** | Monthly breakdown by country |
| 11 | **Multi-Panel Dashboard** | 4-subplot figure: trends, death rate, vaccination, peak analysis |
| 12 | **Pair Plot** | Multivariate scatter matrix with KDE diagonals |

### 🔹 Customization Applied
- Custom color palettes (`viridis`, `Set2`, `husl`)
- Axis formatting with `DateFormatter` and `MonthLocator`
- Annotations, trend lines, and statistical markers
- Professional titles, labels, and legends on every chart

### 🔹 Dataset
Simulated COVID-19 statistics — daily cases, deaths, recoveries, and vaccination rates for Pakistan, India, UK, USA, and Germany

---

## 🛠 Tech Stack

| Tool | Usage |
|------|-------|
| Python 3.10+ | Core language |
| Jupyter Notebook | Interactive development |
| NumPy | Array operations & linear algebra |
| Pandas | DataFrames, groupby, cleaning |
| Matplotlib | All chart rendering |
| Seaborn | Statistical plot styling |

---

## ✅ Completion Checklist

- [x] Installed and verified Anaconda/Python environment
- [x] Demonstrated proficiency in Python data structures (Lists, Dicts, Tuples, Sets)
- [x] Implemented file I/O across CSV, JSON, and text formats
- [x] Executed statistical and linear algebra operations using NumPy on financial data
- [x] Performed end-to-end data cleaning and feature engineering on Titanic dataset
- [x] Built a visualization portfolio with 12 distinct chart types
- [x] Maintained clean, documented, and organized repository structure

---

*This project was completed as part of the Data Analytics Laboratory curriculum — Spring 2026.*

---

## 👥 Project Contributors

- **Abdul Ahad**
- **Abdullah Jabbar**
- **Asjid**

### Group Members

- **Abdullah Jabbar**
- **Abdul Ahad**
- **Quarrat ul Ain Jeelani**
- **Javeria Zainab**
- **Hadia Shahid**
