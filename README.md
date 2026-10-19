Education Gap in the United States  
To measure the education gap between different socioeconomic classes in the United States. 

Project Overview
This project examines the relationship between the percentage of students eligible for free or reduced-price lunch and average school ACT scores. It uses school-level socioeconomic data and public school information to explore whether schools with higher lunch eligibility rates tend to have different average ACT scores.

Objective: To measure the education gap between different socioeconomic classes in the US. 

Domain: Education

Key Techniques: Linear Regression, Data Visualization

Project Structure
├── data/                 
|  ├──EdGap_data.xlsx
|  ├──ccd_sch.029_1617_w_1a_11212017.csv
├  └──education_prepared.csv
├── code/                
   └── education.ipynb
├── reports/              
├── requirements.txt      
└── README.md             

Data
Source: 
https://github.com/brian-fischer/DATA-5100/tree/main/weather
https://www.dropbox.com/scl/fi/fkafjk8902sq8ptxh94r2/ccd_sch_029_1617_w_1a_11212017.csv?rlkey=gucrdz5f6e38bezz2y3yalxbw&e=1&dl=0


Description:
EdGap_data.xlsx: An Excel dataset containing 7,000+ school-level records and 7 variables, including average ACT scores, free and reduced-price lunch eligibility, unemployment rates, adult college attainment, the percentage of children living in married-couple families, and median household income.

ccd_sch_029_1617_w_1a_11212017.csv: A CSV dataset containing 100,000+ school records and school information, including school names, district names, state, city, school level, school type, and school identification codes.

The datasets are cleaned and joined using school identification information. The final dataset is exported as education_prepared.csv in CSV format.

License: N/A

Analysis
The analysis is performed in the Jupyter Lab Notebook code/Education.ipynb, using Python. The notebook documents data preparation, cleaning, integration, and statistical analysis.

To reproduce the results, we analyzed the datasets in the following order:

1. Importing the data: Import the required Python libraries and load both datasets.
2. Inspect the data: Examine the dataset dimensions, column names, data types, and missing values.
3. Clean and prepare the duplicated data: Address missing values, check for duplicates, and prepare school identification fields for merging.
4. Merge the datasets: Combine the school socioeconomic data with school information from the Common Core of Data.
5. Prepare derived variables: Rename columns using lowercase snake_case and create any derived variables needed for analysis.
6. Perform statistical analysis: Calculate descriptive statistics and correlations, then conduct linear regression to examine the relationship between free/reduced-price lunch eligibility and average ACT scores.
7. Visualize and interpret results: Generate a scatterplot with a regression line, report the regression statistics, and summarize the findings and limitations.

Results
The regression graph shows a strong negative relationship between the percentage of students eligible for free or reduced-price lunch and average ACT scores (r) = -0.77. The regression slope was -8.35, meaning higher lunch eligibility was associated with lower ACT scores. The data had an R-squared value of 0.596, meaning that about 59.64% of the variation in average ACT scores was explained by the linear relationship with lunch eligibility. The p-value was reported as 0, which indicates strong statistical evidence. However, this analysis identifies an association and does not establish that lunch eligibility causes lower ACT scores.

This analysis suggests that schools with higher percentages of students eligible for free or reduced-price lunch tend to have lower average ACT scores. This relationship may reflect extensive socioeconomic differences between schools, but the analysis does not prove causation. Future research could examine additional factors, such as school location (rural vs. urban), student demographics, and access to academic resources, to better understand differences in ACT performance.