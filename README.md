# Does the Structure of Seattle's Housing Market Track the 1936 Redlining Boundaries? 

> The following project seeks to determine whether historical redlining in Seattle can be predicted from modern-day housing data. Exploration of this question involves the implementation of unsupervised and supervised machine learning techniques, along with extensive data preprocessing.
---

## Project Overview

This project combines multiple data sets of modern-day Seattle housing data as well as historical redlining data to determine whether contemporary data is predictive of historical redlining grades from the Home Owners' Loan Corporation (HOLC). Data was gathered from three primary sources: the King County Assessor, the American Community Survey, and the Mapping Inequality Project from the University of Richmond. The project utilizes three predominant approaches when accomplishing this analayis:

1. **Data Joining/Preprocessing:** joining housing, demographic, and redlining data into a singular data set
2. **Unsupervised Learning:** applying unsupervised machine learning techniques for the purposes of exploratory data analysis
3. **Supervised Learning:** applying supervised machine learning techniques in predicting HOLC grades from housing and demographic factors

### Key Objectives

- **Objective:** To determine whether historical HOLC grades can be accurately predicted from contemporary Seattle housing data
- **Domain:** Housing/Urban Planning, Demography, Sociology
- **Key Techniques:** Exploratory Data Analysis, Principal Component Analysis, Clustering, Multi-Class Classification, Decision Trees, Random Forests, Boosting, Support Vector Machines

---

## Project Structure

```
PracticalHW4_5322/
│
├── README.md                                                   # Main project documentation
│
├── code/
│   ├── Final_DataPrepModeling.ipynb                            # Application of supervised machine learning techniques
│   ├── Final_RedliningJoin.ipynb                               # Joining housing and demographic data with historical redlining data
|   ├── PracticalHomework4_Modeling.ipynb                       # Application of unsupervised machine learning techniques
│   └── PracticalHomework4_Preprocessing_and_TractJoin.ipynb    # Joining and preprocessing of housing and demographic data
│ 
├── data/
│   ├── B02001_race.csv                                         # ACS data on racial demography in King County
|   ├── B19013_income.csv                                       # ACS data on median household income in King County
|   ├── B25003_tenure.csv                                       # ACS data on tenure status for King County residents 
|   ├── B25070_rent_burden.csv                                  # ACS data on rent burden for King County residents
|   ├── B25077_home_value.csv                                   # ACS data on median home value in King County
|   ├── acs_tract_clean.csv                                     # Combined and cleaned set of all ACS data
|   ├── seattle_parcels_with_tract.csv                          # Combined and cleaned parcel and tract data
│   └── seattle_tracts_holc.csv                                 # Seattle HOLC grade data 
│
└── reports/
    ├── Final_Intro_Methodology_References.docx                 # Final comprehensive report
    ├── RedliningMap.png                                        # HOLC grade maps of Seattle (contemporary vs. historical)
    └── blog.ipynb                                              # Blog post on unsupervised learning application


```


## How to Read/Run
1. Install all available data from data folder (if running models)
2. Execute/read the following files in order: `PracticalHomework4_Preprocessing_and_TractJoin.ipynb`, `PracticalHomework4_Modeling.ipynb`, `Final_RedliningJoin.ipynb`, `Final_DataPrepModeling.ipynb`
   
---

## Data

- **Source:** King County Assessor - (https://kingcounty.gov/en/dept/assessor), American Community Survey - (https://data.census.gov/table), University of Richmond Mapping Inequality Project (https://dsl.richmond.edu/panorama/redlining/)


## Methodology

- **Joining/Preprocessing:** Clean and join 3 primary data sources
  
- **Unsupervised Learning Models:** PCA, k-Means Clustering, Hierarchical Clustering, Matrix Completion
  
- **Supervised Learning Models:** Decision Trees, Random Forest, Boosting, Support Vector Machines
  
- **Scaling:** StandardScaler (z-score normalization)

---

## Analysis

This project applies unsupervised and supervised learning techniques to predict historical HOLC redlining grades for Seattle census tracts using contemporary housing and demographic data. Unsupervised methods were applied for the purposes of exploratory data analysis. Supervised methods were trained and evaluated on test observations. Overall supervised model performance was assessed using accuracy and error rates, weighted F1, and ROC-AUC. To avoid excessively long runtimes, support vector machines were applied to and cross-validated over a random subsample of the data (20,000 observations).

## Results

### Boosting (most accurate model)
| Metric | Value |
|--------|-------|
| Accuracy | 59% |
| Weighted F1 | 91% |
| ROC-AUC | 81% |

## Key Findings

- Primary drivers of variance include factors of race and income
- Tree-based methods far outperform SVMs in predictive accuracy
- HOLC grades often predicted as ranking higher compared to 1936 grades
  
## Authors

-  Jack Neton - [Github Link](https://github.com/netonj)
-  Jennifer Poling - [Github Link](https://github.com/jnplng)
-  Jacob Wilson - [Github Link](https://github.com/jwilsonc)

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## Acknowledgements

**Tools & Libraries Used**

- pandas, geopandas, numpy: Data manipulation and numerical computing

- scikit-learn: Machine learning algorithms and data standardization

- matplotlib & seaborn: Data visualization








