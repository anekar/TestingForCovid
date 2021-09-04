
[![GitHub issues](https://img.shields.io/github/issues/anekar/TestingForCovid)](https://github.com/anekar/TestingForCovid/issues)
![Lines of code](https://img.shields.io/tokei/lines/github/anekar/TestingForCovid)
![GitHub watchers](https://img.shields.io/github/watchers/anekar/TestingForCovid?style=social)
![GitHub last commit](https://img.shields.io/github/last-commit/anekar/TestingForCovid)

# Project Information
The downloadable data files contain information about hospitalisation and
Intensive Care Unit (ICU) admission rates and current occupancy for COVID-19 by date and country. Each row contains the corresponding data for a certain date (day or week) and per country.

# Installation
Install the libraries  from CRAN as follows
```R
install.packages('tidyverse')
install.packages('readxl')
install.packages('ggplot2')
install.packages('readr')
```
OR with ```devtools package``` as follows from github
```R
devtools::install_github("tidyverse/tidyverse")
```
# Data Providers
* Downloadable data from 
```R
European Centre for Disease Prevention and Control
```
# Project Phases
<details>
<summary>Project Phases</summary>

1.  Data Collection
    * Data have been downloaded from European Centre for Disease Prevention and Control
    
2.  Data Cleaning  
    * This process includes all the necessary edits in order to make the data tidy and in format that can be worked in order to produce insights, such as
    ```R
    i) Coverting dates 
    ii) Changing format of some variables
    iii) Deleting columns
    iv) Detecting outliers and NA values 
    ```
3. Exploratory Data Analysis
    * In this stage of the project we produce insights and key visualization that will help ups understand the data and spot trends among them.
   For this reason we rely on
    ```
   barplots
   histograms 
   boxplots
   ``` 
   

</details> 

# Code Samples
* Importing the dataset
```R
df <- read_excel("TestingForCovid.xlsx")
```
* Changing format in some variables 
```R
df$year <- as.numeric(df$year)
df$new_cases <- as.numeric(df$new_cases)
```
* Extracting the final dataset into excel
```R
write.xlsx(df, file = 'TestCovid.xlsx')
```
# Project Goal
The goal of this project aims to analyze certain information about hospitalization, ICU(Intensive Care Units)
and current occupancy of COVID-19.
 
# Visuals
<details>
<summary>Raw Data</summary>
 
 ![df before cleaning](https://user-images.githubusercontent.com/47696240/97710170-10a39400-1ac4-11eb-88df-24f324d5b38b.png)
</details>

<details>
<summary>Dataframe after cleaning</summary>

![df after cleaning](https://user-images.githubusercontent.com/47696240/98140765-7f229080-1ece-11eb-8f9e-9a9847fe2bf3.png)

</details>


# Problems Faced
* Analzying this dataset i came across with varius problems such as:
 ```R 
   1. The column names must be replaced
   2. Columns with no use on dataset must be excluded from the dataframe
   3. The year_week variable is not following the 3rd normality form 
   4. The week variable must be inserted in a new column
   5. Scientific notation 
 ```
# Visualizations
```Tableau Public```,

```Microsoft Excel```

## Languages
```R Programming language```

## Integrated Development Environment
```RStudio```
