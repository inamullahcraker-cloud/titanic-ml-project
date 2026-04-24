## 🔄 Model Improvements & Experiments

### 📌 Feature Engineering

* Applied **log transformation** to reduce skewness in numerical features

* Performed **binning on Fare feature** using `KBinsDiscretizer` with:

  * `n_bins = 5`
  * `strategy = quantile`
  * `encode = ordinal`

* Observed that:

  * Log transformation + binning together did not significantly improve performance
  * **Fare binning alone contributed more effectively**

---

### 🤖 Model Experiments

#### 🔹 Logistic Regression (Baseline)

* Trained model using engineered features
* Evaluated performance after applying binning
* Used as baseline for comparison

---

#### 🔹 Random Forest Classifier (Improved Model)

* Switched to **Random Forest** for better non-linear modeling
* Applied **GridSearchCV** to find optimal hyperparameters

**Tuned Parameters (example):**

* Number of estimators
* Maximum depth
* Minimum samples split

---

### 📈 Final Results

| Model               | Technique                       | Accuracy  |
| ------------------- | ------------------------------- | --------- |
| Logistic Regression | Basic + Feature Engineering     | ~70–81%   |
| Random Forest       | GridSearchCV + Tuned Parameters | **80.1%** |

---

### ✅ Key Insights

* Feature binning (especially Fare) improved model stability
* Random Forest handled feature interactions better than Logistic Regression
* Hyperparameter tuning (GridSearchCV) led to optimal performance

---

## 🧠 Learning Outcome

* Understood impact of **feature skewness and transformations**
* Learned when **simpler transformations outperform complex ones**
* Gained experience with:

  * Feature engineering
  * Model comparison
  * Hyperparameter tuning
