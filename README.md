# School District Analysis
The purpose of the School District Analysis (SDA) is to provide the school board with a district-wide analysis of each school's reading and math scores. A secondary analysis was conducted to account for a an unprecedented case of academic dishonesty at one of the schools under study. To adjust for inaccurate data, the scores recorded for the ninth grade class at Thomas High School were replaced with NaNs.

## Results
When the school board notified the firm about the situation, the issue of data integrity became the forefront of our discussions. The following questions and resolutions provide a detailed summary of the major themes that were discussed.

#### How is the district summary affected?
The following screenshots depict the district summary analysis results for both the corrupted and "new" data sets.

###### Figure 1.1 Corrupt District Summary
![PyCitySchools_NaN_District_Summary](https://github.com/kylegross/School_District_Analysis/blob/master/PyCitySchools_NaN_District_Summary.PNG)

###### Figure 1.2 New District Summary
![PyCitySchools_orig_District_Summary](https://github.com/kylegross/School_District_Analysis/blob/master/PyCitySchools_orig_District_Summary.PNG)

As seen above, this particular report was not greatly impacted by the corrupt data. The Average Math Score, % Passing Math, % Passing Reading, and the % Overall Passing values are merely 0.1 to 1 data point greater in the corrupt summary versus the new summary. This is not a major variance in the data.

#### How is the school summary affected?
The school summary is affected because in the new analysis, by setting the ninth-grade reading and math scores to NaN at Thomas High School, the school's average math and reading scores are both below the 70% passing grade, and so it does not appear in the school summary chart. No other schools are affected.

#### How does replacing the ninth graders' math and reading scores affect Thomas High School's performance relative to other schools?
Like the district summary, replacing the reading and math scores of ninth graders at Thomas High School brought their average scores up very minisculy, in both cases only a tenth of a percentage point. In comparison to other schools, Thomas High School's scores are in parellel to the other schools' averages.

#### How does replacing the ninth-grade scores affect the following:
###### Math and reading scores by grade
By grade, the only math and reading scores affected are those belonging to ninth-grade students at Thomas High School, which both changed from an average of 83% to NaNs.
    
###### Scores by school spending
In the corrupt summary, Thomas High School fell into the $630-644 spending range bucket. In the new summary, the school falls into the same spending bucket. The coincinding scores by school spending changed in % Passing Math and % Passing Reading, which decreased from 73% and 84% to 67% and 77%, respectively. The % Overall Passing also decreased from 63% to 56%.
    
   ###### Figure 2.1 Corrupt School Spending
   ![PyCitySchools_NaN_Spending](https://github.com/kylegross/School_District_Analysis/blob/master/PyCitySchools_NaN_Spending.PNG)

   ###### Figure 2.2 New School Spending
   ![PyCitySchools_orig_Spending](https://github.com/kylegross/School_District_Analysis/blob/master/PyCitySchools_orig_Spending.PNG)
    
    
###### Scores by school size
Thomas High School falls under the Medium-size category, which includes enrollments of 1,000-2,000 students. Comparatively, the values changed in % Passing Math and % Passing Reading, which decreased from 94% and 97% to 88% and 91%, respectively. The % Overall Passing also decreased from 91% to 85%. 
    
   ###### Figure 3.1 Corrupt School Size
   ![PyCitySchools_NaN_Size](https://github.com/kylegross/School_District_Analysis/blob/master//PyCitySchools_NaN_Size.PNG)

   ###### Figure 3.2 New School Size
   ![PyCitySchools_orig_Size](https://github.com/kylegross/School_District_Analysis/blob/master//PyCitySchools_orig_Size.PNG)
    
    
###### Scores by school type
Thomas High School is a Charter School, so the Charter values are the only ones that changed. The overall average scores did not change, but the values did change in % Passing Math and % Passing Reading, which decreased from 94% and 97% to 90% and 93%, respectively. The % Overall Passing also decreased from 90% to 87%. 

## Summary
There are four major changes in the new data analysis. First of all, the data results by grade for Thomas High School are no longer accounted for in the ninth-grade calculations, as the values have all been set to NaNs. Secondly, the scores by spending per student decreased in value for the $630-644 spending range bucket. Thirdly, the scores by school size decreased in the medium-sized category. Finally, the scores by school type decreased in the Charter school type.
