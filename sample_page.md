## Age Detection Project

### 1. *Project Overview*  
This project aims to assist the supermarket chain Good Seed with age detection for its buyers. The objective is to ensure that alcohol is sold only to customers who meet the legal age requirement while ensuring compliance with alcohol laws.

### 2. *Key Features*

* The checkout areas in Good Seed stores are equipped with cameras that capture images when a customer purchases alcohol.
* Computer vision techniques are used to estimate a person’s age from the captured images.
* The primary task is to develop and evaluate a model that can accurately verify a person’s age.
 

```javascript
img = show_image(41, labels, path_2)
plt.imshow(img)

```

### 3. *Model Development*

The model was trained for 20 epochs. 

Training MAE consistently decreased from 7.4339 years (epoch 1) to 3.1785 years (epoch 20), indicating good learning progress.  
Validation MAE improved from epoch 1 to epoch 10, reaching 6.969 years, but fluctuated afterward. It ended with an average validation MAE of 7.6512 years.  
The best validation MAE was 6.6419 years (epoch 17).  
A validation MAE of 7.65 years suggests a gap between training and validation performance, indicating potential overfitting or differences in dataset distribution.  

```javascript
# function to create the model
def create_model(input_shape):
    
    """
    It defines the model
    """
    
    # place your code here
    backbone_model = ResNet50(weights='imagenet', include_top=False, input_shape=input_shape)
    
    model = Sequential([
        backbone_model,
        GlobalAveragePooling2D(),
        Dense(128, activation='relu'),
        Dropout(0.5),
        Dense(1, activation='linear') # regression ouptput, age prediction
    ])
    model.compile(optimizer=Adam(learning_rate=0.0001),
                 loss='mean_squared_error',
                 metrics='mae')

    return model
```


<img src="images/age_det.png?raw=true"/>


### 4. *Business Recommendation*

The model demonstrates strong learning progress, with training MAE decreasing from 7.43 years to 3.18 years, showing it is effectively learning from the data. However, the validation MAE fluctuated and ended at 7.65 years, indicating potential overfitting or distribution mismatches between training and validation sets.  

For business application, improving model generalization will help ensure reliable predictions in real-world scenarios. By addressing these issues, the model can be fine-tuned to provide more consistent and accurate predictions, which can be crucial for decision-making in areas like age verification, customer segmentation, or personalized services. Enhancing model accuracy will contribute to better business outcomes, such as improved compliance, customer satisfaction, and targeted marketing.  
  
This project demonstrates the potential of computer vision for age verification, contributing to legal compliance and responsible retailing. 


