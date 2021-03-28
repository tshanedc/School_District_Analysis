# School_District_Analysis

## Overview
This assignment for this project is to compare several schools within the school district. Standardized tests scores for reading and maths were provided. Throughout this exercise, we grouped the schools by test score, passing percentages, budgets per capita, and even whether or not a school was a District School or a Charter School.

Additionally, there is a case of academic dishonesty present in Thomas High School that affects the 9th grade test scores. Rendering the dataset flawed due to such limited dishonesty is not an open for the school district. I was tasked with identifying and replacing the inaccurate 9th Grade test scores from Thomas High School and conducting analysis on the "clean data". By removing the inaccurate data, true insights were extracted that affect each school's overall standing among others, and also provided Thomas High School principles and teachers with honest, accurate data on the test scores for students in tenth, eleventh, and twelfth grades.

## Results
To remove the inaccurate data from Thomas High School's 9th graders, we imported Numpy and then used the loc method to replace first the math scores, and then the reading scores, of Thomas High School Ninth graders. The faulty data was replaced with NaN to signify that they were not a number. Changing this to 0 in this case would have severly altered the data. This method made the scores "invisible" to a degree.
```
student_data_df.loc[(student_data_df["school_name"] == "Thomas High School") & (student_data_df["grade"] == "9th"), "reading_score"] = np.nan
```

### Effect on District Summary

The effect on the District Summary was limited. Average Math Scores were roughly the same as was reading score. Our understanding of the exact changes is limited due to our formatting efforts to round the scores. The percentage of students passing was more affected, with a slightly smaller percentage of students passing each subject and overall. Previously, 74.98% of students passed math, 85.81% of students passed reading, and 65.17% passed both overall. After removing the inaccurate data, the new scores are 74.8%, 85.7%, and 64.9%, respectively.

![new_districtsummary.png](new_districtsummary.png)

### Effects on School Summary


#### How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?


### How does replacing the ninth-grade scores affect the following:
#### Math and reading scores by grade

#### Scores by school spending

#### Scores by school size
#### Scores by school type

## Summary - Four Major Changes

