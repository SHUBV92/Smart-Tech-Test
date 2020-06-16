This README file acts as an Error Log for the Smart Pensions company and employee database which highlight the UI errors.

This is achieved by breaking the document into three sections:

- Error
- Causation
- Solution

# Error 1

- In the '/companies' route, when clicking on any 'Show' button within the 'Companies List' page, the title section defaults to the first name existing within the company list.

#### Causation:

- In the "companies_controllers.rb", the defined show method has a Company.first "function"??? after retrieving with Company.find "function???" which selects the first id in the companies table.
- The URL shows the id of the company but does not display the respective company name.

#### Solution:

- To fix this issue, remove the Company.first method from the 'show method', so as to retrieve and display the selected company name.

# Error 2

When adding a new employee, it throws the following error: "1 error prohibited this employee from being saved : Surname cannot be blank".

#### Causation:

In the 'new.html.erb' file in the "employees views" folder:

- The label shows "surname", however the textfield attribute shows "middle-name".

#### Solution:

- Add the middlename label with its textfield attribute
- Add the surname label with its texfield attribute

# Error 3

When editing existing employee, the console throws an error: "company id not found".

#### Causation:

- When clicking on a company with: company_id = 9 and employee_id = 14 ???
- Rails Error Handler displays the error: "Couldn’t find Company with 'id'=14"
- The Rails parameter section logs the following parameters: company_id = 14 and employee_id = 9
- The edit method takes the swapped parameters.

#### Solution:

- In the "show.html.erb" file of the companies views folder, add the @companies parameter to the edit link

<hr />

### Documenting my process of debugging the error

- I ran a user experience journey to get familiar with the underlying functionalities of the UI
- Identified the failures of the features not returning the expected behaviour.
- In two of the errors, I found false positives. The last one within the Ruby on Rails console.

### Tools used to debug:

- Rails Console in the shell environment
- Ruby on Rails frontend error console
- Logging the error to the console

### What I could have done better

- Before changing the code
- I should have screenshotted all the features with the pages
- Just so I could compare the difference in each file
