                                                              #**School_District_Analysis**

###**Overview of Analyis**
  
  ###*Desciption of the Data*
  The analysis of the school district involved two csv files.  One of the complete student data and the other with the school information. 15 high schools with grades 9th through 12th grade were included in the school csv file.  The schools fell into two types, charter or district.  The data also included the size of the school and the total budget.The areas assessed were math scores,reading scores, and the percentage of overall passing.  Passing grades were defined as greater than or equal to 70. The information included for the students can be seen below.
  <img width="1195" alt="Student's Dataframe" src="https://user-images.githubusercontent.com/85581208/142255160-ee7f0d41-3bef-4215-92c7-306c31f0f1bb.png">
  
  ###*The Analysis*
  The original analyis started with looking at what the data contained and then searching for any missing values.  No missing values were located.
<img width="786" alt="Search for missing values" src="https://user-images.githubusercontent.com/85581208/142254345-aaddfbc4-037c-4f51-a1c4-d8f2d366fd5c.png">
Then to get the data into one dataframe. The two were merged together with the code show below.
<img width="1239" alt="Dataframe Merging" src="https://user-images.githubusercontent.com/85581208/142256089-65d12ef8-c087-4ec7-b931-1380d7110d0c.png">
The data was then analyzed by calculating the average math scores and average reading scores for each school.  Using the passing scores of reading and math, the overall passing percentage of each school was also calculated for each grade. 
  The schools were further broken down by their spending per student and size.  Separated into 4 category ranges for their spendng per student, <$584", "$585-629", "$630-644", "$645-675".  Broken down into 3 categories -"Small (<1000)", "Medium (1000-2000)", "Large (2000-5000)".  Then with those categories the average scores of reading and math as well passing grades were assessed as well the overall passing percentage.  
  After all that was completed, it was found the 9th grade students of Thomas High School were found to be cheating.  A reanalysis was then performed by first making their reading and math scores NaN.  The code used for that is shown below.
  <img width="914" alt="Changing values to NaN with loc" src="https://user-images.githubusercontent.com/85581208/142264172-868a21bd-7c30-403b-a1cf-705711e8c1b3.png">
The analysis was redone with those students scores removed.  Let's look at the results.

###*Results*

 The two images below show Thomas High School's numbers.  The first image is with the 9th grade math and reading scores.  The second is when cheating was found and they were removed.
 <img width="987" alt="Thomas High Numbers with 9th graders" src="https://user-images.githubusercontent.com/85581208/142276495-b736484b-7144-4902-986a-9c9e38f95f99.png">

 
 
 <img width="1018" alt="Thomas scores without 9th grade" src="https://user-images.githubusercontent.com/85581208/142276507-74514c80-1d53-4a05-9237-2d277e251deb.png">
-There is a slight decrease in the average math and reading scores of Thomas High School.  The big decrease was in the percent of passing students in math and reading.  This makes sense with all of 9th grade taken out of the passing range with NaNs for math and reading.  The percentages with the whole school count will drop.


The image below shows the results of the analysis before removing the 9th grade Thomas High School scores.
<img width="1198" alt="Scores before students scores taken" src="https://user-images.githubusercontent.com/85581208/142267037-7fb99a77-ec7c-4f36-8e43-7fa884bc118e.png">


 
 
 Here is a visual of the results after the 461 students were removed from the data set.
<img width="1215" alt="Scores after students taken out" src="https://user-images.githubusercontent.com/85581208/142267054-8c32089e-3ddf-435a-9150-091bcbd16cde.png">
  
 
 
 
 Here are the differences observed after the Thomas High School 9th grade students reading and math scores were chanded to NaN:
  -School District Average Math Score - dropped from 79 to 78.9. 
  
  -School District Average Reading Score - no change.  It held at 81.9.
  
  -School District % passing math - dropped two tenths of a percent from 75 to 74.8
  
  -School Ditrict % passing reading - went from 86% to 85.7%. Another drop by 0.3%.
  
  -School District % overall passing - decreased from 65% to 64.9%
  
  -When breaking the schools into the spending per student category, there was no change in any of the numbers. 
  
  -The calculations when broken down by school size did not change when compared after formatting to 0.1.
  
  - When breaking schools into category by type, charter or district, there is no change in the numbers either.

###**In Summary**

  After going through all of the results and looking at the comparisons not too much has changed.  When replacing the Thomas High School 9th grade math and reading school with NaN, the biggest difference was in the school district % passing reading.  It decreased by 0.3%. The next biggest drop was in the school district % passing math.  It dropped by 0.2%.  The two other scores affected, school district average math score and the school district % overall passing, both dropped by 0.1.  For it to be measurable with such a large amount of students, shows the cheating was affecting the overall grades and percentages.  Was it really changing the district's overall picture of how the majority of students were performing.  It does not appear to be.
  
  
  

