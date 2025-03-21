# ecgr5105 Assignment 1 Summary

**Student Name:** Yang Xu<br>
**Student ID:** 801443244<br>
**Assignment Number:** 2<br>
**GitHub Repository:** [GitHub repo](https://github.com/xuy50/ecgr5105/tree/main/Assignment_2)<br>

## Problem 1: Baseline Linear Regression

- **Objective:** Implement linear regression with gradient descent on two different sets of input features (Problem 1a and 1b).
- **Features:**
  - *Problem 1a:* area, bedrooms, bathrooms, stories, parking  
  - *Problem 1b:* area, bedrooms, bathrooms, stories, mainroad, guestroom, basement, hotwaterheating, airconditioning, parking, prefarea
- **Learning Rates Tested:** 0.1, 0.05, 0.01  
- **Observations:**
  - Larger learning rates (0.1 or 0.05) converged faster and often reached lower MSE than 0.01.
  - Adding more features (Problem 1b) generally decreased training and validation loss, suggesting improved predictive power.
- **Key Plots:**
  - Training vs. validation loss curves for each feature set and each learning rate.
  - Comparison of final losses helps determine the best learning rate and feature set.

## Problem 2: Linear Regression with Input Scaling

- **Objective:** Repeat Problem 1’s experiments using two scaling methods:
  1. Normalization (Min-Max)
  2. Standardization (Z-score)
- **Experiments:**
  - *Problem 2a:* Same features as 1a, scaled with both methods
  - *Problem 2b:* Same features as 1b, scaled with both methods
- **Learning Rates Tested:** 0.1, 0.05, 0.01 (same approach as Problem 1)
- **Observations:**
  - Standardization often yielded more stable convergence and lower MSE, especially for the smaller feature set (Problem 2a).
  - Normalization performed comparably well for the expanded feature set (Problem 2b) when paired with a higher learning rate.
- **Key Plots:**
  - Side-by-side comparisons of training and validation losses for Normalization vs. Standardization.
  - Additional plots showing the influence of different learning rates on scaled data.

## Problem 3: L2 Regularized Linear Regression

- **Objective:** Add an L2 penalty (regularization) to the gradient descent update while reusing the best scaling approach (Standardization).
- **Experiments:**
  - *Problem 3a:* Regularized version of Problem 2a (area, bedrooms, bathrooms, stories, parking)
  - *Problem 3b:* Regularized version of Problem 2b (expanded feature set)
- **Regularization Strengths:** Various \(\lambda\) values tested (e.g., 0.1, 0.05, 0.01)
- **Observations:**
  - Moderate \(\lambda\) values did not significantly alter final MSE compared to the non-regularized models, indicating limited overfitting or insufficient \(\lambda\).
  - Training losses slightly increased, while validation losses remained stable or slightly decreased, suggesting mild regularization benefits.
- **Key Plots:**
  - Training vs. validation losses for different \(\lambda\) values.
  - Comparisons with Problem 2’s baseline models to highlight the effect of regularization.

---

**Overall**, Assignment 2 demonstrates how **feature scaling** (Normalization vs. Standardization) and **L2 regularization** impact gradient descent training. Each problem includes plots of training/validation losses and final parameters for thorough analysis of model performance.