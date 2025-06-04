# 🔍 Pricing-Analysis-Hyperparameter-Tuning

![ChatGPT Image Jun 4, 2025, 12_37_29 PM](https://github.com/user-attachments/assets/689592cf-2c28-4f92-82bd-9f9d4850ff26)


In every data science project, hyperparameter tuning is a crucial step to ensure model performance is optimized and aligned with real-world decision-making needs. After developing a predictive pricing model for used vehicles, this project focuses on evaluating and improving its accuracy using advanced tuning strategies.

---

## 🎯 Objective

Refine the predictive model built during the pricing analytics project by applying and comparing various hyperparameter tuning techniques. The goal is to improve predictive accuracy while balancing model complexity and training time — culminating in a high-performance XGBoost model.

---

## 🔧 Models and Tuning Methods

| Model                 | Tuning Method         | R² Score |
|----------------------|-----------------------|----------|
| Random Forest         | Default Parameters    | 0.8100   |
| Random Forest         | RandomizedSearchCV    | 0.7381   |
| Random Forest         | HalvingGridSearchCV   | 0.7718   |
| Random Forest         | Optuna Tuning         | 0.7437   |
| **XGBoost (final)**   | **Optuna Tuning**     | ✅ **0.9956** |

---

## 📈 Final Model: XGBoost + Optuna

```python
Best Parameters:
{
  'n_estimators': 157,
  'max_depth': 7,
  'learning_rate': 0.2525,
  'subsample': 0.9835,
  'colsample_bytree': 0.9888,
  'min_child_weight': 8,
  'gamma': 0.0174
}
