# Car Price Prediction - CodeAlpha Data Science Internship

## About this project
This is my Task 3 submission for the CodeAlpha Data Science Internship. The goal was to build 
a model that can predict the selling price of a used car based on things like its present price, 
age, mileage, fuel type, and a few other features.

## Dataset
Used the `car data.csv` dataset provided by CodeAlpha - it has 301 entries with these columns:
Car_Name, Year, Selling_Price, Present_Price, Driven_kms, Fuel_Type, Selling_type, 
Transmission, and Owner.

## What I did
- Checked the data for missing values and duplicate rows, cleaned it up
- Did some EDA - plotted price distributions, checked correlations between features using 
  Seaborn heatmaps
- Created a new feature `Car_Age` from the Year column (thought this might be more useful 
  than raw year for the model)
- One-hot encoded the categorical columns (Fuel_Type, Selling_type, Transmission)
- Trained two models to compare - Linear Regression and Random Forest
- Evaluated both using MAE, MSE, RMSE and R²
- Also checked feature importance from the Random Forest model to see what actually 
  drives car prices

## Results
Linear Regression ended up performing better here (R² ≈ 0.753) compared to Random Forest 
(R² ≈ 0.61). Was a bit surprising since Random Forest usually does better, but with a smaller 
dataset like this, the simpler model held up fine.

Present Price turned out to be the biggest factor in predicting selling price, followed by 
Year, Car_Age, and Driven_kms.

## Tools/Libraries
Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn

## Notes
This was a good exercise in the full ML pipeline - cleaning data, engineering features, 
trying out different models, and actually interpreting what the model learned instead of 
just looking at the accuracy number.
