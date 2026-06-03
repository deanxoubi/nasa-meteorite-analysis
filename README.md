# NASA Meteorite Landings Analysis

This repository contains two data analysis notebooks using NASA meteorite landing data from Kaggle. The project explores how meteorite landing frequency has changed over time and analyzes meteorite mass using confidence intervals, bootstrapping, and hypothesis testing.

## Project Overview

The goal of this project is to better understand patterns in meteorite landings by analyzing two main questions:

1. **Are meteorite landings becoming more common over time?**
2. **What proportion of meteorites weigh more than 1 kilogram, and is the typical meteorite mass below 1 kilogram?**

Together, the notebooks combine data cleaning, exploratory analysis, statistical testing, and interpretation of results.

## Repository Contents

```text
.
├── Meteorite_Project_1.ipynb   # Landing frequency analysis by year
├── Meteorite_Project_2.ipynb   # Meteorite mass analysis and statistical testing
├── meteorlandingscsv.csv       # Dataset used in both notebooks
└── README.md
```

## Dataset

The dataset comes from NASA's Meteorite Landings data, accessed through Kaggle:

https://www.kaggle.com/datasets/nasa/meteorite-landings

Each row represents one meteorite landing and includes information such as:

- Meteorite name
- Mass in grams
- Year of landing or discovery
- Classification
- Fall status
- Latitude and longitude
- Geolocation

## Notebook 1: Meteorite Landing Frequency Analysis

The first notebook analyzes whether meteorite landings have become more common over time.

### Main Question

**How is meteorite landing frequency associated with year?**

### Methods Used

- Cleaned missing and invalid values
- Removed implausible future years
- Grouped meteorite landings by year
- Compared two 50-year periods:
  - 1900-1950
  - 1963-2013
- Calculated average annual meteorite landings for each period
- Visualized landing frequency trends over time

### Key Finding

The analysis found a large increase in recorded meteorite landings between the two periods. The average annual number of recorded landings increased from about **19 per year** from 1900-1950 to about **710 per year** from 1963-2013.

## Notebook 2: Meteorite Mass and Statistical Analysis

The second notebook focuses on meteorite mass and uses statistical methods to analyze how common heavier meteorites are.

### Main Questions

- What proportion of meteorites weigh more than 1,000 grams?
- With 85% confidence, what is a reasonable interval for that population proportion?
- Is the median mass of all meteorites less than 1,000 grams?

### Methods Used

- Cleaned missing values and invalid years
- Created a sample of 200 meteorite observations
- Created a binary variable for meteorites over 1,000 grams
- Used bootstrapping to estimate a confidence interval
- Used hypothesis testing to evaluate median meteorite mass
- Used summary statistics and visualization to identify outliers

### Key Findings

The sample proportion of meteorites over 1,000 grams was about **15.5%**. The 85% confidence interval estimated that the true population proportion of meteorites over 1 kilogram is between **11.5% and 19%**.

The hypothesis test provided evidence that the median meteorite mass is less than **1,000 grams**, suggesting that most meteorites in the dataset are relatively small.

## Tools and Libraries

- Python
- pandas
- NumPy
- matplotlib
- seaborn
- bootstrapping
- hypothesis testing
- confidence intervals

## How to Run the Project

1. Clone this repository:

```bash
git clone <your-repository-link>
```

2. Open the project folder:

```bash
cd <your-repository-name>
```

3. Install the required Python libraries:

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

4. Open Jupyter Notebook:

```bash
jupyter notebook
```

5. Run the notebooks in order:

```text
Meteorite_Project_1.ipynb
Meteorite_Project_2.ipynb
```

Make sure the dataset file, `meteorlandingscsv.csv`, is in the same folder as the notebooks.

## Skills Demonstrated

- Data cleaning and preprocessing
- Exploratory data analysis
- Statistical reasoning
- Bootstrapping
- Confidence interval interpretation
- Hypothesis testing
- Data visualization
- Python programming with pandas

## Author

Dean Xoubi
University of Illinois Urbana-Champaign
Gies College of Business.
