### Credit Card Fraud Detection 

#### 1. Importing Libraries
To begin, essential libraries such as `numpy` and `pandas` are imported for data manipulation and analysis. The `train_test_split` function from `sklearn.model_selection` is used to split the dataset into training and testing sets. `LogisticRegression` from `sklearn.linear_model` is used to create and train a logistic regression model, while `accuracy_score` from `sklearn.metrics` evaluates the model's accuracy.

#### 2. Loading the Dataset
The credit card fraud detection dataset is loaded into a Pandas DataFrame, providing a structured format for data manipulation and analysis.

#### 3. Displaying Dataset Information
- The `head()` and `tail()` methods are used to display the first and last five rows of the dataset, respectively, offering a glimpse of the data structure.
- `info()` method provides detailed information about the dataset, including the number of entries, column names, data types, and non-null values.
- `isnull().sum()` checks for missing values in each column, ensuring data completeness.
- `value_counts()` reveals the distribution of legitimate (class 0) and fraudulent (class 1) transactions, highlighting the class imbalance.

#### 4. Separating Legitimate and Fraudulent Transactions
The dataset is split into two subsets: legitimate transactions and fraudulent transactions. This separation allows for detailed analysis and comparison between the two types of transactions.

#### 5. Statistical Measures of the Data
- Descriptive statistics for the `Amount` column are computed for both legitimate and fraudulent transactions, providing insights into their distribution.
- Mean values for each feature are calculated and grouped by the `Class` column, facilitating a comparison of feature averages between legitimate and fraudulent transactions.

#### 6. Creating a Balanced Dataset
To address the class imbalance, a random sample of legitimate transactions equal to the number of fraudulent transactions is taken. This sample is then concatenated with the fraudulent transactions, creating a new balanced dataset. The class distribution and mean values grouped by class are re-evaluated for this balanced dataset.

#### 7. Splitting Features and Labels
Features (`X`) and labels (`Y`) are separated, with the `Class` column being designated as the label. This separation is essential for model training and evaluation.

#### 8. Splitting the Dataset into Training and Testing Sets
The balanced dataset is split into training and testing sets using an 80-20 split. Stratified sampling ensures that the class distribution is maintained in both the training and testing sets. The shapes of these sets are printed to confirm the split.

#### 9. Training the Logistic Regression Model
A logistic regression model is instantiated and trained using the training data. This model is chosen for its simplicity and effectiveness in binary classification tasks.

#### 10. Evaluating the Model
The trained model is used to make predictions on both the training and testing data. The accuracy of these predictions is calculated using `accuracy_score` and printed for both datasets. This evaluation provides insights into the model's performance and generalization capability.
