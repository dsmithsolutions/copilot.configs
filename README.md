# Copilot Configurations

A repository containing GitHub Copilot configuration files and Model Context Protocol (MCP) server configurations for enhanced AI-assisted development.

## Contents

### GitHub Copilot Instructions
The `.copilot/` directory contains language-specific instruction files that guide Copilot's code generation:

- **`csharp.md`** - C# coding guidelines focused on Azure Functions development
- **`infra.md`** - Infrastructure-as-Code guidelines for Bicep, YAML pipelines, and automation scripts
- **`python.md`** - Python development guidelines for Azure Functions and standalone scripts

### VS Code Settings
- **`settings.json`** - VS Code workspace settings that:
  - Configure Copilot to use the custom instruction files
  - Set up MCP servers for enhanced AI capabilities (sequential thinking and web fetch)

## Usage

1. Copy the `.copilot/` folder to your project root
2. Add the Copilot instruction configuration from `settings.json` to your workspace settings
3. Customize the instruction files based on your project's specific needs

The instruction files provide best practices for:
- Azure development patterns
- Security and configuration management
- Code structure and maintainability
- Testing and observability
