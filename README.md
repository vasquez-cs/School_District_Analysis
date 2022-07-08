# School District Analysis
## Overview of the school district analysis:
The school board has notified Maria and her supervisor that the students_complete.csv file shows evidence of academic dishonesty. Thomas High School ninth grade reading and math grades appear to be tampered with. School board want to uphold state-testing standards and have turned to Maria for help. She has asked me to replace the math and reading scores for Thomas High School with NaNs. Once I replaced the math and reading scores, I repeated the school district analysis and recorded my findings.

### Results:

Following the analysis, I have listed the seven metircs as pairs in the figures below (as "Figure #A" and "Figure #B"). Each of these were run before and after the updates that were made by making the Thomas High School ninth grade reading and math grades NaNs.

### Summary

<img src="https://user-images.githubusercontent.com/107224632/177878408-320065c8-e1c7-45e3-952d-6c0d3239feff.png" width=80% height=80%><br />
*Figure 1A: Original district_summary_df Output*<br />

<img src="https://user-images.githubusercontent.com/107224632/177878138-2d8298f0-5740-4c57-9fb6-adb994ea76f5.png" width=80% height=80%><br />
*Figure 1B: district_summary_df Output after using NaNs for Thomas High School 9th grade math and reading scores*<br />

* In the district_summary_df we can see there was a slight in the post NaNs fix
  * this is due to not formatting correctly, but if we round the % passing math, reading and overall passing to whole numbers, there wouldn't be a difference as those three values in the post fix would round to the whole number and match the original district_summary_df output

<img src="https://user-images.githubusercontent.com/107224632/177879160-21db6f62-f84c-4527-9a9a-ec60a09c9a7d.png" width=80% height=80%><br />
*Figure 2A: Original per_school_summary_df Output*<br />

<img src="https://user-images.githubusercontent.com/107224632/177884983-b7b66ae9-ec72-48a3-9872-445580303b2d.png" width=80% height=80%><br />
*Figure 2B: per_school_summary_df Output after using NaNs for Thomas High School 9th grade math and reading scores*<br />

* In the per_school_summary_df we can see there was a huge jump in the post NaNs fix for Thomas High School
  * All other school values were the same.   
  * This is due to the NaNs fix only affecting the Thomas High School averages
    * Averages were drastically changed as the entire 9th grade reading and math scores were tossed and total number of students used to determine the percentage was reduced by the number of students in the 9th grade, therefore improving the overall percentages for % passing math, reading and overall passing. 

<img src="https://user-images.githubusercontent.com/107224632/177879160-21db6f62-f84c-4527-9a9a-ec60a09c9a7d.png" width=80% height=80%><br />
*Figure 3A: Original top_schools Output*<br />

<img src="https://user-images.githubusercontent.com/107224632/177885752-c99ecc2c-3596-4815-be10-1499af43eac1.png" width=80% height=80%><br />
*Figure 3B: top_5_schools (Renamed) Output after using NaNs for Thomas High School 9th grade math and reading scores*<br />

* In the top_5_schools we can see there was a huge jump in top school position following the post NaNs fix for Thomas High School
  * All other school values were the same.   
  * School went from the 13th position to the 2nd position following the post NaNs fix
    * Position was drastically improved as the entire 9th grade reading and math scores were tossed and total number of students used to determine the percentage was reduced by the number of students in the 9th grade, therefore improving the overall percentages for % passing math, reading and overall passing. 

<img src="https://user-images.githubusercontent.com/107224632/177886490-9497c83f-d5b9-4c23-b98e-0d7865869a0c.png" width=80% height=80%><br />
*Figure 4A: Original bottom_schools Output*<br />

<img src="https://user-images.githubusercontent.com/107224632/177886397-b643d7ae-fa8c-44cb-9414-f0e47d3ca057.png" width=80% height=80%><br />
*Figure 4B: bottom_5_schools (Renamed) Output after using NaNs for Thomas High School 9th grade math and reading scores*<br />

* I would expect that the original bottom_schools image would have Thomas High School as 2nd from the top based on top_schools
  * Appears to be a coding issue as the ouput now has Thomas High School at the bottom

<img src="https://user-images.githubusercontent.com/107224632/177887424-50194b08-6d44-43b8-93b1-a1f988523134.png" width=80% height=80%><br />
*Figure 5A: Original spending_summary_df Output*<br />

<img src="https://user-images.githubusercontent.com/107224632/177887392-5d1a905f-dce9-4a98-b768-b2f259db4811.png" width=80% height=80%><br />
*Figure 5B: spending_summary_df Output after using NaNs for Thomas High School 9th grade math and reading scores*<br />

* I would expect that there would be a change in the averages from the original spending_summary_df Output, but the outputs match
  * Appears to be a coding issue, but the ouput is matching for both outputs before and after the NaN fix.

<img src="https://user-images.githubusercontent.com/107224632/177887697-140bc22b-9a4b-470b-b2ff-169c48e869d8.png" width=80% height=80%><br />
*Figure 6A: Original size_summary_df Output*<br />

<img src="https://user-images.githubusercontent.com/107224632/177887761-241e9f46-9041-4bd4-8491-f4f2c3453072.png" width=80% height=80%><br />
*Figure 6B: size_summary_df Output after using NaNs for Thomas High School 9th grade math and reading scores*<br />

* I would expect that there would be a change in the averages from the original size_summary_df output, but the outputs match
  * Appears to be a coding issue, but the ouput is matching for both outputs before and after the NaN fix.

<img src="https://user-images.githubusercontent.com/107224632/177887882-40d1ca68-5883-4570-8caf-9bea3c09c96b.png" width=80% height=80%><br />
*Figure 7A: Original type_summary_df Output*<br />

<img src="https://user-images.githubusercontent.com/107224632/177887793-4feb7967-3ac2-4213-843e-72bbf239829e.png" width=80% height=80%><br />
*Figure 7B: spending_summary_df Output after using NaNs for Thomas High School 9th grade math and reading scores*<br />

* I would expect that there would be a change in the averages from the original spending_summary_df output, but the outputs match
  * Appears to be a coding issue, but the ouput is matching for both outputs before and after the NaN fix.

The outputs that changed the most were per_school_summary_df and top_5_schools as the changes in averages are very clear. The remaining outputs appear to reflect the new averages for both the prior and post outputs which may just be a coding error.
