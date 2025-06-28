# GitHub Copilot Instructions for Infrastructure Code

You are assisting with infrastructure-as-code and automation scripts using:
- Bicep for Azure resource provisioning
- YAML for Azure DevOps pipelines
- Bash and PowerShell for automation and deployment tasks

## Agent Behavior
- Use full file and folder context when generating or modifying scripts or templates.
- Follow Azure best practices for security, modularity, and clarity.
- Avoid generating redundant or unsupported syntax.
- Do not hardcode secrets or environment-specific values.

## Bicep
- Use parameterization and modules for reusable components.
- Follow the latest Azure Bicep syntax and structure.
- Prefer `existing` resource references instead of redeclaring shared resources.
- Set secure defaults (e.g., HTTPS-only, network rules, encryption).
- Include descriptive comments for all parameters and outputs.

## Azure Pipelines (YAML)
- Follow indentation and schema rules strictly.
- Use templates or stages for reusability when applicable.
- Default to using `$(...)` syntax for variables.
- Support `condition`, `dependsOn`, and `displayName` for clarity in pipeline steps.
- Avoid hardcoded secrets — assume variables are defined securely in the pipeline UI or variable groups.

## Bash & PowerShell
- Prefer idempotent and safe operations.
- Use inline comments to explain command logic and flags.
- Use `set -euo pipefail` in Bash for safer execution.
- For PowerShell, follow standard formatting and include error handling (`try/catch`, `-ErrorAction`).
- Avoid interactive prompts — scripts should be automation-friendly.

## Security & Maintainability
- Never suggest inline secrets or keys.
- Use environment variables, Azure Key Vault references, or secure pipeline variables.
- Ensure generated scripts or templates can run in CI/CD environments.
- Maintain readability and modularity for team collaboration.

Use concise, clear, production-ready syntax. Make automation secure, maintainable, and consistent with Azure standards.
