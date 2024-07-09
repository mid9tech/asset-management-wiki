## Backend Development (NestJS)

### Naming Conventions:
- **Classes:** Use PascalCase (e.g., `UserService`, `UserController`). Classes represent entities or controllers.
- **Interfaces:** PascalCase prefixed with 'I' (e.g., `IUserService`). Interfaces describe data structures and should be clear and descriptive.
- **Variables and Functions:** camelCase (e.g., `getUser`, `createUser`). Use meaningful names that convey their purpose.
- **File Names:** kebab-case (e.g., `user.service.ts`, `app.module.ts`). File names should be descriptive and reflect their content.

### Spacing Conventions:
- Place a space before and after each operator (`=`, `+`, `-`, etc.) for readability and consistency.
- Place a space after each comma in function arguments and array elements to enhance readability.

### Brackets:
- Opening Brace `{`: Place at the end of the first line, with one space before it (`functionName() {`).
- Closing Brace `}`: Place on a new line, without leading spaces before it. Ensure proper indentation for nested blocks.

### Semicolons:
- Use semicolons to end statements. This practice enhances code clarity and prevents potential issues with automatic semicolon insertion.

### Comments:
- Write comments in English for consistency and accessibility.
- Avoid empty comments—they clutter the code without adding value.
- Single-line comments should begin with a single space (`// This is a comment`).

---

## Frontend Development (TypeScript with Functional Approach)

### General Practices:
- Use TypeScript for type safety and improved development experience.
- Prefer functional programming paradigms and immutable array methods (`map`, `filter`, `reduce`) for data transformation and manipulation.

### TypeScript Usage:
- Utilize TypeScript aliases (`type` or `interface`) to define complex types and enhance code readability and maintainability.

### Componentization:
- Break down UI components into smaller, reusable parts with minimal dependencies and clear responsibilities.
- Use indicative prop names (e.g., `isDisabled`, `isLoading`) to clearly communicate component state and behavior.

### Styling:
- Adopt Tailwind CSS for styling to leverage utility-first and responsive design principles.
- Avoid inline styles and use Tailwind's utility classes to maintain consistency and ease of maintenance.

### Best Practices:
- Follow the Single Responsibility Principle (SRP) by ensuring each function, class, or component has a single, well-defined purpose.
- Use meaningful variable and function names that accurately describe their functionality.
- Regularly refactor and review code to improve readability, maintainability, and performance.
- Document code when necessary, focusing on explaining 'why' rather than 'what' (the latter should be clear from the code itself).

By adhering to these coding conventions and best practices, you can create maintainable, scalable, and robust applications with NestJS and TypeScript, ensuring clarity and consistency across your codebase.
