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
