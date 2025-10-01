# ML Mastery Project (Hands-On, No Fluff)

This repo is a **single, cohesive project** to make you *do* machine learning, not just watch it.
It follows the exact sequence you asked for (12 topics), with **from-scratch builds**, **scikit-learn** equivalents, and **experiments**.

## How to use
1. Create/activate a fresh environment (conda or venv).
2. `pip install -r requirements.txt`
3. Open `notebooks/` and go in order: `00_setup_env` → `09_probability_and_mle`.
4. Every notebook has **MANDATORY TODOs**. Do all of them. No shortcuts.
5. Keep results comparable: stick to the same tabular dataset where asked (California Housing, or fallback to synthetic).

## Core topics (notebook order)
0. Setup + dataset check
1. NumPy + Linear Algebra (what you actually use in ML)
2. Linear Regression (Closed form, OLS) — from scratch
3. Gradient Descent vs. Stochastic Gradient Descent — from scratch
4. Basis Functions (Polynomial & Interactions) — theory + code
5. Model Selection Workflow — `Pipeline`, `ColumnTransformer`, `GridSearchCV`
6. Regularization — Ridge, Lasso, Elastic Net (math intuition + CV sweeps)
7. K-Nearest Neighbors — regression with scaling and k tuning
8. Bias–Variance — learning/validation curves, diagnostics
9. Probability + Maximum Likelihood — derive and verify numerically

## Acceptance criteria (you'll know you learned it when...)
- You can reproduce OLS both **analytically** and via **GD/SGD**, and they match within tolerance.
- Your Pipeline+GridSearch beats a baseline and is **not** data-leaky.
- You can plot and explain **validation** and **learning** curves and make the right fix (data vs. regularization vs. simpler model).
- You can show how **λ** affects coefficients in Ridge/Lasso/ElasticNet and defend a choice.
- You can tune **k** for KNN and prove why scaling matters (quantitatively).
- You can derive **MLE for Normal** and verify numerically with code.

## Dataset
- Primary: `sklearn.datasets.fetch_california_housing` (regression). If download fails, notebooks auto-fallback to a synthetic `make_regression` dataset so you can keep working offline.
- Stay consistent across notebooks to compare results.

## Structure
```
ml_mastery_project/
├─ requirements.txt
├─ README.md
└─ notebooks/
   ├─ 00_setup_env.ipynb
   ├─ 01_numpy_linear_algebra.ipynb
   ├─ 02_linear_regression_closed_form.ipynb
   ├─ 03_gradient_descent_and_sgd.ipynb
   ├─ 04_basis_functions_and_polynomial_features.ipynb
   ├─ 05_model_selection_and_pipeline_cv.ipynb
   ├─ 06_regularization_ridge_lasso_elasticnet.ipynb
   ├─ 07_knn_regression.ipynb
   ├─ 08_bias_variance_learning_curves.ipynb
   └─ 09_probability_and_mle.ipynb
```
