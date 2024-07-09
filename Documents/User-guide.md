# 1 Overview

## 1.1 Goal
- Allows Admin to manage company’s assets
- Allows users to request to return an assignment

## 1.2 Brief Description
The asset management application is designed to help organizations manage their assets efficiently. It comprises a front-end built with Next.js, a back-end powered by NestJS, and utilizes various services such as Docker, Azure Container Registry, and Prisma for database management. The entire system is deployed and maintained using Azure services to ensure scalability, security, and reliability.

# 2 Actors and Scope

| Actors | Description |
|--------|-------------|
| Admin  | Full control: Manage/Create/Edit/Disable user, Manage/Create/Edit/Delete asset, Manage/Create/Edit/Delete assignment, Manage/Create Request for Returning, View/Export asset report |
| Staff  | Can Accept/Decline assignments, Can Request for Returning asset |

# 3 Preconditions
The actor must be signed in to the system.

# 4 Flow of Events

## 4.1 Manage User

### Basic Flow – Log in/Log out
1. Users input valid username and password.
2. If this is the first login:
   - Change password popup displays.
   - User inputs new password.
   - System directs to log in window for user to re-log in with the new password.
3. If this is not the first login:
   - System directs to Homepage.
4. User clicks on username at the top right of the page, selects Log out option to logout.
5. The flow ends.

### Alternative Flow – Change password
1. User clicks Change password button.
2. Change password popup displays.
3. User inputs Old password and New password.
4. System directs to log in window for user to re-log in with the new password.
5. The flow ends.

### Alternative Flow – Create new user
1. User goes to Manage user page, clicks on Create new asset.
2. User inputs fields: First name, Last name, DOB, Gender, Joined date, Type.
3. Clicks on Save button.
4. New user is created successfully.
5. Created user appears at top of User list.
6. The flow ends.

### Alternative Flow – Edit user
1. At Manage user list, click on Edit button of any user.
2. First name, Last Name fields are disabled.
3. DOB, Gender, Joined date, Type are enabled to edit.
4. User inputs valid data and clicks Save.
5. Flow ends.

### Alternative Flow – Delete User
1. At Manage user list, click on Disable button of any user.
2. If user has available assignment, warning message is shown -> Disable user unsuccessfully.
3. If user does not have any assignment, Confirmation popup -> Click Yes button -> Disable user successfully.
4. Flow ends.

### Alternative Flow – View user list
1. At Manage user page, Admin can view all users which are the same as Admin’s location.
2. Users can either:
   - Sort by Staffcode, Fullname, Joined date, Type
   - OR
   - Filter by User type: Admin, Staff
3. Users can click on any User record.
4. Detailed user information popup with all information.
5. Flow ends.

## 4.2 Manage Asset

### Alternative Flow – Create new Asset
1. At Manage Asset page, click on Create new asset button.
2. Users input fields: Name, Category, Specification, Installed date, State.
3. Users can either create a new category.
4. Click Save.
5. New asset is created successfully.
6. Created asset appears at the top of Asset list.
7. The flow ends.

### Alternative Flow - Edit Asset
1. At Manage asset list, click on Edit button of any asset.
2. Category field is disabled.
3. Asset name, Specification, Installed Date, State are enabled to edit.
4. Users input valid data and click Save.
5. Flow ends.

### Alternative Flow – Delete Asset
1. At Manage asset list, click on Disable button of any asset.
2. If asset is assigned to any user -> warning message is shown -> Disable asset unsuccessfully.
3. If asset has historical assignment -> warning message is shown -> Disable asset unsuccessfully.
4. OR ELSE
5. Confirmation message displays -> Click yes -> Disable asset successfully.
6. Flow ends.

### Alternative Flow – View Asset list
1. At Manage asset page, Admin can view all assets in the system.
2. Users can either:
   - Sort by Asset code, Asset name, Category, State
   - OR
   - Filter by State, Category
3. Users can click on any Asset record.
4. Detailed asset information popup with all information.
5. Flow ends.

## 4.3 Manage Assignment

### Alternative Flow – Create new Assignment
1. At Manage assignment page, click on Create new assignment button.
2. Users input fields: User, Asset, Assigned date, Note.
3. Users can either search for User in User field or search for Asset in Asset field.
4. Click Save.
5. New assignment is created successfully.
6. Created assignment appears at the top of Assignment list.
7. The flow ends.

### Alternative Flow - Edit Assignment
1. At Manage Assignment list, click on Edit button of any assignment.
2. User, Asset, Assigned date, Note are enabled to edit.
3. Users input valid data and click Save.
4. Flow ends.

### Alternative Flow – Delete Assignment
1. At Manage assignment list, click on Disable button of any assignment.
2. If assignment has Assigned state -> Delete button is disabled.
3. OR ELSE
4. Confirmation message displays -> Click yes -> Delete assignment successfully.
5. Flow ends.

### Alternative Flow – View Assignment list
1. At Manage assignment page, Admin can view all assignments in the system which are the same as Admin’s location.
2. Users can either:
   - Sort by No., Asset code, Asset name, Assigned to, Assigned By, State
   - OR
   - Filter by State, Assigned Date
3. Users can click on any Assignment record.
4. Detailed assignment information popup with all information.
5. Flow ends.

## 4.4 Manage Request for Returning

### Alternative Flow – Create Request for Returning
1. At Home page, click on Return button of individual’s assignment which has Accepted state.
2. If assignment has a different state, go to Step 3.
3. Confirmation popup.
4. Click Yes button.
5. Return request is created successfully.
6. The flow ends.

### Alternative Flow – View Request for Returning list
1. At Request for Returning page, Admin can view all requests which are the same as Admin’s location.
2. Users can either:
   - Sort by No., Asset code, Asset name, Assigned to, Assigned By, State
   - OR
   - Filter by State, Assigned Date
3. Users can click on any Request record.
4. Detailed assignment information popup with all information.
5. Flow ends.
