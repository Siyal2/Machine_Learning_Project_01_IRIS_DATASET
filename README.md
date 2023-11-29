
# Code Overview
### Importing Essential Modules

- Pandas: For data manipulation and analysis.

- NumPy: For numerical operations and array manipulations.

- Matplotlib: For creating static, animated, and interactive visualizations in Python.

- Seaborn: A statistical data visualization library based on Matplotlib, providing a high-level interface for drawing attractive and informative statistical graphics.

- Scikit-learn: A machine learning library that provides simple and efficient tools for data analysis and modeling, including modules for model training, evaluation, and preprocessing.

These libraries collectively provide a comprehensive set of tools for data exploration, preprocessing, visualization, and machine learning model development in Python.

### Loading the Dataset :- 
In my project, I loaded the IRIS dataset using Pandas. The pd.read_csv('Iris.csv') command read the data from a CSV file named 'Iris.csv' into a Pandas DataFrame. I then removed the 'Id' column using :- 

- df = df.drop(columns=['Id'])

, as it is often unnecessary for analysis.

### Exploratory Data Analysis (EDA) :-

During EDA, I visualized key features of the dataset. For instance, I created histograms for features like Sepal Length, Sepal Width, Petal Length, and Petal Width to understand their distributions. Additionally, I generated scatterplots to explore relationships between different features, such as Sepal Length vs. Sepal Width.

### Data Preprocessing :-

I checked for null values using :- 

- df.isnull().sum() 

and confirmed that there were none. This is a crucial step to ensure the dataset's integrity. Since my dataset did not have missing values, there was no need for imputation.

### Splitting the Data :-

I used :- 

  - " train_test_split " 

 from Scikit-learn to divide the data into training and testing sets. This ensures that I have separate datasets for training the models and evaluating their performance.

 ### Choosing a Model :- 

In my project, I experimented with three different classification models: Logistic Regression, K-Nearest Neighbours, and Decision Tree. The choice of models depends on the nature of the problem and the characteristics of the data.


### Model Training :- 

I trained each model using the training set. For example, with logistic regression:-

 - model = LogisticRegression() 
 
 and 
 
 - model.fit(x_train, y_train). 

### Model Evaluation :- 

After training, I evaluated each model's performance on the testing set using 

- model.score(x_test, y_test) 
 The accuracy was printed as a metric to assess how well the models generalize to unseen data .

