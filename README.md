# Genetic Algorithm and Fuzzy Logic for Bankruptcy Prediction

This project applies **Genetic Algorithms (GA)** and **Fuzzy Logic** to the Taiwanese Bankruptcy Prediction dataset. The aim is to select optimal features and rules for predicting bankruptcy status with interpretable fuzzy logic systems.

---

## Table of Contents

1. [Introduction](#introduction)
2. [Project Overview](#project-overview)
3. [Workflow](#workflow)
4. [Key Features](#key-features)
5. [Dependencies](#dependencies)
6. [Results](#results)
7. [Usage](#usage)
8. [License](#license)

---

## Introduction

This notebook demonstrates an end-to-end process for selecting features and rules using Genetic Algorithms while implementing a fuzzy logic system for decision-making. It predicts whether a company is likely to go bankrupt based on financial ratios and other features.

---

## Project Overview

### Objectives:

1. **Feature Selection:**
   - Utilize Genetic Algorithms to select the best subset of features based on fitness metrics like accuracy and F1-score.
   - Compare Logistic Regression and Random Forest models for feature importance.

2. **Fuzzy Logic:**
   - Define membership functions for selected features.
   - Generate fuzzy rules based on the dataset.
   - Select optimal fuzzy rules using Genetic Algorithms to maximize prediction accuracy or F1-score.

3. **Evaluation:**
   - Measure model performance through metrics like accuracy and F1-score.
   - Visualize feature importance.

---

## Workflow

### 1. **Data Preparation:**
   - Handle class imbalance through down-sampling.
   - Split data into training and testing sets.

### 2. **Feature Selection:**
   - Use Genetic Algorithms with various fitness functions (e.g., Logistic Regression and Random Forest).
   - Apply penalties for using too many features to ensure simplicity.

### 3. **Fuzzy Logic System:**
   - Define membership functions (low, mid, high) for each selected feature.
   - Construct rules based on membership degrees and target values.

### 4. **Rules Optimization:**
   - Optimize the fuzzy rule set using Genetic Algorithms with selection methods like Tournament, Rank, or Roulette-wheel selection.

### 5. **Performance Evaluation:**
   - Compare model performance using metrics like accuracy and F1-score.
   - Visualize the importance of features and their contributions to predictions.

---

## Key Features

1. **Dynamic Parameter Updates:**
   - Modify crossover and mutation rates dynamically during Genetic Algorithm runs.

2. **Flexible Fitness Functions:**
   - Accuracy and F1-score metrics for both feature selection and rule selection.

3. **Two Rule Generation Methods:**
   - Method 1: Exhaustive combinations (resource-intensive but comprehensive).
   - Method 2: Reduced logical combinations (efficient and practical).

4. **Fuzzy System Interpretability:**
   - Generate human-readable rules for decision-making.

5. **Scalability:**
   - Parameterized implementation allows easy tuning for different datasets and objectives.

---

## Dependencies

Install the required libraries using:

```bash
pip install -r requirements.txt
```

### Main Libraries:

- `numpy`
- `pandas`
- `skfuzzy`
- `matplotlib`
- `seaborn`
- `deap`
- `scikit-learn`
- `ucimlrepo`

---

## Results

### Key Insights:

1. **Feature Selection:**
   - Logistic Regression and Random Forest models select different optimal features.
   - Genetic Algorithms improve the interpretability and simplicity of the models by selecting a limited number of features.

2. **Fuzzy Logic System:**
   - Rules generated through the fuzzy logic system align with domain knowledge.
   - Optimal rule selection enhances model interpretability without sacrificing accuracy.

3. **Performance:**
   - Best accuracy and F1-scores achieved with selected features and rules:
     - **Logistic Regression:**
       - Best Features: [Features]
       - Best Fitness: [Fitness Score]
     - **Random Forest:**
       - Best Features: [Features]
       - Best Fitness: [Fitness Score]

4. **Feature Importance:**
   - Visualizations highlight the top financial ratios contributing to bankruptcy predictions.

---

## Usage

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/bankruptcy-ga-fuzzy.git
   cd bankruptcy-ga-fuzzy
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the notebook:
   - Open `bankruptcy_prediction_ga_fuzzy.ipynb` and execute the cells to replicate the analysis.

---

## License

This project is licensed under the MIT License. For more details, see the [LICENSE](LICENSE) file.

---

## Acknowledgments

- Dataset sourced from the UCI Machine Learning Repository.
- Inspiration from Fuzzy Logic systems and Genetic Algorithm optimization in predictive analytics.

Feel free to raise issues, suggest enhancements, or contribute to the project!
