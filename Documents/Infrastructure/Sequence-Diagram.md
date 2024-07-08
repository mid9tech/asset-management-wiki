# Sequence Diagram: Assignment Management Flow

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
