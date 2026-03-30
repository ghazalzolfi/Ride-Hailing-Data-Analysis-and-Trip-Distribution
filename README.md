# Ride-Hailing-Data-Analysis-and-Trip-Distribution

## 📌 Project Overview
This repository contains the deliverables for the **Transportation Planning** course at Sharif University of Technology (Fall 1404). The project is divided into two distinct phases, focusing on the analysis of Uber and Lyft trip data from 2018, trip distribution modeling, and revenue optimization.

## 📂 Repository Structure
The project consists of the following four main files:
*   **`Phase_1_Notebook.ipynb`**: The Python code and implementation for Phase 1.
*   **`Phase_1_Report.pdf`**: The comprehensive report detailing the methodologies, analyses, and conclusions for Phase 1.
*   **`Phase_2_Notebook.ipynb`**: The Python code and implementation for Phase 2.
*   **`Phase_2_Report.pdf`**: The comprehensive report detailing the OD matrix analysis, distribution algorithms, and optimization results for Phase 2.

---

## 🚀 Phase 1: Exploratory Data Analysis & Predictive Modeling
The primary objective of the first phase is to analyze trip data from Uber and Lyft to understand pricing patterns and the impact of temporal and weather factors. 

### Key Highlights of Phase 1:
*   **Data Exploration & Preprocessing:** Identifying active origin-destination pairs, handling missing values, and applying encoding techniques for categorical variables like ride types.
*   **Statistical & Exploratory Analysis (EDA):** Conducting statistical tests to determine price differences among ride types, analyzing price trends over time, handling outliers, and visualizing data using histograms, boxplots, and heatmaps (by day and hour).
*   **Weather Impact Analysis:** Utilizing PCA or clustering techniques to analyze weather data and implementing classification models to predict the presence of rain based on weather conditions, evaluated using a confusion matrix.
*   **Price Prediction Models:** Selecting critical features and building regression models to predict ride prices. This includes using advanced ensemble methods like XGBoost and Random Forest, followed by hyperparameter tuning using Grid Search and Taguchi methods.

---

## 🗺️ Phase 2: Origin-Destination (OD) Matrix & Trip Distribution
The second phase shifts focus toward macro-level transportation planning concepts, utilizing the raw data from the first phase without further preprocessing.

### Key Highlights of Phase 2:
*   **OD Matrix Analysis:** Constructing OD matrices for each day of the week to analyze trip frequencies between different pairs and evaluating the input/output balance of various zones.
*   **Trip Distribution Models:** Forecasting future trip distributions across 12 specific zones (e.g., Financial District, Boston University, North End) using given future origin and destination estimates. The following algorithms were implemented and compared for convergence:
    *   Furness Algorithm
    *   Detroit Algorithm (with a growth factor convergence threshold of $[0.99, 1.01]$)
    *   Fratar Algorithm
    *   Gravity Model (using an exponential deterrence function with a parameter of $0.2$, as well as a custom distribution function)
*   **Revenue Stream Optimization:** Developing a strategy to enter the market as a competitor. The goal is to maximize profit by optimizing the number of trips between zones across 6-hour time intervals. The pricing strategy averages the competitors' prices for those specific times, subjected to operational constraints such as a maximum daily fleet service of 20 kilometers and no service provision on Saturdays and Sundays.
