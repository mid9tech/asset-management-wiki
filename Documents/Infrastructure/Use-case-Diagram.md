![image.png](/.attachments/image-869123a1-91d9-4ec3-b8a7-802909543f5c.png)

# Asset Management System Use Case Diagram Explanation

## Actors
1. **Admin**: Responsible for overseeing and managing the entire system, including user, asset, category, and assignment management.
2. **Staff**: Engages with assignment-related functionalities such as accepting, declining, viewing assignments, and creating return requests.

## Modules and Use Cases

### 1. Authentication
- **Sign In**: Users (Admin and Staff) authenticate themselves to access the system functionalities.

### 2. User Management
- **Create**: Admin can add new users to the system.
- **Disable**: Admin can disable existing users to revoke their access.
- **View**: Admin can view user details.
- **Update**: Admin can update user information.

### 3. Asset Management
- **Create**: Admin can add new assets to the system.
- **Delete**: Admin can remove assets from the system.
- **View**: Admin can view details of assets.
- **Update**: Admin can update information related to assets.
- **Category Management**:
  - **View**: Admin can view asset categories.
  - **Create**: Admin can create new asset categories.
  - **View**: Admin can view existing asset categories.
  - **Update**: Admin can update asset categories.

### 4. Assignment Management
- **Create**: Admin can create new assignments for staff.
- **Delete**: Admin can delete existing assignments.
- **Update**: Admin can update assignment details.
- **View**: Admin can view assignment details.
- **Accept**: Staff can accept assignments.
- **Decline**: Staff can decline assignments.

### 5. Request Return Management
- **Create**: Both Admin and Staff can create return requests.
- **View**: Admin can view return request details.
- **Delete**: Admin can delete return requests.
- **Complete**: Admin can mark return requests as complete.

### 6. Report Management
- **View**: Admin can view reports related to system activities.
- **Export**: Admin can export reports for further analysis.
