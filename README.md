# Credit_Risk-Scoring-and-Probability-of-Default-Model
In the unsecured consumer lending industry, a bank's core product isn't money—it is the accurate pricing of risk. I built this end-to-end predictive engine to bridge the gap between traditional banking analytics and modern machine learning architecture.  My primary objective was to develop a robust ML model.
This meant handling extreme data noise, preventing subtle data leakage, understanding Basel III regulatory requirements for model interpretability, and ultimately translating statistical metrics (like F1-Scores) into tangible financial ROI (Expected Value).
This repository contains the complete pipeline for analyzing 2.2 million historical loan records to predict default probabilities strictly using pre-origination data.

**Methodologies & Architecture**
To achieve good results, I implemented a progression of techniques, which are also used by top-tier banks and modern FinTechs:

**Data Integrity & Leakage Prevention:** Rigorously "sponged" the dataset to remove any post-origination variables (e.g., recoveries, last_payment_amount). The model is strictly evaluated on information available at the exact moment of application.

**Weight of Evidence (WoE) & Information Value (IV):** Engineered custom financial ratios (like Loan-to-Income) and applied WoE binning. This transformed non-linear financial data into a standardized mathematical language of risk, feeding into a Logistic Regression baseline.

**Unsupervised Anomaly Detection:** Deployed Isolation Forests to scrub the training data of extreme statistical outliers and manual data-entry errors, providing the algorithms with a mathematically pristine decision boundary.

**Non-Linear Champion Models:** Implemented exhaustively tuned XGBoost (optimizing for the Precision-Recall Area Under Curve) and CatBoost (leveraging Ordered Target Statistics) to capture complex behavioral interactions.

**Threshold Optimization for ROI:** Abandoned the default 0.50 probability threshold. Wrote custom optimization loops to scan all possible thresholds and find the exact "Sweet Spot" that maximizes expected financial return over raw accuracy.
