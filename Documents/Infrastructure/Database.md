**Service** 
- Azure PostgreSQL Flexible Server

**Diagram**

![img.png](/.attachments/img-8857db3d-1523-41c0-b23f-db81fd37ebd0.png)

## Entities and Attributes

### User
- **id**: Unique identifier for the user.
- **firstName**: User's first name.
- **lastName**: User's last name.
- **staffCode**: Unique code assigned to the staff member.
- **username**: Username for user login.
- **password**: Encrypted user password.
- **gender**: User's gender.
- **salt**: Salt used for password encryption.
- **refreshToken**: Token used for session refresh.
- **isAssigned**: Flag indicating if the user is assigned an asset.
- **isDisabled**: Flag indicating if the user is disabled.
- **joinedDate**: Date when the user joined.
- **type**: Type of user (e.g., admin, regular).
- **dateOfBirth**: User's date of birth.
- **state**: Current state of the user.
- **createdAt**: Timestamp when the user was created.
- **updatedAt**: Timestamp when the user was last updated.
- **location**: User's location.

### Category
- **id**: Unique identifier for the category.
- **categoryCode**: Code representing the category.
- **categoryName**: Name of the category.
- **createdAt**: Timestamp when the category was created.
- **updatedAt**: Timestamp when the category was last updated.

### Asset
- **id**: Unique identifier for the asset.
- **assetCode**: Code representing the asset.
- **assetName**: Name of the asset.
- **categoryId**: Foreign key referencing the category to which the asset belongs.
- **installedDate**: Date when the asset was installed.
- **state**: Current state of the asset.
- **location**: Location of the asset.
- **specification**: Specifications of the asset.
- **isRemoved**: Flag indicating if the asset is removed.
- **isAllowRemoved**: Flag indicating if the asset is allowed to be removed.
- **isReadyAssigned**: Flag indicating if the asset is ready to be assigned.
- **createdAt**: Timestamp when the asset was created.
- **updatedAt**: Timestamp when the asset was last updated.

### Assignment
- **id**: Unique identifier for the assignment.
- **assetCode**: Code of the assigned asset.
- **assetName**: Name of the assigned asset.
- **assignedToId**: Foreign key referencing the user to whom the asset is assigned.
- **assignedToUsername**: Username of the assigned user.
- **assignedById**: Foreign key referencing the user who assigned the asset.
- **assignedByUsername**: Username of the user who assigned the asset.
- **assignedDate**: Date when the asset was assigned.
- **state**: Current state of the assignment.
- **note**: Additional notes about the assignment.
- **location**: Location where the asset is assigned.
- **isRemoved**: Flag indicating if the assignment is removed.
- **assetId**: Foreign key referencing the assigned asset.
- **createdAt**: Timestamp when the assignment was created.
- **updatedAt**: Timestamp when the assignment was last updated.

### RequestReturn
- **id**: Unique identifier for the return request.
- **requestedById**: Foreign key referencing the user who requested the return.
- **assignedDate**: Date when the return request was assigned.
- **acceptedById**: Foreign key referencing the user who accepted the return request.
- **returnedDate**: Date when the asset was returned.
- **state**: Current state of the return request.
- **assignmentId**: Foreign key referencing the related assignment.
- **createdAt**: Timestamp when the return request was created.
- **updatedAt**: Timestamp when the return request was last updated.
- **assetId**: Foreign key referencing the returned asset.
- **isRemoved**: Flag indicating if the return request is removed.

### Asset Report
- **category_name**: Name of the asset category.
- **total**: Total number of assets in the category.
- **assigned**: Number of assigned assets in the category.
- **available**: Number of available assets in the category.
- **not_available**: Number of not available assets in the category.
- **waiting_for_recycling**: Number of assets waiting for recycling in the category.
- **recycled**: Number of recycled assets in the category.

## Relationships

- **User to Assignment**: One user can have multiple assignments (one-to-many).
- **Asset to Assignment**: One asset can have multiple assignments (one-to-many).
- **Category to Asset**: One category can have multiple assets (one-to-many).
- **Assignment to RequestReturn**: One assignment can have multiple return requests (one-to-many).
- **User to RequestReturn**: One user can request multiple returns (one-to-many).
- **Asset to RequestReturn**: One asset can have multiple return requests (one-to-many).