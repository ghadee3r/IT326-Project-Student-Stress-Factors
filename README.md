# IT326-Project-Student-Stress-Factors

## Motivation
Student stress is a growing issue that affects mental health, academic performance, and overall well-being. We chose this dataset to gain a deeper understanding of the factors contributing to student stress. By analyzing the dataset, we aim to uncover insights that can help develop strategies for managing stress more effectively and improving students' overall health and performance.

## Student Names
- Ghadeer Alnuwaysir 444200420
- Ghena Almogayad 444203140
- Raneem Nasser 444200975
- Ghaida Alotaibi 444200429
- Juri Alghamdi 444201188

## Missing values
In this step, we are detecting the missing values to ensures that the dataset is complete and reliable for analysis, we noticed that our dataset has no missing values.

## Statistical measures
We performed statistical measures analysis on the dataset, including measures of central tendencies and dispersion of data, such as mean, median, mode, midrange, range, quartiles, interquartile range (IQR), variance, and  Standard deviation for all numeric attributes.

## Outliers
We performed outlier detection using the Interquartile Range (IQR) method on all numeric attributes in the dataset. For each column, we calculated the IQR as the range between the first quartile (Q1) and the third quartile (Q3), and identified outliers as values falling below Q1 - 1.5 * IQR or above Q3 + 1.5 * IQR. After detecting the outliers, we removed them to retain a clean dataset with values within the acceptable range.

## Feature Selection
We chose the filtering selection method to focus on the most relevant attributes impacting student stress levels, thereby enhancing model performance and interpretability. We calculated the absolute correlation of each feature with the target variable (stress_level) and applied correlation analysis to select features based on their relationships. We set a threshold of 0.7 to identify features that have a strong correlation with the target variable, retaining only those that met this criterion. This selection process involved excluding the target variable itself and compiling a new DataFrame with the relevant features, allowing us to streamline our analysis and effectively identify key factors influencing student stress. If a threshold of 0.7 selected only 9 features, it indicates that those features have a strong correlation (greater than 0.7) with the target variable (stress_level), suggesting that these features are likely to be the most relevant predictors for stress levels in our dataset.

