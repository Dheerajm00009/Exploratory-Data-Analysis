***Exploratory_Data_Analysis_Using_Pandas***

***Overview***

This repository contains exploratory data analysis (EDA) performed on multiple datasets. The following analyses were conducted:

***Datasets Used***

**Titanic Dataset**: Focused on univariate preprocessing and bivariate analysis to study survival trends.
Visualized relationships between passenger demographics, ticket class, and survival rates.

**US Flights Dataset**: Demonstrated clustering techniques and time-based analyses using cluster maps and line plots.
Highlighted seasonal patterns and trends in flight data.

**Iris Dataset**: Used for multivariate analysis with pair plots to explore relationships between petal and sepal features across species.

***Data Preprocessing***

Key steps taken before analysis:

Read dataset into a pandas DataFrame for processing and analysis.

Initial Exploration: Used .head(), .sample(), .shape, .columns, .info, and .describe() to understand the structure, dimensions, and summary statistics of the data.

Missing Values: Checked for missing values using .isnull().sum() and handled appropriately during analysis.

Duplicate Data: Identified and removed duplicate rows using .duplicated().

***Univariate Analysis***

***Categorical Data***

Count Plot: Used sns.countplot() to visualize the frequency of categorical variables.

Value Counts: Explored the distribution of categorical data using df['column_name'].value_counts().

Pie Chart: Created pie charts using df['column_name'].value_counts() to represent categorical data as proportions.

_**Numerical Data**_

Histograms: Visualized the distribution of numerical columns using sns.histplot().

Distribution Plot: Used sns.distplot() with:

Only histogram (hist=True, kde=False) for raw distribution.

Only kernel density estimate (KDE) (kde=True, hist=False) for smoothed density visualization.

Box Plot: Displayed numerical data distributions and detected outliers using sns.boxplot().

_**Bivariate Analysis**_

_**Numeric-Numeric Relationships**_

Scatter Plot: Compared numerical variables using sns.scatterplot(). Enhanced visualization by adding hue, size, and palette to encode additional dimensions.

_**Categorical-Numerical Relationships**_

Distribution Plot: Used sns.distplot() with hue and palette to separate distributions based on a categorical variable.

Bar Plot: Visualized averages of numerical data by categories with sns.barplot(). Incorporated hue and palette for deeper insights.

Box Plot: Analyzed the spread of numerical data by categories using sns.boxplot() with options for hue differentiation.

_**Categorical-Categorical Relationships**_

Crosstab and Heatmap: Created distributions of categorical data using pd.crosstab() and visualized them as heatmaps with sns.heatmap().

Cluster Map: Applied hierarchical clustering to the crosstab data with sns.clustermap() to group similar categories.

Groupby and Bar Plot: Aggregated categorical data using pd.groupby() and represented results via bar plots.

_**Time-Based Analysis**_

Line Plot: Visualized changes in numerical variables over time using sns.lineplot(). Useful for detecting trends and seasonality.

_**Multivariate Analysis**_

Pair Plot: Used sns.pairplot() to explore relationships among all numerical features. Color-coded data points using hue for differentiation by categories (e.g., survival status in Titanic, species in Iris).

Heatmap and Cluster Map: Created heatmaps and cluster maps using aggregated or grouped data (pd.pivot_table(), pd.crosstab()) to identify patterns and correlations across multiple variables.

_**Conclusion**_

The Exploratory Data Analysis (EDA) conducted across multiple datasets provided valuable insights into various aspects of data relationships and distributions. The analysis revealed significant trends and patterns:

**Titanic Dataset**: Univariate and bivariate analyses uncovered how survival rates were influenced by factors like age, gender, and ticket class. Visualizations such as heatmaps, box plots, and crosstabs demonstrated the interplay between passenger demographics and survival likelihood.

**US Flights Dataset**: Cluster maps and line plots highlighted seasonal trends and passenger count variations across years and months, offering insights into temporal dynamics in the aviation industry.

**Iris Dataset**: Multivariate analysis through pair plots successfully illustrated the relationships between features like petal and sepal dimensions across different species, showcasing distinct clusters and separations.

This comprehensive EDA effectively used various visualization techniques to uncover hidden patterns, relationships, and actionable insights, enhancing the overall understanding of the datasets.

_**Future Work**_

To further build on this analysis, the following steps are recommended:

**Feature Engineering**: Create new derived features based on existing ones to better capture complex relationships and improve prediction potential for modeling tasks.

**Predictive Modeling**: Apply supervised and unsupervised machine learning algorithms on the datasets to predict outcomes like survival rates (Titanic Dataset) or flight delays (US Flights Dataset).

**Time Series Analysis**: For the US Flights Dataset, delve deeper into time-based data using advanced techniques such as ARIMA or seasonal decomposition to forecast future trends.

**Advanced Clustering**: Explore methods like DBSCAN or K-Means on the Iris Dataset to better understand species grouping and outliers.
