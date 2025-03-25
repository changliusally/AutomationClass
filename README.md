# Active Learning Strategies for Biological Data – Automation Class (Spring 2025)

This repository contains code developed for the coursework of the Automation class (Spring 2025). The focus is on implementing and evaluating various **active learning** strategies in a classification setting, particularly within the context of biological datasets. The goal is to compare these methods against passive learning to explore the practical benefits of active learning in biological data analysis.

---

## Overview

In this hw2, several **active learning** strategies are implemented using **Random Forest** as the base classifier. The general workflow involves:

- Starting with 50% of the full dataset as the initial training set.
- Iteratively querying and adding informative samples to the training set using different active learning strategies.
- Retraining the Random Forest model after each addition.
- Evaluating the performance of each method using 5-fold cross-validation accuracy.
- Plotting the final model performance over iterations using a line chart for visual comparison.

---

## Key Components

### 🧪 `exercise_1.ipynb` – Core Strategies  
- **`QueryByCommittee`** class: Implements the query-by-committee strategy by selecting 5 random trees from a 50-tree Random Forest and identifying samples with the highest prediction variance among the committee.
- **Uncertainty Sampling**: Selects data points with the least confident predictions, in this classification, we use cross entropy as a measure of uncertainty.
- **Density-Based Sampling**: Incorporates feature space density to prioritize samples from densely populated regions.
- **Passive Learning (Random Sampling)**: Baseline strategy that selects data points randomly.

### 🧠 `exercise_2.ipynb` – IWAL (Importance Weighted Active Learning)  
- Implements the IWAL strategy, which assigns importance weights to each queried instance to correct for selection bias.

### 📊 `exercise_3.ipynb` – ZLG Strategy  
- Implements the ZLG algorithm for active learning, which combines both prediction uncertainty and representativeness of data points in the selection process.

---

## Visualization

Each strategy’s performance is tracked and visualized through a **line chart**, showing the 5-fold CV accuracy of the Random Forest model over time as new data is actively added. There is a report named 'Chang_Liu_hw2.pdf' for further information.


---

## Goals

- Understand the mechanisms of active learning in classification tasks.
- Compare performance across diverse data query strategies.
- Explore trade-offs between exploration and exploitation in sample selection.

---

Feel free to contribute or reach out if you’re also working on active learning problems!
