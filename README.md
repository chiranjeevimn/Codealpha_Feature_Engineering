# Codealpha_Feature_Engineering

Here is a breakdown of the methods and steps included in the provided code:

1. **Data Loading:**
   - `datasets.load_breast_cancer()`: Loads the Breast Cancer dataset from scikit-learn.

2. **Data Manipulation and Preprocessing:**
   - Introduces missing values in the dataset for demonstration purposes.
   - `SimpleImputer(strategy='mean')`: Imputes missing values with the mean of the respective columns.
   - No explicit handling of outliers is demonstrated in this example.

3. **Normalization or Scaling:**
   - `StandardScaler()`: Scales the data to have zero mean and unit variance.

4. **Feature Engineering:**
   - Adds an artificial time column to the dataset.
   - Creates time-based features such as 'month' and 'day_of_week'.
   - Computes rolling statistics (mean and standard deviation) for each feature over a specified window.
   - Applies additional transformations like logarithm and square root to specific features.
   - Drops rows with missing values introduced during rolling statistics computation.

5. **Data Splitting:**
   - `train_test_split()`: Splits the dataset into training and testing sets.

6. **Pipeline with PCA and RandomForestClassifier:**
   - `Pipeline`: Constructs a pipeline for sequential application of transformations and a final estimator.
   - `SimpleImputer(strategy='mean')`: Imputes missing values in the pipeline.
   - `StandardScaler()`: Scales the data within the pipeline.
   - `PCA(n_components=10)`: Performs Principal Component Analysis with 10 components.
   - `RandomForestClassifier(random_state=42)`: Utilizes a RandomForestClassifier as the final estimator.

7. **Model Fitting:**
   - `pipeline.fit(X_train, y_train)`: Fits the pipeline to the training data.

8. **Performance Evaluation:**
   - `pipeline.predict(X_test)`: Predicts the labels on the test set.
   - `accuracy_score(y_test, y_pred)`: Computes the accuracy of the model on the test set.
   - Prints the accuracy score as a performance metric.

These steps collectively demonstrate a comprehensive workflow for data preprocessing, feature engineering, model building, and performance evaluation using scikit-learn in Python.
