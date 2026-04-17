#  Spaceship Titanic ML Project

##  Overview
This project aims to predict whether a passenger was transported to another dimension using machine learning models.

The project focuses on building a clean ML pipeline, applying feature engineering, and evaluating models using cross-validation and test sets.

---

## 📊 Dataset
- Competition: Spaceship Titanic (Kaggle)
- Link: https://www.kaggle.com/competitions/spaceship-titanic

---

## ⚙️ Data Preprocessing

- Split `Cabin` into:
  - Deck
  - Num
  - Side
- Converted boolean features:
  - VIP → 0/1
  - CryoSleep → 0/1
- Handled missing values using `SimpleImputer`
- Used `ColumnTransformer` for structured preprocessing

---

##  Feature Engineering

- **TotalSpend**:
  Sum of all spending columns:
  - RoomService
  - FoodCourt
  - ShoppingMall
  - Spa
  - VRDeck

- **HasSpending**:
  Indicates whether a passenger spent any money

---

## 🤖 Models Used

- Logistic Regression
- Decision Tree
- Support Vector Classifier (SVC)
- K-Nearest Neighbors (KNN)

Final model:
- **Voting Classifier (Soft Voting Ensemble)**

---

## 🔬 Evaluation

- Used **5-Fold Cross Validation**
- Compared CV score with Test score
- Avoided data leakage using pipeline

---

## 📈 Results

- **Cross Validation Accuracy:** ~80.07%
- **Test Accuracy:** ~80.39%
- **Kaggle Public Score:** **79.47%**

---

## ❌ What Did NOT Work

- Log Transformation → Decreased performance
- IQR Outlier Handling → Decreased performance
- Random preprocessing without validation

---

##  Key Learnings

- Clean pipeline improves model reliability
- Feature engineering is more impactful than random preprocessing
- Cross-validation is essential for proper evaluation
- Avoid data leakage by keeping all transformations inside pipeline

---

##  Future Improvements

- Add more feature engineering:
  - Group-based features
  - Route (HomePlanet + Destination)
- Try advanced models:
  - RandomForest
  - ExtraTrees
  - XGBoost / LightGBM
- Hyperparameter tuning



