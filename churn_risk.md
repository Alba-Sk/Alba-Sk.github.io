### Project:  Churn reduction strategy
### *Project Overview*  

The telecom company aims to predict and prevent customer churn by leveraging customer data across multiple services, including landline, internet, security, tech support, and streaming. The project’s goal is to reduce churn rates through targeted promotions and special offers, enhancing customer retention.  

The project involves analyzing customer behavior, segmenting churn-prone clients, and crafting personalized retention strategies based on model predictions. The model also informs resource allocation and service improvements to optimize the customer experience.  

### 2. *Model Development*  
The churn prediction model was trained using customer data, including contract details, service usage patterns, and demographic information. A classification model was chosen to predict whether a customer will churn (i.e., terminate services) or remain with the telecom company.  

Data Preprocessing:    
Data cleaning, handling missing values, and encoding categorical variables.  
Feature selection to retain the most impactful predictors of churn.  

Model Selection:  
The model was trained using CatBoost due to its ability to handle categorical features and deliver high performance.
The model was validated using cross-validation techniques and tuned for optimal performance using hyperparameter tuning.

Training:
The model was trained for a sufficient number of epochs to ensure convergence and improvement in prediction accuracy.  
```javascript
# Prepare the Pool for training and validation
train_pool = Pool(features_resample, target_resample)
valid_pool = Pool(features_valid, target_valid)

# Define parameters for the CatBoost model (using params_cv defined earlier)
params_cv = {
    'iterations': 2000,
    'depth': 6,
    'learning_rate': 0.03,
    'l2_leaf_reg': 5,
    'loss_function': 'Logloss',
    'eval_metric': 'AUC',
    'random_seed': 42,
    'verbose': 0
}
# Train final model on the resampled dataset with evaluation set
final_model = CatBoostClassifier(**params_cv)

```

### 3. *Results*  
The model's performance metrics were evaluated to gauge its effectiveness in identifying churners and non-churners:  

ROC AUC: 93.33%    
This indicates excellent model performance, with the ability to distinguish churn clients from active clients effectively. The high ROC AUC suggests minimal false positives and negatives.

Accuracy: 88.20%  
The model correctly predicted churn or non-churn in about 88.20% of cases, demonstrating overall correctness.  

Precision: 75.74%  
The model predicts with a precision of 75.74%, meaning that 75.74% of the time, when the model predicts a customer will churn, it is correct. This helps reduce false positives, ensuring marketing resources are not wasted on clients who aren't likely to churn.  

Recall: 81.82%  
The model identifies 81.82% of actual churn clients. This high recall ensures that most churn-prone clients are correctly targeted for retention strategies.  

F1 Score: 78.66%  
The F1 score balances precision and recall, reflecting a reasonable trade-off between identifying churn clients and avoiding false positives.  
<img src="images/Corr_churn.jpg?raw=true"/>

### 4. *Business Recommendation*
The recommandation and Insights for the Telecom business as follow:  
1) <font color='blue'> Targeted Retention strategies </font> : - With hight score of recall 81.82% focus on developing targeted retention strategies for the clients predicted to churn. This could involve personalized offers, discounts, or reach in other services which the client doesnt access yet.  
2) <font color='blue'> Optimize resouce allocation </font> : - With precision 75.74% ensure that marketing and customer service are allocated effectivly. Focus efforts on clients predicted to churn while also maintaing the strategy to minimize engagement with the client which not  are a risk for churn.  
3) <font color='blue'> Customer Feedback </font> : Establish mechanisms to gather feedback from the clients who have churned to identify common pain points. This information improvements in service or products offering for the pottential churn client.  
3) <font color='blue'> Model monitoring </font> : Implementing a system  for ongoing monitoring  of the models over time because the clients behavior it changes and the date need to be realistically on time.
