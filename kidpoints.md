# KIDPOINTS

## Functional Requirements

This is a secured web application. An user has to login in order to get full access to the features.
The first three pages (welcome, sign up and forget your password) are the only ones visible without authentication.

### WELCOME Page:
_UNAUTHENTICATED_
From this screen, a new user should sign up in the application, and a existing user should login.
#### FORM:
* E-mail (text field) _required in SIGN UP_
* Password (password field) _required in SIGN UP_
* SIGN IN (button)
* SIGN UP (button): 
* FORGET YOUR PASSWORD (link)

#### ACTIONS

##### SIGN IN
It will validate the user/pass against DB and will redirect to main page in case of success. Anyway, it will show a error message.
###### Validations
* Blank field/s.
* E-mail is not valid or doesn't exists in DB.
* Password is incorrect.

##### SIGN UP
Redirects to **SIGN UP** page.
###### Validations
none

##### FORGET YOUR PASSWORD
Redirects to **FORGET YOUR PASSWORD?** page.
###### Validations
none

### FORGET YOUR PASSWORD Page:
_UNAUTHENTICATED_
#### FORM
* E-mail (text) _required_
* SUBMIT BUTTON
* RESET BUTTON
* GO BACK BUTTON
#### ACTIONS
##### SUBMIT
It will send an automatic e-mail to the user's e-mail with the stored password. Redirects to **WELCOME** Page.
###### Validations
* E-mail is blank, is not valid or doesn't exists in DB.
##### RESET
It'll erase data from the form.
###### Validations
none
##### GO BACK
Redirects to **WELCOME** Page.
###### Validations
none
    
### SIGN UP Page: 
_UNAUTHENTICATED_
There will be a new screen showing a form to fill with basic personal details:
* Name (text)
* Genre (F/M combo)    
* Email (text)
* ¿Additional data? (not really necessary)
* Password (password)
* Repeat password (password)
* SUBMIT BUTTON: this will create a new temporary user in the DB with the data introduced, and it will send a confirmation email to the user with an activation link. This user's account won't be active until the link in the email is clicked.
* RESET BUTTON: simply erases the data in the form.
* GO BACK BUTTON: redirects to the **WELCOME** page
    
# Entities
* Kid
* Reward
* Calendar
* User

# Kid:
  The kid's entity will maintain the data of a kid. 
  It'll store all the personal data, and the list of users (parents) able to modify/manage it.
  Every kid will have only one calendar, and a list of possible rewards. 
  This list can be shared by two (or more) different kids if the manager users are the same.
* Attributes
  * Name
  * Surname
  * Photo (optional)
  * Calendar: 1 per child.
  * Rewards: 1 list per child (can be shared by two+ kids if the users are the same)
  * Users: list of users authorized to manage the kid's data
  * Audit Data: registry of operations 

# Reward:
  A reward is merely a prize and the cost associated to it. 
  Every user will create his/her own list of rewards. 
* Attributes
  * Name
  * Photo (optional)
  * Cost: in points
  * Audit Data: registered by, datetime, cost's updates.
