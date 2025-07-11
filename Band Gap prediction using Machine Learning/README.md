# Band Gap Prediction with XGBoost

This folder contains two Python scripts for training and testing machine-learning models that predict the band gap of compounds:

- **`BandGap_Model_Training.py`**  
  Loads an experimental band-gap dataset, featurizes compositions using Magpie elemental properties, trains:  
  1. A **classifier** to distinguish metals (zero bandgap) from non-metals (non-zero bandgap)  
  2. A **regressor** to predict the band gap (eV) for non-metal compounds  
  It evaluates both models, plots performance figures, and saves the trained models as `XGBClassifier.joblib` and `XGBRegressor.joblib`.

- **`BandGap_Model_Testing.py`**  
  Loads the saved classifier & regressor, featurizes a set of custom chemical formulas, classifies each as metal/non-metal, and predicts the band gap for the non-metal ones.  
  It reports RMSE and mean absolute deviation on our custom test set. See Table. 4 in the report for results.

---

## Prerequisites

- Python 3.8+  
- Recommended: create and activate a virtual environment:

  ```bash
  python3 -m venv venv
  source venv/bin/activate     # Linux / macOS
  venv\Scripts\activate.bat    # Windows

# Reference

   [1]  Y. Zhuo, A.M. Tehrani, and J. Brgoch. Predicting the band gaps of inorganic solids by machine learning. J. Phys. Chem. Lett., 9:1668–1673, 2018.
