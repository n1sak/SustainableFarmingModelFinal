# 🌱 Sustainable Farming Model

A machine learning model built to improve sustainable agriculture by increasing crop yields through the analysis of soil bacteria data from 1,344 farms.

---

## Problem

690 million people go to bed hungry every night. That number is projected to rise to 840 million by 2030. Meanwhile, over 40% of food is wasted globally.

As the world population approaches 9 billion, increasing food availability is essential.

---

## Objective

This model explores how the presence of specific soil bacteria affects crop yields. By identifying beneficial microbial patterns, the model helps optimize farm output and food availability.

---

## Data

- Input (X): Soil bacteria sample counts from 1,344 farms  
- Output (Y): Predicted crop yield per farm

### Preprocessing Steps

- Removed low-prevalence bacterial species (present in <10 farms)
- Applied log normalization to reduce variance and emphasize relative differences:

N_norm = log(N + 1)

This ensures all values remain positive while improving model performance.

---

## Model

A Random Forest Regressor was selected for its balance between interpretability and predictive power.

### Why Random Forest?

- Handles complex, non-linear relationships
- More robust than individual decision trees
- Offers enough transparency to be understood by non-technical stakeholders

### Hyperparameter Tuning

Hyperparameters were carefully optimized to improve efficiency and accuracy.

---

## Model Performance

| Metric                 | Value  |
|------------------------|--------|
| R² Score               | 0.80   |
| Mean Absolute Error    | 0.06   |
| Relative Squared Error | 0.19   |

These results indicate strong generalization to unseen test data.

---

## Real-World Impact

A simulated test compared two approaches for selecting farms based on predicted yield:

- Random Selection: 5–8 lbs/acre  
- Model-Assisted Selection: **12.615 lbs/acre**

✅ Result: Nearly 2× increase in crop yield using the model.

---

## Policy Relevance

Policymakers tend to prefer interpretable models such as:

- Decision Trees  
- Linear Regression  
- K-Nearest Neighbors

This model uses Random Forests, which retain interpretability while offering high performance and making them suitable for policy-oriented deployment.

---

## Future Extensions

- Autonomous crop harvesting systems  
- Image recognition for produce sorting  
- Real-time bacterial monitoring in soil

---

## References

- [Feeding 9 Billion – National Geographic](https://www.nationalgeographic.com/foodfeatures/feeding-9-billion/)
- [Cyanobacteria Overview – Oklahoma DEQ](https://www.deq.ok.gov/state-environmental-laboratory-services/environmental-public-health-information/harmful-algal-blooms/what-are-cyanobacteria/)
- [Agricultural Innovation – Azernews](https://www.azernews.az/region/135338.html)

---

## Author

Built by **Nisa**.
