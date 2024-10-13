# Assignment - Retention Prediction

Retention prediction, also known as _customer churn prediction_, is a process in data science and business analytics that aims to identify and predict the likelihood of customers or users discontinuing their relationship with a company, product, or service. The term `retention` refers to the ability of a business to retain its customers over a specific period.

![churn-prediction.png](./ml/churn-prediction.png)

<aside>

**NOTE!** 

- This is an individual assignment.
- Be ready to do additional googling to complete this exercise, if necessary.
- Feel free to explore, experiment, and ask questions if you encounter any challenges. 
</aside>

##  Bank Customer Retention Prediction
In this assignment, you will build a Machine Learning model to predict whether a bank customer is likely to churn (exit) or not based on various features such as credit score, age, tenure, and more. The dataset contains information about the customers, including their demographics, banking behaviors, and whether they have exited the bank (the label to be predicted). The dataset consists of the following columns:

- **CustomerId**: Unique identifier for each customer
- **Surname**: Customer's last name
- **CreditScore**: Customer's credit score
- **Geography**: Customer's country of residence
- **Gender**: Customer's gender
- **Age**: Customer's age
- **Tenure**: Number of years the customer has been with the bank
- **Balance**: Account balance
- **NumOfProducts**: Number of bank products the customer uses
- **HasCrCard**: Whether the customer has a credit card (1 = yes, 0 = no)
- **IsActiveMember**: Whether the customer is an active bank member (1 = yes, 0 = no)
- **EstimatedSalary**: Estimated salary of the customer
- **Exited**: Whether the customer has exited the bank (1 = yes, 0 = no)


### Repository
[![Click to open the project](https://img.shields.io/static/v1?label=Open%20Project&message=Bank%20Customer%20Retention%20Prediction&color=blue)](https://github.com/kiboschool/ids-bank-customer-retention-prediction)


### TODOs

- Load the dataset into a DataFrame using Python's `Pandas` library.
- Explore the dataset to understand the features, data types, and potential missing values.
- Preprocess the data by handling missing values, converting categorical variables, and scaling numerical features (if needed).
- Split the data into training and testing sets.
- Choose a suitable classification algorithm (e.g., Logistic Regression, Random Forest, etc.) and train the model on the training data.
- Evaluate the model's performance on the testing data using appropriate metrics (e.g., accuracy, precision, recall, etc.).
- Fine-tune the model if necessary to achieve better results.
- Finally, use the trained model to predict customer churn on new data.
- Complete the assignment using the `notebook` in the repository.
    - Push your solution back to Github once completed.
- Submit your notebook on **[Gradescope](https://www.gradescope.com/courses/544001/assignments)**
    - Look for **Assignment - ML** under assignments

### HINTS
- Load the dataset into a DataFrame using Python's pandas library.
- Explore the dataset to understand the features, data types, and potential missing values.
- For data exploration, you can use Pandas methods like `head()`, `info()`, `describe()`, and `value_counts()`.
- To preprocess the data, consider using the `OneHotEncoder` from scikit-learn to encode categorical variables.
- Use scikit-learn's `LogisticRegression` or `RandomForestClassifier` for building the classification model.
- Evaluate the model's performance using metrics such as accuracy.
- Visualize the results and explore the important features that contribute to customer churn using matplotlib or seaborn.

## `Good Luck! 🤝`