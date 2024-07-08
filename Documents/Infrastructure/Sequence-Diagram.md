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
![User Login Flow](path_to_your_image)

## Notes
- The login process includes validation of credentials and user role-based redirection.
- The system enforces a password change for first-time logins to ensure security.
- Error messages guide the user in case of invalid credentials or other login issues.