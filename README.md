# houseprice_prediction
# House Price Prediction using Azure AutoML

## :rocket: Project Overview
In this project I have used Azure AutoML to predict house prices. Unlike traditional approaches in R or Python, where we need to manually select models and tune hyperparameters, **Azure AutoML automates the entire process**, making model selection and optimization much easier.

## 🔑 Key Features of Azure AutoML that helped in this project
- ✅ **Automated model selection** and hypertuning
- ✅ Preprocessing handled automatically
- ✅ Multiple models tested to chose the best one
  
## Dataset Info

 I have used a publicly available housing dataset which has properties such as:

 - **ID**
 - **Date**
 - **Price** (Target Variable)
 - **Bedrooms**
 - **Bathrooms**
 - **floors**
 - **sqft**
 - **year_built**
 - **condition** etc

## Steps followed to complete the project

### Step 1: Starting a new Automated ML Job
1. Logged into **Azure Machine Learning Studio**.
2. Under Automated ML, clicked **New Automated ML Job**.
3. Set Job name, experiment name and selected task type as **Regression**.

### Step 2: Selecting the dataset
1. Chose **source of dataset** as Local and uploaded the dataset.
2. Selected Azure Blob Storage as datastore type.
3. Selected target variable which is Price.

### Step 3: Validating and testing
1. Chosen validation type as Automatic.
2. Test Data as **Train-test Split** with 10% of test data.

### Step 4: Running the model
1. Selected Compute type and submitted model for job.

### Step 5: Evaluating the model
1. AutoML tested multiple models and chose best model based on the metrics.
2. VotingAssemble was the model chosen.

<Picture>
<img width="162" alt="metrics" src="https://github.com/user-attachments/assets/82c2167e-5e88-4ca7-a128-122e6c4b9c04" />

## Model Performance:
1. **R² Score is 88%**, which means the model explains 88% of the variance in house prices.
2. Predicted vs Ideal plot shows the **model predicted well**. (Refer images for the plot)
3. Although MAE and RMSE are high, it should be ok considering variablity in house prices.

## Key Points to be noted:
1. 💯 **Azure AutoML** reduced a lot of manual effort by eliminating the need of manual model selecting and hypertuning.
2. 💯 Model performance is great with **minimal effort**.
3. 💯 Difficult to achieve similar results manually. 
4. 💯 Useful for real world applications.
