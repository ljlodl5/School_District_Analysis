# School_District_Analysis
Data analysis of school district testing

## **Overview of the school district analysis**

Utilizing two sample school district datasets; 1) student count/budget and 2)student reading and math test results, the goal of this assignment is to present the impact of the removal of a subset of potentially dishonest scores reported within the Thomas High School 9th grade cohort.  
By excluding THS 9th graders from the original report, the district will ascertain the level of impact to the district's student-body success in math and reading and determine if refactored decisions are now needed to support student success.
In addition, change to the dataset to exclude 9th graders (aka: NaN) will have an impact to calculations and it is important to ensure the data presented is accurate.   

## **Results**
### **District Summary Impacts** 

The district student body is ~39k students and Thomas High School 9th graders comprises of 461 students. 

On the surface, the 9th grade averages for THS are ~83% for both reading and math respectively which aligns with the 83% average for 10-12th grades at the same school. 
In addition, taking a look at the entire district (including the THS 9th graders) the averages are extremely close (within tenths of a percentage) to when the students are excluded.
In order to impact the district-level average math and reading scores the tests results would have to be considerably overstated off the mean (large amount out of outliers), or could contain more inconspicous changes between the 69 vs.70 threshold thereby understating the % of pass reading and math scores.   

#### ![At a Glance](https://github.com/ljlodl5/School_District_Analysis/blob/main/Resources/Comparison%20NaN%20before%20and%20after%20code%20adjustments.png)


At a district level the end result of removing 9th graders is very slight (assuming the dataset is adjusted appropriately for NaN impacts) 

Exhibit A: Pre-Adjustment

#### ![District Summary pre-NaN](https://github.com/ljlodl5/School_District_Analysis/blob/main/Resources/School%20District%20Summary%20Pre-Adjusted.png)


Exhibit B: Post-Adjustment  

#### ![District Summary post-NaN](https://github.com/ljlodl5/School_District_Analysis/blob/main/Resources/School%20District%20Summary%20Adjusted.png)



### **School Summary Impacts**
The school summary is similar to the district analysis in that there are only neglible changes to the data existed when the appropriate adjustments occured to NaN for the THS 9th graders.

Exhibit A: The data for the school when all THS students were included (pre-NaN). 

#### ![School Summary pre-NaN](https://github.com/ljlodl5/School_District_Analysis/blob/main/Resources/THS%20pre%20NaN.png)


Exhibit B: The data for the school when 9th grade students were removed but totals were adjusted (post-NaN, total student count 10-12th grade = 1174 ).  

#### ![School Summary adjusted NaN](https://github.com/ljlodl5/School_District_Analysis/blob/main/Resources/THS%20post%20adjusted%20replacement.png)


Exhibit C: The data for the school district when student count was not adjusted.(post NaN, total student count = 1635). 
The NaN values reduced math and test scores from the dataset but the full student count erroneously remained, thus the need for coding adjustments and replacement values. 

#### ![School Summary adjusted NaN but with incorrect total student count](https://github.com/ljlodl5/School_District_Analysis/blob/main/Resources/PreAdjusted%20THS.png)


### Elimination of Thomas High School 9th grade scores
Impact of replacing the ninth graders’ math and reading scores and affect on Thomas High School’s performance relative to the other schools: 
		* Math and reading scores by grade
		  There was very little impact other than one less cohort to consider for the school. 
		  The average 9th grade reading and math scores and percentages were already in line with the other grades (displayed above). The scores were averaged among three grades instead of four but this had negligible impact 
			
### ![Math Grades](https://github.com/ljlodl5/School_District_Analysis/blob/main/Resources/Math%209th%20grade%20average.png)

### ![Reading Grades](https://github.com/ljlodl5/School_District_Analysis/blob/main/Resources/Reading%209th%20grade%20average.png)


		*Scores by school spending
		  Spending for THS is $638 per student which is above district average. THS performs well and is a top five school regardless whether 9th graders are included/excluded. 
		   
#### ![Scores By School Spending](https://github.com/ljlodl5/School_District_Analysis/blob/main/Resources/Charter%20School%20Success.png)


		*Scores by school size
		  School size is close is on the low-end of district average with a student body of 1635 students. THS performs well and is a top five school regardless of whether 9th graders are included/excluded.  


#### ![Scores By School Size](https://github.com/ljlodl5/School_District_Analysis/blob/main/Resources/School%20Size%20-Bin%20and%20Scores%20and%20Percentages.png)


		*Scores by school type
		  THS like most Charter schools in the district tend to do exceptionally well (top five schools) while district schools remain in the bottom 5. Removal of 9th grade scores have no bearing on the result 


#### ![Scores By School Type](https://github.com/ljlodl5/School_District_Analysis/blob/main/Resources/District%20vs%20Charter%20School.png)




## **Summary**
### Four Impacts to Data

Summarize four changes in the updated school district analysis after reading and math scores for the ninth grade at Thomas High School have been replaced with NaNs.
   	
	*There were neglible changes to average values (tenths of a percentage point) when the THS 9th grade total student count was removed . See above.  
	  
  	 Note: There were considerable changes to fields dependent on total counts because NaN did not remove the entire row from the dataset. Student count adjustment is a dependency for accurate percentages. 

	*The need to adjust the count of students at THS from 1635 to 1174 (461 students are 9th graders). NaN removed data from inclusion into total test scores/averages, but the student count remained in the dataset thereby deflating overall THS percentages. 

	*Calculation adjustments to percentages that were dependent on adjusted THS count (10th-12th graders)

	* Data replacements (%reading, %math, %overall) were required to the dataframe to include the calculations with adjusted total count (10th-12th graders) 
   	 
### Final Synopsis
The high performance of Thomas High is aligned with other charter schools in the district. Removal of the grade had little impact to overall percentages in the district and at the THS school level between grades. 
The largest impact to the dataset was ensuring that the removal of a grade (via NaN) was carefully assessed within the code to ensure the dataframe(s) was reflective of proper data.  
	

#### Link to PyChallenge 
(https://github.com/ljlodl5/School_District_Analysis/blob/main/PyCitySchools_Challenge.ipynb)

