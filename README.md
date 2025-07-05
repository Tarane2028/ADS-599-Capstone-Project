# ADS-599 Capstone Project: Spatial-Temporal and Predictive Modeling of Radiological Contaminant Exceedances in California Public Water Systems

## Overview
This repository contains the code, data processing scripts, analysis notebooks, and dashboard for our ADS-599 capstone project. We perform a comprehensive spatial-temporal analysis of radiological contaminant results from California’s public water systems, quantify exceedance rates of EPA Maximum Contaminant Levels (MCLs), and build predictive models to identify system characteristics that drive risk.

## Table of Contents
- [Dataset](#dataset)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Usage](#usage)
  - [Data Preprocessing](#data-preprocessing)
  - [Exploratory Analysis](#exploratory-analysis)
  - [Modeling](#modeling)
  - [Dashboard](#dashboard)
- [Results & Deliverables](#results--deliverables)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Dataset
- **Source:** U.S. EPA’s Safe Drinking Water Information System (SDWIS) extract for California.
- **Rows & Columns:** ~600,000 records, 57 variables including system identifiers, population served, analyte codes, sample dates, result values, detection flags, MCL thresholds, and more.

## Project Structure
```
├── data/                      # Raw and processed data files
│   ├── raw/                   # Original SDWIS extracts
│   └── processed/             # Cleaned datasets for analysis
├── notebooks/                 # Jupyter notebooks for analysis
│   ├── 01_data_cleaning.ipynb
│   ├── 02_exploratory_analysis.ipynb
│   ├── 03_spatial_trends.ipynb
│   ├── 04_time_series.ipynb
│   └── 05_predictive_modeling.ipynb
├── scripts/                   # Python scripts for data pipelines
│   ├── preprocess.py
│   ├── feature_engineering.py
│   └── modeling.py
├── dashboard/                 # Flask or Dash app code
│   ├── app.py
│   └── templates/
├── requirements.txt           # Python dependencies
└── README.md                  # This file
```

## Getting Started

### Prerequisites
- Python 3.8+ 
- Virtual environment tool (e.g., `venv` or `conda`)

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/Tarane2028/ADS-599-Capstone-Project.git
   cd ADS-599-Capstone-Project
   ```
2. Create and activate a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate        # macOS/Linux
   venv\Scripts\activate.bat     # Windows
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

### Data Preprocessing
Run the preprocessing script to clean raw SDWIS data, impute non-detects, and standardize formats:
```bash
python scripts/preprocess.py --input data/raw/Final.xlsx --output data/processed/cleaned.csv
```

### Exploratory Analysis
Execute the notebooks under `notebooks/` to generate summary statistics, visualizations, and geospatial maps:
```bash
jupyter notebook notebooks/01_data_cleaning.ipynb
``` 

### Modeling
Train and evaluate predictive models with:
```bash
python scripts/modeling.py --config config/model_config.yaml
``` 

### Dashboard
Launch the interactive dashboard:
```bash
cd dashboard
python app.py
```  
Open your browser to `http://localhost:8050`.

## Results & Deliverables
- **Interactive Dashboard:** Visualize exceedance hot spots and time-series trends.
- **Technical Report:** Executive summary and detailed appendix (located in `docs/` folder).
- **Policy Recommendations:** Top 10 systems/counties prioritized for monitoring.

## Contributing
1. Fork the project
2. Create a feature branch (`git checkout -b feature/MyFeature`)
3. Commit your changes (`git commit -m 'Add MyFeature'`)
4. Push to the branch (`git push origin feature/MyFeature`)
5. Open a Pull Request

## License
This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.

## Contact
- **Tarane Javaherpour:** Tarane2028
- **Davood Aeien:** Davoodaein66
