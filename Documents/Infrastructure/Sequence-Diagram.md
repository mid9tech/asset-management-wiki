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
![SD_AssetManagement_Login.png](/.attachments/SD_AssetManagement_Login-f5c506ce-f47b-474d-9c42-cbdc9f49a348.png)

## Notes
- The login process includes validation of credentials and user role-based redirection.
- The system enforces a password change for first-time logins to ensure security.
- Error messages guide the user in case of invalid credentials or other login issues.

# II. Sequence Diagram: Assignment Create Flow

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
![SD_AssetManagement_CreateAssignment.png](/.attachments/SD_AssetManagement_CreateAssignment-b5a1931a-f164-4099-9565-f315a269fa41.png)

## Notes
- The confirmation popup serves as a safeguard to prevent accidental changes to assignment states.
- Toast notifications provide immediate feedback to the user about the success of their actions.
- The assignment list on the home page updates dynamically to reflect the current state of assignments.

# III. Sequence Diagram: Asset Return Flow

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
![SD_AssetManagement_CreateRequestReturn.png](/.attachments/SD_AssetManagement_CreateRequestReturn-854c8f15-d3a7-41ab-8a76-287777cd5c16.png)

## Notes
- The confirmation popup serves as a safeguard to prevent accidental return requests.
- Toast notifications provide immediate feedback to the user about the success of their actions.
- The assignment list on the home page updates dynamically to reflect the current state of assignments.


# IV. Sequence Diagram: Assignment Management Flow

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
![SD_AssetManagement_StaffResponseAssignment.png](/.attachments/SD_AssetManagement_StaffResponseAssignment-f756a1cd-0c19-4483-ae7f-8b9e1cb758e9.png)

## Notes
- The confirmation popup serves as a safeguard to prevent accidental changes to assignment states.
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
![SD_AssetManagement_CompleteRequestReturn.png](/.attachments/SD_AssetManagement_CompleteRequestReturn-ad06a14e-b26c-45ad-80b6-bebc5068c5b8.png)

## Notes
- The confirmation popup ensures that the admin verifies the action before changing the status of a request.
- The success message provides feedback to the admin about the successful completion of the request.
- The system dynamically updates the status on the request page after confirmation.
