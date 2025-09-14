# flight-price-prediction
✈️ Machine Learning project to predict airline ticket prices using regression models, with feature engineering, categorical encoding, and model evaluation.

# ✈️ Flight Price Prediction

This project predicts airline ticket prices based on flight details such as airline, class, number of stops, source city, destination city, duration, and days left before departure.  
It applies data preprocessing, exploratory data analysis (EDA), and machine learning models to build a reliable price prediction system.

---

## 📊 Dataset
The dataset includes flight details with the following features:
- **Airline**
- **Source City**
- **Destination City**
- **Departure Time** (Morning, Afternoon, Evening, Night)
- **Arrival Time**
- **Stops** (zero, one, two or more)
- **Class** (Economy, Business)
- **Duration**
- **Days Left** (days before flight booking)
- **Price** (target variable)

---

## 🔍 Exploratory Data Analysis
- Histograms and KDE plots to check distributions and skewness.  
- Boxplots for outlier detection.  
- Price comparisons by class, airline, stops, and routes.  
- Scatter plots showing relationships (e.g., price vs. duration, price vs. days left).  

---

## 🛠 Preprocessing
- Handling skewness (log/yeo-johnson transformations).  
- Outlier detection and removal using boxplots/IQR.  
- Encoding categorical features:
  - **Ordinal Encoding** for ordered categories (class, departure/arrival period, stops).  
  - **One-Hot Encoding** for nominal features (airline, source city, destination city).  
- Train-test split for model evaluation.  

---

## 🤖 Models
- **Linear Regression** (baseline)  
- Future improvements: **Random Forest**, **XGBoost** for non-linear patterns.  

---

## 📈 Results (Linear Regression)
- **MAE:** 4509.31  
- **MSE:** 46,787,872.20  
- **RMSE:** 6840.17  
- **R²:** 0.9083  

✅ Model explains **~91% of price variation**, with average prediction error around **₹4500–₹6800**.  

---

## 🚀 How to Run

```bash
# Clone repo
git clone https://github.com/<your-username>/flight-price-prediction.git
cd flight-price-prediction

# Install dependencies
pip install -r requirements.txt

# Run training
python src/train.py
