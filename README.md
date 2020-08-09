# machine_hack_melanomma


##  Problem statement
 The problem statement is to predict the melanoma tumor size based on various attributes. Melanomas present in many different shapes, sizes, and colors. 
 That’s why it’s tricky to provide a comprehensive set of warning signs. Melanoma, also known as malignant melanoma, is a type 
 of skin cancer that develops from the pigment-producing cells known as melanocytes. The primary cause of melanoma is ultraviolet 
 light (UV) exposure in those with low levels of the skin pigment melanin. The UV light may be from the sun or other sources, such 
 as tanning devices. 

Melanoma is the most dangerous type of skin cancer. Globally, in 2012, it newly occurred in 232,000 people. In 2015, 
there were 3.1 million people with active disease, which resulted in 59,800 deaths. Australia and New Zealand have the highest 
rates of melanoma in the world. There are also high rates in Northern Europe and North America, while it is less common in Asia, 
Africa, and Latin America. In the United States melanoma occurs about 1.6 times more often in men than women.

## Correlation matrix
![alt text](https://github.com/SHINE1607/machine_hack_melanomma/blob/master/images/correlation_heatmap.png)


## Model Used and Approach

### Pytorch
* The paramters are:
epochs used are: 1200
### model architecture is given below
![alt text](https://github.com/SHINE1607/machine_hack_melanomma/blob/master/images/architecture.png)

**mse** obatiend for test data: **5.481205342349706**, which is not a good one!!

 ### XGBRegressor
 * The model is trained using arbndomized search CV
 * the best parameterts obtaiend are:
{'colsample_bytree': 0.8,
  'learning_rate': 0.03,
  'max_depth': 7,
  'min_child_weight': 4,
  'n_estimators': 300,
  'nthread': 4,
  'objective': 'reg:linear',
  'silent': 1,
  'subsample': 0.7})
  * The mae score obtained for the validation data is **3.5504568039269024**
  
  The final model used XGBRegresor and score for final prediction, which got me score of **4.41** in leaderboard
