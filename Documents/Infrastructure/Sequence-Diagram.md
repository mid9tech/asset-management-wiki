# I. Sequence Diagram: User Login Flow

## Overview
This sequence diagram illustrates the user login process within the system. It covers scenarios where a user logs in, is redirected based on their role, or changes their password upon the first login. The interactions between the User, System, LoginPage, HomePage, ChangePwdScreen, and Database components are depicted to showcase the complete workflow.

## Participants
1. **User**: The individual attempting to log in.
2. **System**: The backend system validating credentials and managing user sessions.
3. **LoginPage**: The interface where the user enters their login credentials.
4. **HomePage**: The main page displayed upon successful login.
5. **ChangePwdScreen**: The interface for changing the password during the first login.
6. **Database**: The storage system holding user credentials and roles.

## Flow Description
### Request Login
1. User requests the Login Page.
2. System displays the Login Page.

### Login Attempt
3. User enters their username and password.
4. User clicks the Login Button.
5. System validates the credentials against the Database.

### Successful Login
- **Alt Path**: If credentials are correct:
  - System retrieves user information and checks the role of the User.
  - System redirects the User to the Home Page corresponding to their role.

### Unsuccessful Login
- **Alt Path**: If credentials are incorrect:
  - System returns an error message.
  - System displays the error message on the Login Page.

### First-Time Login
6. System checks if it's the first time the User has logged in.
- **Alt Path**: If it's the first time:
  - System displays the Change Password Screen.
  - User enters a new password.
  - System updates the password in the Database.
  - System displays a success message for the password change.
  - System redirects the User to the Login Page.
- **Alt Path**: If not the first time:
  - System redirects the User to the Home Page.

## Diagram
![SD_AssetManagement_Login.png](/.attachments/SD_AssetManagement_Login-f204cee2-8e89-43bd-b2e4-d5e1b8c2d840.png)

## Notes
- The login process includes validation of credentials and user role-based redirection.
- The system enforces a password change for first-time logins to ensure security.
- Error messages guide the user in case of invalid credentials or other login issues.

# II. Sequence Diagram: Assignment Management Flow

## Overview
This sequence diagram illustrates the process of managing assignments within the system. It covers scenarios where an admin creates, saves, or discards an assignment. The interactions between the Admin, System, ManageAssignmentPage, CreateNewAssignmentPage, UserSearchPopup, AssetSearchPopup, and Database components are depicted to showcase the complete workflow.

## Participants
1. **Admin**: The individual managing assignments.
2. **System**: The backend system handling the logic and state changes for assignments.
3. **ManageAssignmentPage**: The interface displaying existing assignments.
4. **CreateNewAssignmentPage**: The interface for creating a new assignment.
5. **UserSearchPopup**: The UI element for selecting a user for the assignment.
6. **AssetSearchPopup**: The UI element for selecting an asset for the assignment.
7. **Database**: The storage system holding assignment data.

## Flow Description
### Access Manage Assignment Page
1. Admin opens the Manage Assignment Page.
2. System displays the Manage Assignment Page.
3. System fetches assignment data from the Database.
4. System returns assignment data.
5. System displays the assignment data on the Manage Assignment Page.

### Create New Assignment
6. Admin opens the Create Assignment Page.
7. System displays the Create Assignment Page.

### Search User for Assignment
8. Admin opens the Search User Popup.
9. System displays the Search User Popup.
10. Admin selects a user.

### Search Asset for Assignment
11. Admin opens the Search Asset Popup.
12. System displays the Search Asset Popup.
13. Admin selects an asset.

### Enter Assignment Details
14. Admin enters the assigned date.
- **Alt Path**: If the assigned date is valid (greater than or equal to the current date):
  - System displays the assigned date on the input field.
- **Alt Path**: If the assigned date is invalid:
  - System displays an error message.

15. Admin enters optional notes for the assignment.

### Save or Discard Assignment
16. Admin clicks on the Save Button.
  - System validates the fields.
  - System inserts the assignment data into the Database with the status "Waiting for acceptance".
  - System redirects the Admin to the Manage Assignment Page.
  - System displays the new assignment in the list.

- *Alt Path**: Admin* clicks on the Cancel Button.
  - System displays a discard confirmation popup.
  - **Alt Path**: If the admin clicks "discard":
    - System redirects to the Manage Assignment Page.
  - **Alt Path**: If the admin does not discard:
    - System redirects to the Create Assignment Page.

## Diagram
![SD_AssetManagement_CreateAssignment.png](/.attachments/SD_AssetManagement_CreateAssignment-dec8e9c2-6e6c-4589-ba75-f6e5b8272928.png)

## Notes
- The system ensures the assigned date is valid to avoid future conflicts.
- The discard confirmation popup helps prevent accidental loss of data during assignment creation.
- The assignment list on the Manage Assignment Page updates dynamically to reflect new or updated assignments.

# III. Sequence Diagram: Staff Response to His/Her Assignment Flow

## Overview
This sequence diagram illustrates the process of managing assignments within the system. It covers the scenarios where a staff member accepts or declines an assignment. The interactions between the Staff, System, Home Page, Confirmation Popup, and Database components are depicted to showcase the complete workflow.

## Participants
1. **Staff**: User interacting with the system.
2. **System**: The main backend system handling logic and state changes.
3. **Home Page**: The initial user interface where assignments are displayed.
4. **Confirmation Popup**: The UI element prompting user confirmation for actions.
5. **Database**: The storage system holding assignment data.

## Flow Description
### Login and Initial Display
1. **Staff** logs in using a username and password.
2. **System** displays the home page.
3. **System** fetches assignment data from the **Database**.
4. **System** displays the fetched assignment data on the home page.

### Accepting an Assignment
- **Alt Path**: Staff clicks the Accept button.
  - **System** displays a confirmation popup.
  - **Alt Path**: Staff clicks "Yes" on the confirmation popup.
    - **System** changes the state of the assignment to Accepted in the **Database**.
    - **System** displays a toast notification indicating the assignment is accepted.
    - **System** disables the Accept button for that assignment.
    - **System** closes the confirmation popup.
  - **Alt Path**: Staff clicks "No" on the confirmation popup.
    - **System** closes the confirmation popup.

### Declining an Assignment
- **Staff** clicks the Decline button.
  - **System** displays a confirmation popup.
  - **Alt Path**: Staff clicks "Yes" on the confirmation popup.
    - **System** changes the state of the assignment to Declined in the **Database**.
    - **System** displays a toast notification indicating the assignment is declined.
    - **System** closes the confirmation popup.
    - **System** removes the assignment from the list displayed on the home page.
  - **Alt Path**: Staff clicks "No" on the confirmation popup.
    - **System** closes the confirmation popup.

## Diagram
![SD_AssetManagement_StaffResponseAssignment.png](/.attachments/SD_AssetManagement_StaffResponseAssignment-72118645-fc0d-4f3c-8a64-66d86ea9b7da.png)

## Notes
- The confirmation popup serves as a safeguard to prevent accidental changes to assignment states.
- Toast notifications provide immediate feedback to the user about the success of their actions.
- The assignment list on the home page updates dynamically to reflect the current state of assignments.

# IV. Sequence Diagram: Create Request For Return Asset Flow

## Overview
This sequence diagram illustrates the process of returning an assignment within the system. It covers the scenario where a staff member initiates a return request for an assignment. The interactions between the Staff, System, Home Page, Confirmation Popup, and Database components are depicted to showcase the complete workflow.

## Participants
1. **Staff**: User interacting with the system.
2. **System**: The main backend system handling logic and state changes.
3. **Home Page**: The initial user interface where assignments are displayed.
4. **Confirmation Popup**: The UI element prompting user confirmation for actions.
5. **Database**: The storage system holding assignment data.

## Flow Description
### Login and Initial Display
1. **Staff** logs in using a username and password.
2. **System** displays the home page.
3. **System** fetches assignment data from the **Database**.
4. **System** returns assignment data.
5. **System** displays the fetched assignment data on the home page.

### Returning an Assignment
- **Staff** clicks the Return button.
  - **System** displays a confirmation popup.
  - **Alt Path**: Staff clicks "Yes" on the confirmation popup.
    - **System** saves the return request to the **Database**.
    - **System** displays a toast notification indicating the return request was created successfully.
    - **System** changes the state of the assignment to "Waiting for returning".
    - **System** disables the Return button for that assignment.
    - **System** closes the confirmation popup.
  - **Alt Path**: Staff clicks "No" on the confirmation popup.
    - **System** closes the confirmation popup.

## Diagram
![SD_AssetManagement_CreateRequestReturn.png](/.attachments/SD_AssetManagement_CreateRequestReturn-d1448f1a-31ca-4f60-ad6e-36b39f9f6d5e.png)

## Notes
- The confirmation popup serves as a safeguard to prevent accidental return requests.
- Toast notifications provide immediate feedback to the user about the success of their actions.
- The assignment list on the home page updates dynamically to reflect the current state of assignments.


# V. Sequence Diagram: Request for Return Completion Flow

## Overview
This sequence diagram illustrates the process of completing a request for return within the system. It covers the scenarios where an admin completes a request and confirms the completion. The interactions between the Admin, System, "Request For Return Page", "Confirmation Popup", and Database components are depicted to showcase the complete workflow.

## Participants
1. **Admin**: The individual managing return requests.
2. **System**: The backend system handling the logic and state changes for return requests.
3. **Request For Return Page**: The interface where the admin views return requests.
4. **Confirmation Popup**: The UI element prompting the admin to confirm the completion of a request.
5. **Database**: The storage system holding return request data.

## Flow Description
### Access Request for Return Page
1. Admin navigates to the Request For Return Page.
2. System fetches the request for return data from the Database.
3. System returns the request for return data.
4. System displays the request for return data on the Request For Return Page.

### Complete Request for Return
5. Admin clicks on the Complete Button.
6. System opens the Confirmation Popup.

### Confirm Completion
- **Alt Path**: If the admin clicks "Yes" on the Confirmation Popup:
  - System changes the status of the request for return to "Completed" in the Database.
  - System returns a success message.
  - System displays the success message on the Confirmation Popup.
  - System closes the Confirmation Popup.
  - System updates the status to Completed on the Request For Return Page.

### Decline Completion
- **Alt Path**: If the admin clicks "No" on the Confirmation Popup:
  - System closes the Confirmation Popup.

## Diagram
![SD_AssetManagement_CompleteRequestReturn.png](/.attachments/SD_AssetManagement_CompleteRequestReturn-8644dda1-7ab9-4986-8cb1-3dfb0ddf3455.png)

## Notes
- The confirmation popup ensures that the admin verifies the action before changing the status of a request.
- The success message provides feedback to the admin about the successful completion of the request.
- The system dynamically updates the status on the request page after confirmation.