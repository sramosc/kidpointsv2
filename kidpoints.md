# KIDPOINTS

## Functional Requirements

### WELCOME Page:
From this screen, a new user should sign up in the application, and a existing user should login.
#### Form:
* E-mail (text field) _required in SIGN UP_
* Password (password field) _required in SIGN UP_
* SIGN IN (button):  Redirects to main page if Ok. It will validate the user/pass against DB and will redirect to main page in case of success. Anyway, it will show a error message.
* SIGN UP (button): Redirects to **SIGN IN** page.
* FORGET YOUR PASSWORD (link): Redirects to **FORGET YOUR PASSWORD?** page.
#### Validations
##### SIGN IN
* Blank field/s.
* E-mail is not valid or doesn't exists in DB.
* Password is incorrect.
    
### FORGET YOUR PASSWORD Page:
#### Form
* E-mail (text) _required_
* SUBMIT BUTTON: It will send an automatic e-mail to the user's e-mail with the stored password
* RESET BUTTON: It'll erase data from the form.
* GO BACK BUTTON: Redirects to **WELCOME** Page.

#### FYP validations:
* E-mail is blank, is not valid or doesn't exists in DB.
    
### SIGN UP Page: 
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
