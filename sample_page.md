## Age Detection Project

### 1. **Project Overview:** 
This project aims to assist the supermarket chain Good Seed with age detection for its buyers. The objective is to ensure that alcohol is sold only to customers who meet the legal age requirement while ensuring compliance with alcohol laws.

### 2. Key Features

* The checkout areas in Good Seed stores are equipped with cameras that capture images when a customer purchases alcohol.
* Computer vision techniques are used to estimate a person’s age from the captured images.
* The primary task is to develop and evaluate a model that can accurately verify a person’s age.
 

```javascript
if (isAwesome){
  return true
}
```

### Model Development

To train the model, a dataset consisting of photographs labeled with the respective ages of individuals was used.

Results & Performance

Model Learning Progress:
* The validation MAE decreased from 14.1033 to 13.4243, indicating slight improvement.

Loss Reduction:
* Both training and validation loss (MSE) decreased, showing that the model is learning.

Challenges:
* The Mean Absolute Error (MAE) of 13 years suggests a high error margin, likely due to overfitting, insufficient epochs, or a broad age range (1-100 years old)

```javascript
if (isAwesome){
  return true
}
```

### 3. Support the selection of appropriate statistical tools and techniques

<img src="images/Corr_churn.jpg?raw=true"/>

### 4. **Result interpretation**

<font color='red'>**Roc Auc 93.33%**</font>:
 * This indicated excellent model performance in distinguishing between churn client and active clients, showing a strong ability to predict the positive class (churn clients) without a hight positive rate.
 
 <font color='red'> **Accuracy 88.20%**</font>:
 * This reflect overall correctness of the model, indicating that approximately  88.20% were correct.
 
 <font color='red'>**Precicion 75.74 %**</font>:
 * The model predict the client will churn , and prediction rate is 75.74%. The hight rate precision is important to minimize false positive.
 
 <font color='red'> **Recall 81.82%**</font>:
 * This parameter indicates that 81.82% of actual churn clients were correct identified by the model. 
 
 <font color='red'> **F1 Score78.66 %**</font>:
 * This parameter provide a balance between precison and recall, indicating a reasonable trade between two metrics. This mscore show that the model preform well on identifying churn clients.

### 5. Business Recommendation

The recommandation and Insights for the Telecom business as follow:
1) <font color='blue'> **Targeted Retention strategies** </font> : - With hight score of recall 81.82% focus on developing targeted retention strategies for the clients predicted to churn. This could involve personalized offers, discounts, or reach in other services which the client doesnt access yet.
2) <font color='blue'> **Optimize resouce allocation** </font> : - With precision 75.74% ensure that marketing and customer service are allocated effectivly. Focus efforts on clients predicted to churn while also maintaing the strategy to minimize engagement with the client which not  are a risk for churn.
3) <font color='blue'> **Customer Feedback** </font> : Establish mechanisms to gather feedback from the clients who have churned to identify common pain points. This information improvements in service or products offering for the pottential churn client.
3) <font color='blue'> **Model monitoring** </font> : Implementing a system  for ongoing monitoring  of the models over time because the clients behavior it changes and the date need to be realistically on time.
  
This project demonstrates the potential of computer vision for age verification, contributing to legal compliance and responsible retailing. 

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).
