# Structure Documentation

This document defines the directory structure and documentation guidelines for projects.

## Required Directory Structure

```
/project-root
│
├── src/         # Core implementation code
├── examples/    # Example code
├── test/        # Test code
├── tmp/         # Temporary files and data
├── user/        # User-specific files
├── locales/     # Language translations
├── images/      # Image storage
└── ...
```

## Documentation Guidelines

- Each directory (e.g., `src/`, `examples/`) must include a `README.md` summarizing its purpose and key components.
- Use clear and concise language in all documentation.

## README Writing Templates

### Project Root README (e.g., `/README.md`)
1. **Overview**: Explain the overall purpose and background of the project.
2. **Installation & Usage**: Provide installation steps and basic usage instructions.
3. **Structure**: Describe the directory layout and key files.
4. **License & Credits**: Include license information and acknowledgments.

### Folder-Level README (e.g., `/src/README.md`)
1. **Purpose**: Describe the folder's role within the project.
2. **Contents**: List and summarize important files or submodules.
3. **Usage Notes**: Any specific usage or dependency instructions.

## Including Witch Guideline and Witch Core

To include this repository (`witch-guideline`) and `Witch Core` as submodules:

1. Add `witch-guideline` as a submodule:
   ```bash
   git submodule add https://github.com/witch-series/witch-guideline.git witch-guideline
   ```

2. Add `Witch Core` as a submodule:
   ```bash
   git submodule add https://github.com/witch-series/witch-core.git witch-core
   ```

3. Initialize and update submodules:
   ```bash
   git submodule update --init --recursive
   ```

4. Periodically update submodules:
   ```bash
   git pull --recurse-submodules
   ```

## Python Virtual Environments

- Use virtual environments prefixed with `pyenv` for Python projects to isolate dependencies (e.g., `pyenv-myproject`).
- Activate the virtual environment before installing packages or running the project.

## Testing Guidelines

- Write tests to verify the functionality of all implemented features.
- Organize test files to mirror the structure of the main codebase.
- Ensure that tests cover edge cases and common scenarios.
- Use descriptive names for test cases to clearly indicate their purpose.

## Relationship Between Samples and Core

- **src/**: Directory for implementing the core functionality of the project.
- **examples/**: Provides examples that demonstrate the usage of features defined in `src/`.
  - `examples` also serves as a learning resource to naturally understand how to use `src` functionalities.
  - Focused on learning, usually includes manual usage code or sample apps.
- **test/**: Contains unit and integration tests to ensure correctness of code.
  - Focused on validation, using automated assertions.

## Internationalization (i18n) and Image Storage

- **i18n**: Use a `locales/` folder with subfolders for each language (e.g., `en/`, `ja/`).
  - Use consistent keys across translations.
- **Images**: Store all images in an `images/` folder to maintain organization.
  - Use lowercase and hyphen-separated names for image files (e.g., `robot-diagram.png`).

## .gitignore Recommendations

Include the following items in `.gitignore`:

- **Python Virtual Environments**: `pyenv*/`
- **Temporary Files**: `*.tmp`, `*.log`
- **Temporary and User-Specific Folders**: `tmp/`, `user/`

By following this structure, projects can maintain clarity and consistency, making them accessible to both human and AI collaborators.