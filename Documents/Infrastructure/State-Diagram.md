

# State Flow and State Machine Diagrams
 The document is about the State Transitions of Assets, Assignments and Request Returns.

## Asset Scenarios and State Transitions

### Create Asset
- **Action**: Admin creates an asset.
- **State**: Initially `AVAILABLE` or `NOT_AVAILABLE`.

### Create Asset
- **Action**: Admin updates an asset.
- **State**: Initially `AVAILABLE` or `NOT_AVAILABLE` or `WAITING FOR RECYCLING` or `RECYCLED`.

### Delete Asset
- **Action**: Admin deletes an asset.
- **State**: Asset can be deleted only if it has never been assigned to any user.

![Assets_State_Diagram.png](/.attachments/Assets_State_Diagram-4ea50479-ebf4-4653-aecb-889dbd4c8a64.png)

## Assignment Scenarios and State Transitions

### Create Assignment
- **Action**: Admin creates a new assignment.
- **Information**: Assigned user, asset, future date (optional).
- **State**: Assignment starts as `WAITING_FOR_ACCEPTANCE`.

### Delete Assignment
- **Action**: Admin deletes an assignment.
- **State**: Assignment can be deleted only if it is in the `WAITING_FOR_ACCEPTANCE` state.

### User Respond to Assignment
- **Action**: User accepts or declines the assignment.
- **State**: 
  - If accepted, the assignment state changes to `ACCEPTED`.
  - If declined, the assignment state changes to `DECLINED`.

![Assignments_State_Diagram.png](/.attachments/Assignments_State_Diagram-4086fd79-c81c-45f1-9fe6-4142140c27a4.png)

## Request Return Scenarios and State Transitions

### Create Return Request
- **Action**: Admin creates a return request for an assigned asset.
- **State**: Return request starts as `WAITING_FOR_RETURNING`.

### Complete Return Request
- **Action**: Admin marks a return request as completed.
- **State**: 
  - Return request state changes to `COMPLETED`.
  - Assignment is marked as `isRemoved = true`.
  - Asset state changes back to `AVAILABLE`.

### Cancel Return Request
- **Action**: Admin cancels a return request.
- **State**: Return request state changes to `CANCELED`.

![RequestReturn_State_Diagram.png](/.attachments/RequestReturn_State_Diagram-8e66e0b3-8c7f-4d28-a0ff-a36e70a671cb.png)


