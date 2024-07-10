
**Project structure**
```
src/
├── domains/
│   ├── assets/
│   ├── assignments/
│   ├── request-returns/
│   ├── users/
├── services/
│   └── prisma/
├── shared/
│   ├── constants/
│   ├── enums/
│   ├── exceptions/
│   ├── generics/
│   ├── helpers/
├── app.module.ts
├── main.ts
└── schema.graphql
```
# Domains

### assets
Manages and handles all functionalities related to assets, such as asset creation, modification, and tracking.

### assignments
Contains features for managing assignments, including assignment creation, updates, tracking, and assignment-related operations.

### request-returns
Manages the request and return processes, including creating requests, approving/denying requests, and processing returns.

### users
Handles user-related functionalities such as user registration, authentication, profile management, and user roles.

### Services/prisma
Contains services related to database interactions using Prisma ORM, managing data access, and database operations.

# Shared

### Constants
Contains constants used throughout the application, ensuring consistency and easy maintenance.

### enums
Includes enumeration types used in the application for defining a set of named values.

### Exceptions
Handles custom exceptions and error handling logic for the application.

### Generics
Contains generic utilities and functions that can be used across different modules of the application.

### Helpers
Includes helper functions and utilities to support various functionalities within the application.

### app.module.ts
Contains the main module configuration for the application, including importing and configuring other modules and services.

