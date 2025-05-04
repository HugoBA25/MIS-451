# Titanic Dataset - Week 2 Assignment

## 1. Dataset Description:
The Titanic dataset from Seaborn contains the following features:

- **survived**: Survival status (0 = No, 1 = Yes)
- **pclass**: Ticket class (1 = 1st, 2 = 2nd, 3 = 3rd)
- **sex**: Gender of the passenger
- **age**: Age of the passenger
- **sibsp**: Number of siblings or spouses aboard the Titanic
- **parch**: Number of parents or children aboard the Titanic
- **fare**: Passenger fare (in British pounds)
- **embarked**: Port of embarkation (C = Cherbourg, Q = Queenstown, S = Southampton)
- **class**: Class of travel (1st, 2nd, 3rd)
- **who**: Man, woman, or child
- **adult_male**: Whether the passenger is an adult male
- **deck**: Deck level
- **embark_town**: Town of embarkation
- **alive**: Whether the passenger survived (1 = Yes, 0 = No)
- **alone**: Whether the passenger was alone on board (1 = Yes, 0 = No)

## 2. Exploratory Data Analysis (EDA):
In this section, I performed the following steps:

- **Checked for missing values**: 
  - Identified missing values in columns like `age`, `embarked`, and `deck`, and addressed them.
  - Missing `age` values were filled with the median, and missing `embarked` values were filled with the mode.

- **Generated descriptive statistics**: 
  - Generated statistical summaries for numerical features such as `age`, `fare`, `sibsp`, `parch`, etc.
  - This step helped understand the central tendencies (mean, median) and the spread (standard deviation) of these features.

- **Visualized the distribution of variables**: 
  - Created **histograms** and **boxplots** for numerical variables like `age` and `fare` to understand their distributions and identify potential outliers.
  - Plotted survival rates based on features like `sex`, `pclass`, and `age`.

- **Analyzed the correlation between survival and other variables**: 
  - Examined relationships using visualizations such as bar charts and scatter plots.
  - Observed that females had a significantly higher survival rate compared to males.
  - Passengers in 1st class had a higher survival rate than those in 2nd and 3rd classes.

### Insights:
- **Gender impact**: More males than females were aboard the Titanic, but females had a much higher survival rate (approximately 70% for females vs. 20% for males).
- **Ticket class**: Passengers in **1st class** had a significantly higher survival rate compared to those in **2nd** and **3rd class**.
- **Age distribution**: The dataset showed more children and elderly passengers who had a higher survival rate, especially children under 10 years old.
- **Fare analysis**: The higher the fare, the better the chances of survival, especially for first-class passengers.
- **Embarked port**: Most passengers embarked from **Southampton (S)**, followed by **Cherbourg (C)** and **Queenstown (Q)**. However, the port of embarkation did not strongly influence survival rates.

## 3. Data Transformation:
The following transformations were made to prepare the data for machine learning:

- **Handled missing values**: 
  - Missing `age` values were imputed with the median, and missing `embarked` values were filled with the mode.
  
- **Converted categorical variables**: 
  - The `sex` column was transformed into numerical values (0 for male, 1 for female).
  - The `embarked` column was one-hot encoded to create three binary columns representing each embarkation port (`C`, `Q`, and `S`).

- **Feature engineering**: 
  - The `embarked` feature was transformed into three binary columns using one-hot encoding.
  - `age` and `fare` were scaled and standardized where necessary to ensure they are properly handled by machine learning models.

## 4. Conclusion:
- **Data is clean**: After performing exploratory data analysis and transforming the data, all missing values have been handled, categorical variables have been encoded, and the dataset is now ready for machine learning.
- **Ready for modeling**: The dataset is prepared for building predictive models that will estimate survival based on these features.

## How to Run This Notebook:
1. Clone this repository to your local machine or open it in Google Colab.
2. Ensure you have all the required libraries installed, such as `pandas`, `seaborn`, `matplotlib`, and `sklearn`.
3. Run the notebook step-by-step to see the EDA and data transformation steps in action.
4. In the next step, I will begin building predictive models based on this transformed data.
