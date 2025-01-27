# University Dataset Clustering Project

This project aims to analyze a university dataset using clustering techniques to segment institutions based on various attributes. The dataset includes features related to the institution's applications, acceptance rates, enrollment, expenses, faculty qualifications, and student demographics. The goal is to perform feature engineering, scaling, and clustering, and to interpret the results.

## Dataset Description

The dataset consists of the following columns:

- **Unnamed: 0**: The index or row number in the dataset.
- **Private**: Status of the institution (private or public).
- **Apps**: The number of applications received by the university.
- **Accept**: The number of applications accepted by the university.
- **Enroll**: The number of students accepted and enrolled in the university.
- **Top10perc**: Percentage of students from the top 10% of their high school class.
- **Top25perc**: Percentage of students from the top 25% of their high school class.
- **F.Undergrad**: Number of first-year undergraduate students.
- **P.Undergrad**: Number of upperclassmen (intermediate and senior undergraduate students).
- **Outstate**: Tuition fees for out-of-state students.
- **Room.Board**: Cost of room and board at the university.
- **Books**: Cost of books and study materials.
- **Personal**: Personal expenses for students.
- **PhD**: Percentage of faculty with a PhD.
- **Terminal**: Percentage of faculty with a terminal degree in their field.
- **S.F.Ratio**: Student-to-faculty ratio.
- **perc.alumni**: Percentage of alumni who contribute to the university.
- **Expend**: Expenditure per student by the university.
- **Grad.Rate**: Graduation rate of students.

## Data Preprocessing

1. **Missing Data**: No missing data in the dataset.
2. **Feature Engineering**: Applied One-Hot Encoding and Standard Scaler for scaling features.
3. **Outlier Detection**: Visualized potential outliers using boxplots.
4. **Feature Selection**: Used Variance Threshold for feature selection to remove low-variance features.
5. **Dimensionality Reduction**: Reduced dimensionality using Principal Component Analysis (PCA) with 2 dimensions.

## Clustering Models

### K-Means Clustering

- K-Means clustering was applied to group the universities based on the selected features.
- Silhouette Score: 0.4065, which indicates a moderate clustering quality.

### DBSCAN

- DBSCAN was also applied, but K-Means produced the most interpretable results.

## Results Interpretation

After applying the K-Means clustering model, the institutions were grouped into the following clusters:

- **Cluster 0**: Institutions with higher academic performance, more applications and acceptances, and higher expenses.
- **Cluster 1**: Institutions with moderate numbers of applications, acceptances, and expenses, and lower graduation rates compared to Cluster 0.

## Conclusion

This project demonstrates how clustering techniques such as K-Means and DBSCAN can be used to segment institutions based on various features. Further steps could include improving the clustering model with additional features or trying other clustering algorithms to validate the findings.

## Libraries Used

- Pandas
- Scikit-learn
- Matplotlib
- Seaborn
- NumPy

## How to Run

1. Clone the repository: `git clone <repository_link>`
2. Install the necessary dependencies: `pip install -r requirements.txt`
3. Run the Python script: `python clustering_analysis.py`

## License

This project is licensed under the MIT License.
