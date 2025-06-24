# Exploratory Data Analysis of Global Smoking Trends
# Introduction
Smoking remains one of the leading preventable causes of disease and death globally. Understanding smoking patterns across countries can help policymakers and health practitioners develop more targeted, data-driven health interventions. In this exploratory data analysis (EDA) project, I examined a global dataset of smoking-related statistics to uncover patterns, explore correlations between variables, and segment countries based on similarities in smoking behavior.

This analysis is particularly important for identifying high-risk regions and enabling the design of public health campaigns tailored to regional characteristics.

# Objective of the Project
The main objective of this project was to conduct a structured exploration of a global smoking dataset to:

Identify trends and anomalies in smoking prevalence across different countries.

Examine relationships between smoking-related variables.

Group countries into clusters based on similarities using unsupervised machine learning (K-Means clustering).

Generate actionable insights that could guide future research or policy initiatives.

# Data Overview
The dataset used for this project was a CSV file containing country-wise smoking-related statistics. Each row represents a country, while the columns include various metrics such as total smoking prevalence and other related indicators.

Notably, the dataset does not contain demographic data such as age or gender, nor does it include timestamps for temporal analysis. While this limits the depth of analysis, the available variables were sufficient for high-level trend analysis and clustering.

# Tools and Technologies Used
Python: Primary programming language

Pandas & NumPy: Data loading and manipulation

Matplotlib & Seaborn: Visualization and plotting

Scikit-learn: Data scaling and K-Means clustering

# Data Cleaning and Preprocessing
Upon loading the dataset, I began by inspecting its structure using functions like .head(), .info(), and .describe(). These revealed that the dataset was generally clean, with no major missing values.

# To prepare for analysis:

I standardized all column names by converting them to lowercase and replacing spaces with underscores to ensure consistency and code readability.

I confirmed that all relevant variables were numerical and suitable for statistical analysis.

I performed basic checks for duplicates and inconsistencies.

This preprocessing ensured that the data was well-structured and ready for exploration and modeling.

# Exploratory Data Analysis
1. Univariate Analysis
I started by examining individual variables:

Histograms were used to understand the distribution of smoking rates.

Descriptive statistics showed that smoking prevalence varied widely across countries, with some countries showing extremely high or low values.

I used boxplots to detect outliers and examine the spread of data for each numeric variable.

This step helped highlight countries with unusually high smoking rates, which would become important in later stages.

2. Bivariate and Correlation Analysis
Next, I explored the relationships between variables:

A correlation heatmap was created using Seaborn to visualize how variables interact with each other.

Strong positive correlations were found between total smoking prevalence and both male and female smoking indicators (where available), indicating a consistent smoking culture within countries.

Some variables had little to no correlation, suggesting that they might capture different aspects of smoking behavior or be affected by unrelated external factors.

# Clustering Analysis
To uncover hidden structures in the data, I applied K-Means Clustering, an unsupervised machine learning algorithm that groups data points based on similarity.

Process:
Feature Scaling:
I used StandardScaler to normalize the dataset so that all variables contributed equally to the clustering algorithm.

Choosing Number of Clusters:
I applied the Elbow Method, plotting the within-cluster sum of squares (WCSS) for different values of k. This helped me determine the optimal number of clusters (3).

Model Implementation:
I fit the K-Means model and assigned a cluster label to each country. These labels were then used to visualize countries grouped by similar smoking profiles.

Cluster Insights:
Cluster 0 consisted of countries with very high smoking rates—these are likely to be priority regions for health interventions.

Cluster 1 included countries with moderate smoking patterns, possibly undergoing lifestyle transitions.

Cluster 2 had countries with low smoking prevalence, likely due to strict regulations, cultural attitudes, or effective public health campaigns.

# Key Insights
Countries with high smoking prevalence tend to have consistent trends across different subgroups, pointing to systemic cultural or economic factors.

Clustering successfully revealed three distinct global patterns in smoking behavior.

Lack of demographic data (e.g., age, gender, socioeconomic status) limited deeper analysis, particularly around vulnerable populations.

No temporal data meant that trend evolution over time couldn’t be studied—this is a key area for future work.

# Recommendations
Based on this analysis, I propose the following:

Enrich the dataset by integrating external sources that contain demographic or temporal features for deeper segmentation and trend analysis.

Use clustering outputs to inform country-specific public health strategies and allocate resources more effectively.

Apply predictive models in future work to estimate health risks based on smoking behavior, especially if demographic and disease data become available.

# Conclusion
This project has demonstrated the value of exploratory data analysis in understanding complex public health issues such as smoking. Even with a limited dataset, it was possible to uncover meaningful patterns and segment countries into logical groups using statistical and machine learning techniques.

While this analysis provides a strong foundation, future efforts should focus on combining this dataset with demographic, economic, and time-series data to gain a more holistic view of global smoking trends. These insights can drive better public health policy and education efforts worldwide.

