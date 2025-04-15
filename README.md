## Project Title: World Bank Data Analysis

This project performs exploratory data analysis (EDA), data preprocessing, and various statistical and visual analyses on a dataset containing World Development Indicators from India and China. The dataset covers several economic and social indicators from 1999 to 2023, and the analysis aims to identify trends, correlations, and outliers for each country.


---

### Dataset Description:
This dataset contains various indicators related to the development of two countries—India and China—from 1999 to 2023. It includes information across several socioeconomic and health-related metrics such as GDP, mortality rates, hospital beds, renewable energy consumption, and others. Each row corresponds to a country, a series name (which identifies the indicator), and the values across multiple years.

#### Columns:
1. **country_name**: The name of the country (India or China).
2. **country_code**: The country code (IND for India, CHN for China).
3. **series_name**: The name of the indicator, e.g., GDP, Mortality rate, etc.
4. **year_{1999}, year_{2000}, ..., year_{2023}**: These columns represent the value of the respective indicator for each year.

#### Indicators in the dataset:
Sure! Here's a simplified bullet list of the 19 indicators:

- **Access to electricity (% of population)**  
- **Renewable energy consumption (% of total energy use)**  
- **CO2 emissions (% change from 1990, excl. LULUCF)**  
- **Current health expenditure (% of GDP)**  
- **Hospital beds (per 1,000 people)**  
- **Life expectancy at birth (years)**  
- **Under-5 mortality rate (per 1,000 live births)**  
- **Physicians (per 1,000 people)**  
- **Adult literacy rate (% ages 15+)**  
- **Primary school enrollment (% gross)**  
- **Government spending on education (% of GDP)**  
- **GDP (current US$)**  
- **GDP per capita (current US$)**  
- **GNI per capita, PPP (current international $)**  
- **Inflation (consumer prices, annual %)**  
- **Unemployment (% of total labor force)**  
- **Mobile subscriptions (per 100 people)**  
- **Internet users (% of population)**  
- **Total population**


---

### Project Files:

1. **EDA_WorldBankData.ipynb**: This Jupyter notebook contains all the code for data preprocessing, exploratory data analysis (EDA), and outlier detection. It includes:
   - Data loading and cleaning
   - Reshaping and pivoting of the dataset
   - Correlation matrix analysis
   - Time-series analysis and visualizations
   - Regression analysis
   - Outlier detection using z-scores

2. **WorldDevelopmentData_lNDCHN.csv**: This CSV file contains the World Development Indicators for India and China, with columns such as country names, country codes, series names (for different indicators), and the years from 1999 to 2023.

3. **README.md**: This file contains the description of the project, instructions for running the analysis, and an overview of the methods used.

---

### Data Preprocessing

The following steps are taken to clean and preprocess the data:
1. **Importing Libraries**: Libraries like `pandas`, `matplotlib`, `seaborn`, `plotly`, and `scipy` are used for data manipulation, visualization, and statistical analysis.
2. **Loading the Dataset**: The dataset is loaded into a pandas DataFrame and columns are renamed for easier understanding.
3. **Handling Missing Data**: Missing values are handled using forward-fill and backward-fill methods.
4. **Reshaping Data**: The dataset is reshaped from wide to long format for better analysis and insights.
5. **Data Cleaning**: Stripped leading and trailing spaces from columns for consistency.

---

### Exploratory Data Analysis (EDA)

The main focus of the EDA includes:
1. **Descriptive Statistics**: Summary statistics for each country (India and China).
2. **Interactive Visualizations**: Boxplots for a visual understanding of data distribution over the years.
3. **Correlation Analysis**: Heatmaps to visualize the correlation between various indicators for India and China.
4. **Trend Analysis**: Line plots to observe trends of economic indicators like GDP, unemployment, life expectancy, and more over time.
5. **Regression Analysis**: Scatter plots with regression lines to understand relationships between indicators such as GDP vs. internet usage and CO2 emissions vs. renewable energy consumption.

---

### Outlier Detection

Z-scores are used to detect outliers in the dataset, with any z-score greater than 3 being considered an anomaly. Anomalies are checked for various features like:
- Hospital beds per 1,000 people
- Unemployment rate
- GDP growth
- Renewable energy consumption

---

### Visualizations

Several visualizations have been created to showcase the findings:
1. **Boxplots**: To analyze the distribution of data for each indicator.
2. **Heatmaps**: For correlation matrices of economic indicators for both India and China.
3. **Time-Series Plots**: To visualize trends in indicators over the years.
4. **Regression Plots**: To show relationships between various indicators like GDP, life expectancy, and internet usage.
   
---

### Dependencies

The following Python libraries are required:
- pandas
- matplotlib
- seaborn
- plotly
- scipy

You can install them using pip:
```bash
pip install pandas matplotlib seaborn plotly scipy
```

---
### Insights

Here are the **top 5 insights** comparing China and India across various development indicators:

1. **Healthcare Disparity Despite Similar Spending**  
   China exhibits significantly **better health outcomes**—higher life expectancy (~78 years), lower under-5 mortality, and better hospital infrastructure—despite spending a **smaller percentage of GDP** on healthcare than India. This suggests **greater efficiency and accessibility** in China’s healthcare system.

2. **Renewable Energy Leadership in India**  
   India leads in **renewable energy consumption** (35–40% vs. China’s 15–20%) and shows a **strong negative correlation with CO₂ emissions** (-0.92), indicating that **India’s clean energy transition** is more directly tied to improving environmental and health outcomes.

3. **Digital Connectivity and Economic Growth**  
   In both countries, **internet usage strongly correlates with GDP**, but China shows a **tighter and more linear relationship**, suggesting a more **strategic integration of digital infrastructure** into its economic development.

4. **Education Impacting Health Outcomes**  
   A **positive correlation exists between literacy and life expectancy** in both countries. However, **China's higher literacy rate (91–97%)** supports its superior life expectancy (~78.5 years vs. India’s ~68 years), showcasing the **direct benefits of stronger educational outcomes**.

5. **Hospital Infrastructure Trends Diverge**  
   China has **consistently improved** hospital bed availability (1.7 to 5 beds per 1,000 people), in contrast to **India’s decline** (from 2.1 to 1.6), despite India’s growing GDP. This underscores a **critical gap in healthcare capacity expansion** in India.

---
