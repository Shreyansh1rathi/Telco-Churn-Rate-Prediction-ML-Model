# Telco-Churn-Rate-Prediction-ML-Model
## Project Overview

Customer churn is a key challenge for telecom companies, as losing customers directly impacts revenue. By predicting churn, businesses can take proactive steps such as improving services or offering retention benefits.The Telco Customer Churn dataset contains **7,043 records and 21 columns**, including customer demographics, services subscribed, billing details, and the target variable Churn (Yes/No).
The goal of this project is to analyze factors affecting churn and build predictive models that help improve customer retention strategies.

**`customerID`** → Unique customer identifier  
**`gender`** → Male / Female  
**`SeniorCitizen`** → 0 (No) / 1 (Yes)  
**`Partner`** → Whether customer has a partner (Yes/No)  
**`Dependents`** → Whether customer has dependents (Yes/No)  
**`tenure`** → Number of months the customer has stayed  
**`PhoneService`** → Yes/No  
**`MultipleLines`** → No phone service / No / Yes  
**`InternetService`** → DSL / Fiber optic / No  
**`OnlineSecurity`** → Yes / No / No internet service  
**`OnlineBackup`** → Yes / No / No internet service  
**`DeviceProtection`** → Yes / No / No internet service  
**`TechSupport`** → Yes / No / No internet service  
**`StreamingTV`** → Yes / No / No internet service  
**`StreamingMovies`** → Yes / No / No internet service  
**`Contract`** → Month-to-month / One year / Two year  
**`PaperlessBilling`** → Yes / No  
**`PaymentMethod`** → Electronic check / Mailed check / Bank transfer / Credit card  
**`MonthlyCharges`** → The amount charged monthly  
**`TotalCharges`** → The total amount charged  
**`Churn`** → Target variable (Yes = churn, No = stay)  


## Project Workflow: Telco Customer Churn Prediction

1. **Data Analysis**
   
   (a):- Explored the Telco Customer Churn dataset, reviewed customer demographics, service usage, billing info, and churn status.
   
   (b):-Identified numeric vs categorical features, handled missing values, and converted `TotalCharges` to numeric.

3. **Preprocessing Pipeline**
   
 Built a reusable pipeline:
 
    (a) Numeric features → imputation (median) + scaling.
    
    (b) Categorical features → imputation (most frequent) + one-hot encoding.
    
    (c) Combined using ColumnTransformer.

5. **Train-Test Split**
   
    (a) Split dataset into training (80%) and testing (20%).
   
    (b) Encoded Churn as binary (0 = No, 1 = Yes).

7. **Model Training & Evaluation**
   
    (a) Trained 4 models: **Logistic Regression, Random Forest, Gradient Boosting, XGBoost**.
   
    (b) Evaluated with **classification report, confusion matrix, accuracy, cross-validation score**.
   
    (c) **Logistic Regression** gave the best trade-off between accuracy and recall.

9. **Final Prediction System**

    (a) Combined preprocessing + best model into one pipeline.
   
    (b) Built an interactive system where users enter customer details (e.g., gender, tenure, contract, charges).
   
    (c) Model outputs **churn probability** and **final decision (Yes/No)**.

