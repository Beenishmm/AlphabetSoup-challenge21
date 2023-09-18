# AlphabetSoup-challenge21
Report on the Neural Network Model for AlphabetSoup Charity Funding Predictor

**Overview of the Analysis:**

The purpose of this analysis is to create a deep learning model capable of predicting whether applicants for funding from Alphabet Soup will be successful or not. This prediction is based on various features provided in the dataset, such as application type, affiliated industry sector, organization classification, use case for funding, organization type, active status, income classification, special considerations for application, and funding amount requested.

**Results:**

*Data Preprocessing*

- **Target Variable:** The target variable for our model is "IS_SUCCESSFUL," which indicates whether the funding was used effectively.

- **Feature Variables:** The feature variables include:
  - APPLICATION_TYPE
  - AFFILIATION
  - CLASSIFICATION
  - USE_CASE
  - ORGANIZATION
  - STATUS
  - INCOME_AMT
  - ASK_AMT

- **Removed Variables:** We removed the "EIN" and "NAME" columns as they were not relevant to our analysis.

- We also performed one-hot encoding using `pd.get_dummies()` to encode categorical variables.

*Compiling, Training, and Evaluating the Model*

- We designed a neural network model with two hidden layers, comprising 80 neurons in the first layer and 40 neurons in the second layer. We used the Rectified Linear Unit (ReLU) activation function for these layers.

- Unfortunately, we were unable to achieve the target model performance of greater than 75% accuracy.

- To improve model performance, we attempted to increase the number of neurons, layers, and also removed the "SPECIAL_CONSIDERATIONS" feature. However, these adjustments did not lead to better accuracy.

**Summary:**

In summary, our deep learning model did not meet the desired performance target. We recommend exploring alternative models, such as a Random Forest classifier, which may be more suitable for this classification problem. Additionally, the dataset may contain outliers or require further preprocessing to improve model performance. Further optimization attempts are necessary to achieve the desired accuracy level.
