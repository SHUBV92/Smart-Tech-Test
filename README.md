This READMe file acts as an Error Log for the Smart Pensions company and employee data base. 
This file highlights UI Errors and a an causation 
Thhis is achived by breaking the document into three sections 
-   [Error](# Error 1)
-   Causation
-   Recommendations


# Error 1
-   When clicking on the show button in the company row 
* The name of the company appears to be Alan Autos in the title section in the company page

#### Causations: 
* In the Controller the show method has a Company.first 
* This method displays the first id in the companies table
* It also seems that all the companies show the name of the top company in the list 
* The URL shows the id of the company but does not display it on the actual page 

#### Recommendation:
-    To fix this issue, I just need to remove the Company.first method from the 'showmethod' file.


# Error 2
When adding a new employee 
* It throws the following error - { 1 error prohibited this employee from being saved: Surname cannot be blank}
When editing the following error appears
* Surname can't be blank

#### Causation: 
The editemployee file in the views folder 
* The Label shows a surname - the textfield shows middle-name
* The form is missing a set of middlename & surname %>
File: new.html.erb
File.path: UsersMachine/smart-pension/smart-cs-support-test/app/views/employees/new.html.erb

#### Recomendations:
- Add the middlename label with its textfield 
- Add the surname label with its texfield 


# Error 3
When trying to editing new employee

#### Causation
-   When clicking on a company with the company id = 9 & employee id = 14 
-   Rails Error Handler - Error Couldn’t find Company with “id”=14
-   In the info section of the Rails Error it shows the error below
-   The Railse Error console shows the company id = 14 & employee id = 9 

#### Recommendations

Navigation (Suggestion)
* When on employees tab it only shows go back to employees 


### Documenting my process of Debugging the Error 
* I ran a whole user experience journey to get familiar with the underlying functionalities of the UI 
* Identified the failures of the features behaving in the way they should 
* In two of the errors I found false positives 
* in the third one i found the error Ruby on Rails console


### Tools used to debug: 
* Rails Console in the shell environment
* Ruby on Rails frontend error console 
* Logging the error to the console 

### What I could have done better 
* Before changing the code 
* I should have screenshotted all the features with the pages 
* Just so I could compare the difference in each file 






<!-- Delete this 
Error 2
In the Employees tab for all companies 
*  it shows only 3 Employees Micahel Janet Sarah
* The Employees table only shows the Employees for Gatwick, Curtains for u
Causation


<!-- 

# Contents

[Error 1](# Error 1)
-   Explanation
-   Causation 
-   Recommendations

Error 2
-   Explanation
-   Causation 
-   Recommendations

Error 3
-   Explanation
-   Causation 
-   Recommendations --> 