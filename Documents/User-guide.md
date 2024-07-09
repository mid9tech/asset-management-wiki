1	Overview
1.1	Goal
Allows Admin to manage company’s asset
Allows user to request to return an assignment
1.2	Brief Description
The asset management application is designed to help organizations manage their assets efficiently. It comprises a front-end built with Next.js, a back-end powered by NestJS, and utilizes various services such as Docker, Azure Container Registry, and Prisma for database management. The entire system is deployed and maintained using Azure services to ensure scalability, security, and reliability.
2	


| Actors | Description	  | Scope |
|-|--|--|
| Admin	 | Full control: Manage/Create/Edit/Disable user Manage/Create/Edit/Delete asset
●	Manage/Create/Edit/Delete assignment
●	Manage/Create Request for Returning
●	View/Export asset report |  |
|  |  |  |



Full control: 
●	Manage/Create/Edit/Disable user
●	Manage/Create/Edit/Delete asset
●	Manage/Create/Edit/Delete assignment
●	Manage/Create Request for Returning
●	View/Export asset report	All employees
Staff	Can Accept/Decline assignments
Can Request for Returning asset	Individual
3	Preconditions
The actor must be signed in to the system
4	Flow of Events
4.1	Manage User
Basic Flow – Log in/Log out
Step	Event Description
1	Users could either:
Input valid username and password provided
2	If this is the first time user log in : 
-	Change password popup displays, User input new password 
-	System directs to Log in window for user to re-log in with new password
If this is not first time user log in : 
-	System directs to Homepage 
3	User click on username on topright of page, select Log out option to logout
4	The flow ends
Alternative Flow – Change password
Step	Event Description
1.	Users click Change password button
2.	Change password popup displays
User is required to input Old password and New password
3. 	System directs to Log in window for user to re-log in with new password
4	The flow ends
Alternative Flow – Create new user
Step	Event Description
1.		User go to Manage user page, click on Create new asset
2.	User input fields: First name, Last name, DOB, Gender, Joined date, Type
Click on Save button
3.	New user is created successfully
Created user is appeared at top of User list
The flow ends

Alternative Flow – Edit user
Step	Event Description
1.	At Manage user list, Click on Edit button of any user
2.	First name, Last Name field is disable
DOB, Gender, Joined date, Type is enable to Edit
3.	Users input valid data and click Save
4.	Flow ends
4.1.1	Alternative Flow – Delete User
Step	Event Description
1.	At Manage user list, Click on Disable button of any user
2.	If user has avaiable assigment, warning message is shown -> Disable user unsuccessfully
If user does not have any assignment, Confirmation popup -> Click Yes button -> Disable user successfully
3.	Flow ends.
Alternative Flow – View user list
Step	Event Description
1.	At Manage user page, Admin can view all of users which is the same as Admin’s location
2.	Users can either:
Sorting by Staffcode, Fullname, Joined date, Type
OR
Filter by User type: Admin, Staff
3.	Users can:
Click on any User record
Detailed user information popup with all informations
4.	Flow ends
4.2	Manage Asset
Alternative Flow – Create new Asset
Step	Event Description
1.	At Manage Asset page, click on Create new asset button
2.	Users input fields: Name, Category, Specification, Installed date, State
Users can either: Create new category
Click Save
3.	New asset is created successfully
Created asset is appeared at top of Asset list
The flow ends
Alternative Flow - Edit Asset
Step	Event Description
1.	At Manage asset list, Click on Edit button of any asset
2.	Category field is disable
Asset name, Specification, Installed Date, State is enable to Edit
3.	Users input valid data and click Save
4.	Flow ends


Alternative Flow – Detele Asset
Step	Event Description
1.	At Manage asset list, Click on Disable button of any asset
2.	If asset is assigned to any user -> warning message is shown -> Disable user unsuccessfully
If asset has historical assignemtn -> warning message is shown -> Disable user unsuccessfully
OR ELSE
Confirmation message displays -> Click yes -> Disable asset successfully
3.	Flow ends.
Alternative Flow – View Asset list
Step	Event Description
1.	At Manage asset page, Admin can view all of assets in system
2.	Users can either:
Sorting by Asset code, Asset name, Category, State
OR
Filter by State, Category
3.	Users can:
Click on any Asset record
Detailed asset information popup with all informations
4.	Flow ends

4.3	Manage Assignment
Alternative Flow – Create new Assignment
Step	Event Description
1.	At Manage assignment page, click on Create new assignment button
2.	Users input fields: User, Asset, Assigned date, Note
Users can either: 
Search for User in User field
OR
Search for Asset in Asset field
Click Save
3.	New assignment is created successfully
Created assignment is appeared at top of Assignment list
The flow ends
Alternative Flow - Edit Assignment
Step	Event Description
1.	At Manage Assignment list, click on Edit button of any assignment
2.	User, Asset, Assigned date, Note is enabled to Edit
3.	Users input valid data and click Save
4.	Flow ends


Alternative Flow – Delete Assignment
Step	Event Description
1.	At Manage assignment list, Click on Disable button of any assignment
2.	If assignment has Assigned state -> Delete button is disable 
OR ELSE
Confirmation message displays -> Click yes -> Delete assignment successfully
3.	Flow ends.
Alternative Flow – View Assignment list
Step	Event Description
1.	At Manage assignment page, Admin can view all of assignment in system which is the same as Admin’s location
2.	Users can either:
Sorting by No., Asset code, Asset name, Assigned to, Assigned By, State
OR
Filter by State, Assigned Date
3.	Users can:
Click on any Assignment record
Detailed assignment information popup with all informations
4.	Flow ends

4.4	Manage Request for Returning
Alternative Flow – Create Request for Returning
Step	Event Description
1.	At Home page, 
Click on Return button of individual’s assignment which has Accepted state
If assignment has different state, Go to Step 3
Confirmation popup
2.	Click Yes button
3.	Return request is created successfully
The flow ends
Alternative Flow – View Request for Returning list
Step	Event Description
1.	At Request for Returning page, Admin can view all of requests in which is the same as Admin’s location 
2.	Users can either:
Sorting by No., Asset code, Asset name, Assigned to, Assigned By, State
OR
Filter by State, Assigned Date
3.	Users can:
Click on any Assignment record
Detailed assignment information popup with all informations
4.	Flow ends



