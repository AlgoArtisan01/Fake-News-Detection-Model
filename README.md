# Fake News Detection Using Machine Learning

<h3>The following steps outline the complete workflow of the project:</h3>


### 1. **Import Necessary Libraries**
The code begins by importing essential libraries for various tasks:
- `pip install pandas` for data manipulation.
- `pip install sklearn` for machine learning tasks.
- `pip install matplotlib` and `pip install seaborn` for data visualization.
- `pip install numpy` for numerical operations.

### 2. **Load the Datasets**
The code reads two CSV files containing fake and real news articles.

### 3. **Assign Labels**
Labels are assigned to the articles:
- `1` for fake news.
- `0` for real news.

### 4. **Drop Unnecessary Columns**
The code drops the `title`, `subject`, and `date` columns from the datasets, as they are not needed for the classification task.

### 5. **Merge and Shuffle the Dataframes**
The datasets are merged into one and shuffled to ensure a good mix of fake and real news articles.

### 6. **Preprocess the Text**
The text is preprocessed by:
- Converting it to lowercase.
- Replacing non-word characters with spaces.

### 7. **Split the Data into Training and Testing Sets**
The data is split into two sets:
- **80%** for training the model.
- **20%** for testing the model’s performance.

### 8. **Vectorize the Text Data**
The text data is converted into numerical data using the **TF-IDF Vectorizer**. This step is necessary because machine learning models require numerical input.

### 9. **Train a Logistic Regression Model**
A **Logistic Regression** model is trained on the training data to classify news articles as fake or real based on the features extracted from the text.

### 10. **Make Predictions**
The trained model is used to make predictions on the testing data.

### 11. **Evaluate Model Performance**
The accuracy of the model is calculated, and a **classification report** is generated, including:
- **Precision**
- **Recall**
- **F1-Score** for each class.

### 12. **Compute and Plot ROC Curve**
- The **ROC curve** and the **Area Under the ROC Curve (AUC)** are computed.
- The ROC curve is plotted, showing the true positive rate (sensitivity) against the false positive rate (1 - specificity) for different thresholds.

### 13. **Compute and Plot Precision, Recall, and F1-Score**
- The **precision**, **recall**, **F1-score**, and **support** for each class are computed.
- A bar graph is plotted to visualize the performance metrics for each class.

### 14. **Predict News Article Authenticity**
A function is defined to predict whether a news article is fake or real:
- The function preprocesses and vectorizes the input text.
- It makes a prediction using the trained model.
- The function returns either “Fake” or “Real” based on the prediction.

### 15. **Test the Function**
The function is tested by passing a sample news article, and it prints whether the article is predicted to be “Fake” or “Real”.
