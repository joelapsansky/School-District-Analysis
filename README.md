# School District Analysis
Finished Jupyter Notebook Deliverable: [PyCitySchools Challenge](/PyCitySchools_Challenge.ipynb)

## Overview of School District Analysis
Using Python in Jupyter Notebook, I completed an analysis on school district data in order to help uphold state-testing standards and proper school funding.

## Resources
Here are the csv files containing the datasets:     
[Schools Complete](/Resources/schools_complete.csv)  
[Students Complete](/Resources/students_complete.csv)

## Results
Before performing the analysis, I first had to clean the data by inputting NaN for 9th - graders at Thomas High School.  
![Thomas NaN](/Resources/Thomas_NaN.png "Thomas NaN")  
I later removed the NaNs and put the clean Thomas High School data into a new DataFrame using the following code:  
```
clean_school_data_complete_df = school_data_complete_df[(school_data_complete_df["school_name"] == "Thomas High School")].dropna()
```  
The student count at Thomas dropped from 1635 to 1174.  
  
### Analysis Summary 
* Since Thomas students dropped by 461, total students also dropped by 461 from 39,170 to 38,709.
* The district summary shows a small drop in passing percentages, except for Reading, which barely increased.    
  -Before (unformatted):   
![District Summary Before](/Resources/District_Summary_Before.png "District Summary Before")  
  -After (formatted):    
![District Summary After](/Resources/District_Summary_After.png "District Summary After")  
* All changes in metrics are due to the removal of Thomas 9th graders.   
  -Thomas is still second on the list for high performing schools, but their passing rates are very slightly lower  
  -Thomas average math score dropped by 0.07%  
  -Thomas average reading score increased 0.5%  
  -Thomas % Passing Math decreased 0.09%  
  -Thomas % Passing Reading decreased 0.29%  
  -Thomas % Overall Passing decreased 0.32%  

## School District Summary
After replacing scores for the ninth grade at Thomas High School with NaNs, I conducted an analysis using 461 less students.  This pushed reading scores across the districts a tad higher (0.05%), but resulted in small drops in math percentages and overall percentages.  None of the changes were big enough to change the top five or bottom five performing schools.  Thomas still ranked second overall.  If we drill down into schools by type, District schools are obviously unchanged; Charter schools, however changed slightly.  Percent overall passing went from 90.43% to 90.39%.  Average reading scores actually increased less than 0.01%, but percent passing reading dropped, which tells us that our dataset is somewhat skewed.  The final formatted output rounded to the nearest whole percent shows us no changes whatsoever.
