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

In the defined neural network model for the AlphabetSoup Charity Funding Predictor, it's important to evaluate its performance based on the chosen architecture:

**Evaluation:**

1. **Input Layer:**
   - The input layer is dynamically determined by the shape of the input data, so it adjusts automatically to the number of features in the dataset. This flexibility is helpful as it accommodates different datasets without the need for manual specification.

2. **First Hidden Layer:**
   - The first hidden layer consists of 80 neurons with a sigmoid activation function. Using sigmoid introduces non-linearity to the model, which can be beneficial for capturing complex relationships in the data. However, the choice of 80 neurons may require further investigation and tuning. A larger number of neurons may lead to overfitting, while a smaller number may result in underfitting.

3. **Second Hidden Layer:**
   - The second hidden layer includes 40 neurons with the ReLU activation function. ReLU is an excellent choice for hidden layers, as it addresses the vanishing gradient problem and is computationally efficient. The choice of 40 neurons should be evaluated through experimentation. It's important to monitor the model's performance and consider increasing or decreasing the number of neurons based on validation results.

4. **Output Layer:**
   - The output layer consists of a single neuron with a sigmoid activation function. This is a suitable configuration for binary classification tasks. The sigmoid activation function ensures that the model produces output in the [0, 1] range, representing the probability of a positive outcome (in this case, successful funding). 

In summary, the neural network architecture you've defined is a reasonable starting point for the problem. However, the success of the model also depends on other factors, such as data quality, preprocessing, and hyperparameter tuning. It's essential to evaluate the model's performance on both training and validation data, and potentially use techniques like cross-validation to fine-tune the hyperparameters, including the number of neurons and layers. Additionally, monitoring metrics like accuracy, precision, recall, and F1-score can provide a more comprehensive assessment of the model's effectiveness in classifying successful and unsuccessful funding applications.

- Unfortunately, we were unable to achieve the target model performance of greater than 75% accuracy.

- To improve model performance, we attempted to increase the number of neurons, layers, and also removed the "SPECIAL_CONSIDERATIONS" feature. However, these adjustments did not lead to better accuracy.

**Summary:**

In summary, our deep learning model did not meet the desired performance target. We recommend exploring alternative models, such as a Random Forest classifier, which may be more suitable for this classification problem. Additionally, the dataset may contain outliers or require further preprocessing to improve model performance. Further optimization attempts are necessary to achieve the desired accuracy level.
