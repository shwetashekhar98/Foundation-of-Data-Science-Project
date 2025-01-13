# CS-GY 6053 Foundation of Data Science Project

# Food Delivery Time Analysis: Impact of Weather Conditions

## **Project Overview**
This project aims to analyze how different weather conditions impact food delivery times across varying distances. By understanding the relationship between weather, distance, and delivery times, this study can provide actionable insights for food delivery services to optimize routes, improve delivery time estimates, and set better customer expectations.

---

## **Research Question**
**How do different weather conditions impact food delivery times across varying distances?**  
This question explores the relationship between environmental and logistical factors, helping identify trends and patterns that affect delivery efficiency.

---

## **Dataset Description**
- **Source**: [Kaggle - Food Delivery Dataset](https://www.kaggle.com/datasets/gauravmalik26/food-delivery-dataset)
- **Sample Size**: ~10,000 delivery records.
- **Key Variables**:
  - **Order ID**: Unique identifier for each order.
  - **Delivery Time (T)**: Time taken for delivery (in minutes).
  - **Distance (D)**: Distance between the restaurant and delivery location.
  - **Weather Conditions (W)**: Categorized as sunny, rainy, stormy, foggy, etc.
  - **Order Time**: Timestamp when the order was placed.
  - **Delivery Location Type**: Urban, suburban, or rural classification.
  - **Traffic Conditions**: Status of traffic during the delivery (if available).

---

## **Causal Model**
The analysis uses a Directed Acyclic Graph (DAG) to represent variable relationships:
- **Treatment Variable**: Weather conditions (W).
- **Outcome Variable**: Delivery time (T).
- **Confounding Variable**: Distance (D).

---

## **Statistical Models**
Two models are employed to evaluate the relationship between variables:
1. **Multivariate Linear Regression**:
   - Captures linear relationships between delivery time, weather, and distance.
2. **Decision Tree Regression**:
   - Handles non-linear interactions and provides interpretable outputs.

---

## **Proposed Enhancements**
- **Interaction Terms**: Including interaction effects between weather conditions and distance in the regression model.
- **Feature Engineering**: Additional variables such as traffic, time of day, and road type may be included if data is available.
- **Regularization**: Techniques like Lasso or Ridge regression to mitigate overfitting risks.
- **Data Preprocessing**:
  - Imputation of missing data.
  - Scaling continuous variables.
  - Encoding categorical variables (e.g., weather types).


---

## **Expected Insights**
- Quantify the impact of weather on delivery times.
- Identify patterns in delivery delays under specific weather and distance combinations.
- Provide recommendations for optimizing delivery efficiency in different scenarios.

---

## **Project Team**
- **Akshat Singh** 
- **Abha Wadijkar** 
- **Shweta Shekhar** 

For additional details or collaboration inquiries, please contact the project team members.
