# IT326-Project-Student-Stress-Factors

## Motivation
Student stress is a growing issue that affects mental health, academic performance, and overall well-being. We chose this dataset to gain a deeper understanding of the factors contributing to student stress. By analyzing the dataset, we aim to uncover insights that can help develop strategies for managing stress more effectively and improving students' overall health and performance.


## Missing values
In this step, we assessed the completeness and reliability of the dataset by checking for missing values. Our analysis confirmed that the dataset contains no missing values, ensuring its readiness for further analysis.


## Statistical measures
We conducted a statistical analysis of the dataset, examining measures of central tendency and dispersion for all numeric attributes. This included calculations of the mean, median, mode, midrange, range, quartiles, interquartile range (IQR), variance, and standard deviation. These measures provide a comprehensive overview of the data distribution.

## Graph visualization
Understanding the relationships between stress levels and different life factors is crucial for identifying how stress impacts daily life. An analysis of several graphs was conducted to examine the distribution, relationships, and variation of stress levels alongside a variety of attributes. While many factors were considered, a few key trends emerged. As stress levels increased, both depression and headache levels showed a clear rise. Similarly, the box plot of anxiety levels revealed a strong positive relationship, with higher stress linked to increased anxiety. In contrast, living conditions showed little variation with stress, though a few individuals experienced extreme cases. Finally, higher stress was slightly associated with lower academic performance.

## Outliers
We performed outlier detection using the Interquartile Range (IQR) method on all numeric attributes in the dataset. For each column, we calculated the IQR as the range between the first quartile (Q1) and the third quartile (Q3), and identified outliers as values falling below Q1 - 1.5 * IQR or above Q3 + 1.5 * IQR. After detecting the outliers, we removed them to retain a clean dataset with values within the acceptable range.

## Discretization
Discretization involves converting continuous data into discrete bins or categories, which can be beneficial for certain machine learning algorithms and analyses. This approach enhances interpretability, allowing for easier analysis and visualization. In our project, we employed the 'cut' function from the pandas library to discretize the anxiety_level, self_esteem, and depression columns, as their continuous nature was not necessary for our analysis. During this process, we defined bin edges and corresponding labels, ensuring that we accurately reflected the distribution of scores without distorting the underlying information. Finally, we compared the original values of these columns with the new categorical values to clearly illustrate the changes made.



## Min-Max Normalization
We applied Min-Max normalization to the dataset to scale the numeric features to a range between 0 and This process enhances the performance of machine learning models by ensuring that all features contribute equally to the distance calculations and prevents features with larger ranges from dominating the model's behavior. During normalization, we excluded the class label (stress_level) because it is the target variable we aim to predict, and including it would distort the scaling process. Additionally, we did not normalize the mental_health_history feature, as it is a binary attribute and normalization would not provide meaningful insights for its interpretation. We focused on the important numeric features while keeping the target variable unchanged, which helps prepare the data for analysis and modeling.

## Feature Selection
We chose the filtering selection method to focus on the most relevant attributes impacting student stress levels, thereby enhancing model performance and interpretability. We calculated the absolute correlation of each feature with the target variable (stress_level) and applied correlation analysis to select features based on their relationships. We set a threshold of 0.7 to identify features that have a strong correlation with the target variable, retaining only those that met this criterion. This selection process involved excluding the target variable itself and compiling a new DataFrame with the relevant features, allowing us to streamline our analysis and effectively identify key factors influencing student stress. If a threshold of 0.7 selected only 10 features—'self_esteem', 'bullying', 'sleep_quality', 'future_career_concerns', 'anxiety_level', 'depression', 'academic_performance', 'headache', 'safety', and 'basic_needs'—it indicates that those features have a strong correlation (greater than 0.7) with the target variable (stress_level), suggesting that these features are likely to be the most relevant predictors for stress levels in our dataset. After cleaning and filtering the dataset, we ended up with 10 columns, but we added the class label (stress_level) back in, resulting in a final dataset with 11 columns.


## Student Names
- Ghadeer Alnuwaysir 444200420
- Ghena Almogayad 444203140
- Raneem Nasser 444200975
- Ghaida Alotaibi 444200429
- Juri Alghamdi 444201188
