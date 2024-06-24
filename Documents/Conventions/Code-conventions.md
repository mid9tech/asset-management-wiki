

# Code Conventions

**1.	Backend**
-	Naming conventions: 
•	Classes: PascalCase (e.g., `UserService`, `UserController`)
•	Interface: PascalCase prefixed with `I` (e.g., IUserService).
•	Variables and Functions: camelCase (e.g., getUser, createUser).
•	File Names: kebab-case (e.g., user.service.ts, app.module.ts).
-	Space conventions:
•	Place a space before and after the operator: 
•	Place a space after each comma: 
 
-	Brackets:
•	Opening Brace `{`: Place the opening brace `{` at the end of the first line of the block. 
•	Use one space before the `{`.
•	Closing Brace `}`: Place the closing brace `}` on a new line.
•	Do not add any leading spaces before the `}`.
 
-	Semicolons: Use semicolons.
 
-	Comment conventions:
•	Write comments in English.
•	Do not add empty comments.
•	Begin single-line comments with a single space.

**2.	Frontend**
-	Using typecript.
-	Using Functional (Instead of Object-Oriented).
-	Prefer functional & immutable array methods (.ie map/filter/reduce/some/every over any types of mutable for loop.)
-	Use typescript aliases:
-	Don't Repeat Yourself
-	Components:
•	Break down components into smaller parts with minimal props to keep complexity low.
•	Ensure a prop name is indicative of what it does (eg., `isDisabled`, `isLoading`).
-	Using Tailwind for styling.
