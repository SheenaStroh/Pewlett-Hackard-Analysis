# Pewlett Hackard Retirement Analysis

## Overview
At Pewlett Hackard there are a large number of employees that are reaching retirement age within the 
next few years. The purpose of this report is to determine the number of retiring employees who have 
specific titles, as well as to find the employees who would be eligible to participate in a mentorship 
program.

## Results
The analysis produced the following results:
- A list of retirement eligible employees, including their name and any title 
  they had held during their time at PH. This list was filtered from the main employee table using the 
  following query:
  
  ![Retiring_emp_query](https://user-images.githubusercontent.com/85318060/128639860-78079318-3954-49b1-8936-f8ceb6540197.png)
  
  This query used date of birth from 1952-1955, assuming those employees would be the ones ready for retirement in the coming years.
  
- Then using the following query this list was filtered down to only 
  include the most recent title for each staff member:
  
  ![Distinct_query](https://user-images.githubusercontent.com/85318060/128639582-2221a752-1c3a-4f92-982a-35daad4de6ef.png)
  
  This list showed a total of 90,398 employees.
  
- Using this list and the GROUP BY function, a list of the total number of employees in each title 
  was created.

  ![Title_count](https://user-images.githubusercontent.com/85318060/128639701-e17c9fbe-df57-4ed1-b86a-98b7b1b51cd8.png)
  
- Finally, it was decided that employees born in 1965 would be eligible for a mentorship program to 
  prepare for the wave of retiring staff that was coming. The following query was used to determine 
  how many eligible current employees were at PH:

  ![Mentorship_query](https://user-images.githubusercontent.com/85318060/128640043-759a87e3-6423-4a75-b840-89cc93645cc0.png)

  A total of 1,549 employees were determined to be mentorship eligible.
  
## Summary
Overall there are a large number of roles that will need to be filled as the upcoming retirement wave begins to impact the company. The initial list showed a total of 90,398 employees, though that list seems to include retirement aged employees who may no longer be employed with PH. The following is an additional query that could be run on that retirement list to get a list that only contains current employees who will be ready for retirement:

![Current-retiring](https://user-images.githubusercontent.com/85318060/128640328-36613cb4-cbc7-49d3-959b-74075ae4c1da.png)

This cuts the toles that will need to be filled down to 72,458.

By filtering down to only the currently employed staff, we can see that there are more than enough retiring staff to mentor the 1,549 employees who would be mentorship eligible based on the inital given criteria. Given that there are so many more positions that will need to be filled, it would make sense to extend the criteria for mentorship eligibility to include employees who were born in 1963-1965. Counting the extended eligibility we get the following table:

![Extended_eligibility_count](https://user-images.githubusercontent.com/85318060/128640725-1278a4a6-608e-4321-9d81-3c766b25357e.png)

Which gives us more people who could be in the mentorship program, which in turn will give the company a better head-start on the influx of retiring employees in the following years.
