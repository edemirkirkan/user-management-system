# user-management-system

# Design and Implementation
## UI Navigation
- The main page displays the data of the user with the columns: ID, username, email, enabled
- There are sort buttons for each column
- There is a new user button to open to form that adds the given user to the database
- After the new user is added (save user button is pressed), the system again navigates to the main page
- There is a hide user button to hide disabled users in the main page

## Product scope
### Target user profile

- Studies in a management deparment of a company
- Frequently uses and edits user data
- Is unfamiliar with databases and SQL 

### Non-Functional Requirements
The system should be reliable and recoverable since the user data is too important to lose.
### Functional Requirements
The system should be concurrent as more than one manager may try to add a user at the same time. Moreover, the system should high performance and scalable as number of user entries may be too much after some point.

## Functionalities
Main page displays the data of the user with the columns: ID, username, email, enabled
### Sort User
The system's api has a function to sort the rows using the specific column.
### Add user
There must be a sql table named user to store the user data. Schema of the user table is as follows: 
- user-id : GUID
- username : VARCHAR(50)
- display-name : VARCHAR(50)  
- phone : VARCHAR(50) 
- email : VARCHAR(50)
- user-role : VARCHAR(10)
- enabled : BOOLEAN

After pressing new user button, the system should navigate from main page to the form to take the user specific data. Hence, also we need to have user specific end-point <br><br>
/users/{user-id} 
### Hide user
The system's api has a function to hide the specific users using the information in enabled column in user table
