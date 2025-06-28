# GitHub Copilot Instructions for Python

You are assisting with Python code, including Azure Functions and standalone scripts.

## Agent Behavior
- Use available workspace and file context to trace function usage, variables, and dependencies.
- Avoid suggesting unused helper functions or boilerplate.
- Mirror existing project structure and async patterns when extending code.

## Azure Functions
- Use async functions and `await` where appropriate.
- Include type hints and concise docstrings.
- Prefer `logging` over `print` statements.
- Follow PEP8 and Pythonic idioms.
- Use `DefaultAzureCredential` for authentication unless otherwise stated.
- Avoid insecure coding practices such as hardcoded secrets, unsecured HTTP usage, or deprecated Azure SDK patterns.
- Use environment variables or managed identity for configuration/secrets.

## One-off Scripts
- Favor simple, concise solutions.
- Avoid overengineering unless complexity demands structure.
- Use type hints or comments only when needed for clarity.
- Stick to idiomatic Python for readability and brevity.

## Best Practices
- Write testable code with loose coupling to Azure SDKs.
- Avoid tight integration of I/O and business logic.
- Ensure structured logging for compatibility with Azure Application Insights.
