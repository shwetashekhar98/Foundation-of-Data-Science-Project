# CS-GY 6053 Foundation of Data Science Final Project

# Causal Impact of Weather Conditions on Food Delivery Times

## Project Overview
This project investigates the causal impact of weather conditions on food delivery times, accounting for traffic density as a significant confounding variable. The analysis focuses on understanding how weather directly and indirectly affects delivery efficiency, providing insights that can help optimize logistics and improve customer satisfaction.

---

## Research Question
**How do weather conditions causally influence food delivery times, considering traffic density as a confounding factor?**

This question addresses the interplay between environmental and logistical factors to uncover the total and direct effects of weather on delivery times.

---

## Dataset Description
The dataset was sourced from Kaggle and includes **100 observations** on delivery performance across different conditions. Key variables are:

- **Delivery Time (`time`)**: Measured in minutes, representing the outcome variable.
- **Weather Conditions (`weather`)**: Categorical variable with six levels:
  - Cloudy
  - Fog
  - Sandstorms
  - Stormy
  - Sunny
  - Windy
- **Traffic Density (`traffic`)**: Categorical variable with three levels:
  - High
  - Medium
  - Low

---

## Causal Model
The causal relationships between variables are depicted using a **Directed Acyclic Graph (DAG)**:
- **Weather → Traffic**: Weather influences traffic density.
- **Weather → Delivery Time**: Weather conditions directly impact delivery time.
- **Traffic → Delivery Time**: Traffic density affects delivery time.
- **Weather → Traffic → Delivery Time**: Weather indirectly impacts delivery time through traffic.

### Statistical Models
1. **Total Effect Model**: Captures the overall impact of weather conditions on delivery times without controlling for traffic.
2. **Direct Effect Model**: Isolates the direct impact of weather on delivery times by accounting for traffic as a mediator.

---

## Priors and Distributions
- **Weather-Specific Effects (`α[w]`)**: Assumed to follow a `Normal(0, 0.5)` distribution.
- **Residual Variability (`σ`)**: Modeled using an `Exponential(0.5)` distribution.

---

## Methodology
### Preprocessing
- Standardized delivery times for uniformity.
- Encoded categorical variables for compatibility with statistical modeling.

### Model Evaluation
- Leave-One-Out Cross-Validation (LOO) was performed to compare models.
- Pareto `k` values were assessed to confirm reliable LOO estimates.

---

## Key Findings
1. **Adverse Weather Conditions**:
   - Weather types such as storms and sandstorms significantly increase delivery times.
   - Sunny and windy conditions have relatively lower impacts.
2. **Traffic Density**:
   - Traffic density mediates the impact of weather on delivery times, with high traffic amplifying delays.
3. **Model Performance**:
   - The **Direct Effect Model** (ELPD = 228.90) demonstrated superior fit compared to the **Total Effect Model** (ELPD = 273.82).

---

## Visualizations
1. **Scatter Plots**:
   - Show the relationship between weather, traffic, and standardized delivery times.
2. **Box Plots**:
   - Highlight the variation in delivery times across weather categories.
3. **Posterior Predictive Checks**:
   - Validate the models' fit to observed data.
4. **DAGs**:
   - Depict the causal pathways and their effects.

---

## Conclusion
The study confirms that weather and traffic are critical factors influencing delivery times. By isolating direct and mediated effects, the findings provide actionable insights for improving delivery efficiency under varying weather and traffic conditions.

---

Food Delivery Data Subset
This document describes the food_delivery_data.csv file, which is a subset of the Kaggle Food Delivery Dataset. It is specifically curated for a causal inference project as part of the CS-GY 6053: Foundations of Data Science course at NYU Tandon, Fall 2024.

Dataset Details
Filename: food_delivery_data.csv
Number of Rows: 100
Columns:
Weather: Represents the weather conditions during food delivery.
Traffic: Indicates road traffic density.
Time: The time taken for food delivery, measured in minutes.

## How to Run the Analysis
1. Clone this repository:
   ```bash
   git clone <repository-url>
## Contributors of this project 
Akshat Singh 
Shweta Shekhar
Abha Wadijkar
