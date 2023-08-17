# bdda1
# GROUP 12

A machine learning pipeline that uses a RandomForestClassifier to predict whether a product will go on backorder or not. The code involves data preprocessing, model training, and performance evaluation. 

Here's how I've progressed through the pipeline:

1. **Data Loading and Exploration:**
   - I load a CSV file containing my data into a pandas DataFrame (`df`) and showcase its initial rows along with some basic insights.
   - I visualize the distribution of the target variable (`went_on_backorder`) by utilizing a bar plot.

2. **Feature Analysis:**
   - I examine the impact of the `lead_time` feature on backorders through a bar plot.
   - I create a histogram to gain a clearer picture of the distribution of the `lead_time` feature.

3. **Data Preprocessing:**
   - I convert binary categorical variables (`'potential_issue'`, `'deck_risk'`, etc.) from text-based values ('Yes' and 'No') into numerical equivalents (0 and 1).
   - I handle any missing values in the `'perf_6_month_avg'` and `'perf_12_month_avg'` columns by replacing them with the median value.

4. **Data Splitting and Model Training:**
   - I partition the data into training and testing subsets using the `train_test_split` function.
   - I set up a pipeline that involves `SimpleImputer` to fill missing values and a `RandomForestClassifier` model.
   - I proceed to train the pipeline using the training data.

5. **Model Evaluation:**
   - I generate predictions for the test data using the trained pipeline and calculate the accuracy score.
   - I compute the accuracy and produce a classification report using the `classification_report` function.
   - I craft a Receiver Operating Characteristic (ROC) curve to visualize the model's performance, calculating the area under the curve (AUC) to gauge its effectiveness.

6. **ROC Curve Analysis:**
   - I create a function designed to plot the ROC curve and AUC for a specified model.
   - I utilize this function to generate the ROC curve for the Random Forest model and determine the corresponding ROC AUC score.
