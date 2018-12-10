## Employee Retention Study  ![picture](./InputFiles/Teamwork.jpg)

*Steve Bramhall, Hayley Horn*


Employee attrition has been a costly problem for a long time, looking back we see that The Journal of Applied Psychology published first empirical study regarding turnover in 1925 (isbn 978-1-4338-9042-0) and articles dating back to 1917. This means there has been 100 years of new ideas and approaches on addressing employee churn. This project applies a Data Science approach to this problem and provides an example on how clients can have the best visibility for this area of talent management.


#### The purpose of this case study was to predict employee attrition. Goals include:
- Exploratory Data Analysis (EDA)
- Determine key contributors to attrition from a training data set
- Identify any job role trends
- Point out other interesting findings
- Build a model to predict attrition
- Provide data visualization in the final presentation


### CODEBOOK

#### PROJECT FILES
* .gitignore - lists local files specific to the team member, version control not needed
* DDSCaseStudy2.Rproj - Rstudio project file
* AttritionStudy.Rmd - main program
* AttritionStudy.html - html output from the main program

#### INPUT FILES: (Folder = InputFiles)
1. CaseStudy2.csv - information about 1170 employees
2. CaseStudy2Validation.csv - information about 300 employees
3. DataDictionary.csv - data dictionary

#### OUTPUT FILES: (Folder = OutputFiles)
* DFPred.csv - predictions of validation data from model

#### LIBRARIES
* dplyr      - for string functions
* ggplot2    - for plots
* kableExtra - for table formatting
* knitr      - for presenting in html
* Hmisc      - for describing data
* caret      - for classification & regression training
* mlr        - for machine learing
* class      - for classification funtions
* corrplot   - for correlation matrix
* data.table - for table creation for using one_hot
* mltools    - for one_hot dummy creation
* gridExtra  - for plots formatting  

#### DEFINITIONS
* Variable - Factor, Feature

#### VARIABLES
##### writePredFile - *flag to write to the prediction file predFile.csv*
##### train - *data frame of employee training data from csv file*
##### validation - *data frame of employee validation data from csv file*
##### alldata, plotalldata - *data frame of the train+validation data*
##### AgePlot, Genderplot, EducationPlot, etc - *basic histograms of the data field, includes both training and validation data*
##### percentData - *reused for identifying the percentage of attrition for a category*
##### data1...data5 - *data frames used for the correlation plots, plots were split for readability*
##### m_df1...m_df5 - *data frames of numeric data for correlation plots*
##### M1...M5 - *correlation plots, split for readability*
##### train.dummies - *data frame of training data that includes dummy variables for the categorical data*
##### val.dummies - *data frame of validation data that includes dummy variables for the categorical data*
##### train_n - *normalized training data*
##### val_n - *normalized validation data*
##### k - *number of nearest neighbors to use for the KNN model*
##### predKNN - *predictions from the KNN model*
##### dfPred - *predictions in data frame*
##### logreg - *logistic regression response terms*
##### logreg.prob - *logistic regression probability vector*
##### test.logreg - *data frame for the logistic regression validation data*

#### FUNCTIONS
##### normalize - function to normalize numerical data for the KNN model

