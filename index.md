#  Project for Stata II (Intermediate)

## SURVIVAL ANALYSIS: (Does self-reported health status predict mortality? )

### *By- Asma Rayani (Created on May 17, 2024)*


### 1. Purpose of the Project:
  We are conducting this project so that we can keep working for the next 3 weeks on survival analysis to evaluate if the self-reported health status
  can help predict mortality.
 Other collaborators are welcome to contribute by adding their inputs to `read.me` file in 
 [my PROJECT_MAIN repository](https://github.com/Asmaray5/Project_main)
  and putting a comment while committing changes.
### 2. Description of Data Source:
  We will use the different datasets from [National Health and Nutrition Examination Survey](https://www.cdc.gov/nchs/nhanes/index.htm) for this project.
  - This is the [NHANES SURVEY DATASET](https://wwwn.cdc.gov/Nchs/Nhanes/1999-2000/DEMO.XPT)
  - This is the link to [NHANES MORTALITY DATASET](https://ftp.cdc.gov/pub/HEALTH_STATISTICS/NCHS/datalinkage/linked_mortality/)
    - Use `NHANES_1999_2000_MORT_2019_PUBLIC.dat`'
   
### 3. Downloaded a do-file, edited and uploaded in my repository:** 
   - First, [a do-file from NHANES website](https://ftp.cdc.gov/pub/HEALTH_STATISTICS/NCHS/datalinkage/linked_mortality/Stata_ReadInProgramAllSurveys.do) was downloaded and 
    edited for the directory path,  and renamed as `followup.do` and posted in my repository so that it can be run directly from the remote repository. 
    You can see what changes were made through clicking `history` in the 
    right corner of [followup.do](followup.do) file.
        

**3.1. Then, merged the `followup.dta` with another dataset:**
   - We imported the NHANES mortality dataset.
   - We merged this dataset to the `followup.dta` in our directory, using the id variable `seqn`.
   - The imported dataset has 9965 observations and 152 variables

        Click [here](week7.dta) to see the merged dataset.
     
### 4. Preparing for the next weeks
   - Get familiar with the datasets and variables
       - We can look at the [data documentation and codebook](https://wwwn.cdc.gov/Nchs/Nhanes/1999-2000/HUQ.htm) for more information on variables
   - We specially need these variables:
     - Id variable: `seqn`
     - Exit Variable: `permth_int` This is person-month, change it into person-years
     - Outcome Variable: `mortstat` This is the Final Mortality Status-only keep those who are eligible
     - Main Independent Variale: `uq010` This is the self-reported health status
     - Other independent Variables: Need to explore more
   - We will do different anaysis
        - Do survival analysis and make cumulative mortality curves by the main independent variable
        - Do both unadjusted and adjusted cox regressions 
   - We will include results and graphs from the analysis here
### 5. Week 7 (Updated on Saturday May 17, 2024): Lets do some analysis
   - We will do non-parametric (Kaplan Meier) and  semi-parametric (Cox Regression) analysis to get the effect estimates
   - We will also look at the mortality risk for specific scenario (a 40 year old man who self-reported good health)
   - You can see the [Detailed Stata codes and Analysis directly from Stata](dyndoc.html)
