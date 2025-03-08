# Cursor Rules Collection

A collection of custom rules for [Cursor](https://cursor.sh/), the AI-powered code editor. These rules help customize AI behavior for specific programming languages and workflows.

## What are Cursor Rules?

Cursor Rules are custom instructions for the AI assistant in Cursor, guiding its behavior when interpreting code, generating suggestions, and responding to queries. They can be:

- **Global Rules**: Set in Cursor Settings under `General` > `Rules for AI`
- **Project-Specific Rules**: Defined in the `.cursor/rules` directory in your project

## Rules in this Repository

This repository contains rules for:

- **Go**: Best practices for Go development, including dependency management
- **Python**: Guidelines for using `uv` for Python project management
- **Meta Rules**: Rules for creating and improving Cursor rules themselves

## How to Use These Rules

1. **Global Usage**:
   - Copy the content of any `.mdc` file
   - Go to Cursor Settings > General > Rules for AI
   - Paste the content into the text area

2. **Project-Specific Usage (Recommended: Symlink)**:
   - Instead of copying files, create symbolic links to the rule files in this repository
   - This allows you to automatically get updates when the repository is updated
   - Create the `.cursor/rules` directory in your project if it doesn't exist
   - Symlink the desired `.mdc` files:
     ```bash
     # Example for Unix/Linux/macOS
     ln -s /path/to/this/repo/go/go-mod-handling.mdc /path/to/your/project/.cursor/rules/
     
     # Example for Windows (requires admin privileges)
     mklink /path/to/your/project/.cursor/rules/go-mod-handling.mdc /path/to/this/repo/go/go-mod-handling.mdc
     ```

3. **Alternative: Manual Copy**:
   - Copy the content of any `.mdc` file
   - Create a file in the `.cursor/rules` directory of your project
   - Paste the content into this file
   - You can use the command palette with `Cmd + Shift + P` > `New Cursor Rule`

## Contributing

Feel free to contribute your own Cursor rules by submitting a pull request!

## Resources

- [Official Cursor Documentation on Rules for AI](https://docs.cursor.com/context/rules-for-ai)
- [Cursor Directory](https://cursor.directory/) - Community-curated collection of Cursor rules
