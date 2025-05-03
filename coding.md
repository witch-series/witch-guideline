# Coding Guidelines

This document outlines coding standards and best practices for Witch Series projects, with a particular focus on facilitating collaborative development between humans and AI systems.

## Guidelines

### General Coding Rules

#### Formatting Rules
- Use consistent indentation and spacing throughout the code.
- Limit lines to a reasonable length to enhance readability.
- Use UTF-8 encoding for all files.

#### Naming Conventions
- Follow the naming conventions standard for each programming language or framework used.
- Maintain consistency within each module or file.

#### Documentation
- Include comments to explain the purpose and functionality of code sections.
- Use docstrings or equivalent documentation methods to describe functions and classes.
- All comments and docstrings must be written in English to ensure global accessibility and AI compatibility.

#### Testing
- Write tests to verify the functionality of all implemented features.
- Place test files under a `test/` directory, following the same naming and structure as the corresponding source files.

### Modular Design
- Each feature should be implemented as an independent module to enhance reusability.
- Minimize dependencies between modules to ensure flexibility and scalability.
- Clearly define module interfaces (e.g., through function signatures or interface files) to improve clarity and reusability.
- These modular design principles also apply at higher levels of architecture, such as separating frontend from backend, or decoupling the core logic from GUIs.

#### Backend and Frontend Separation

- **Backend**:
  - Responsible for providing data and logic through APIs (e.g., REST, GraphQL).
  - Should be designed to be reusable across different interfaces.

- **Frontend**:
  - Focuses on user interface and user experience.
  - Communicates with the backend exclusively through defined APIs.

- **Core and GUI Separation**:
  - Core functionality should be implemented independently of the graphical user interface (GUI).
  - This separation ensures that the core logic can be reused in different contexts (e.g., CLI, web, desktop applications).
  - The GUI should act as a client to the core, interacting through well-defined interfaces.

### Implementing Executable Files

- All executable files must:
  - Support `--help` or `-h` arguments to display usage instructions.
  - Print informative error messages when required arguments are missing or invalid.

### File and Folder Relocation

- Design scripts and modules to be location-independent. Use absolute paths or configuration files to ensure that the code can run correctly even if the file or folder is moved.
- Avoid hardcoding file paths; instead, use environment variables or command-line arguments to specify paths dynamically.

### Documentation Updates for Changes

- When renaming or relocating files, folders, or classes, ensure that the corresponding `README.md` files in the affected folders are updated to reflect these changes.
- Include the new names and locations in the documentation to avoid confusion for future developers.

By adhering to these guidelines, developers can ensure consistency and maintainability across Witch Series projects.