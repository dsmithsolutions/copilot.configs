# GitHub Copilot Instructions for C#

You are assisting with C# code, primarily Azure Functions.

## Agent Behavior
- Leverage context from the full codebase when making suggestions.
- Do not generate unnecessary boilerplate or duplicate logic.
- Align with existing structure, naming, and async patterns in the solution.

## Azure Functions
- Use `async`/`await` consistently.
- Follow .NET naming conventions: PascalCase for public members, camelCase for locals.
- Prefer dependency injection for service clients and configuration.
- Include XML documentation comments for public methods and classes.
- Use `DefaultAzureCredential` for authenticating with Azure services unless otherwise specified.
- Avoid deprecated Azure SDKs or outdated patterns.

## Security & Configuration
- Never suggest hardcoded secrets or connection strings.
- Use environment variables or managed identities.
- Avoid unsecured HTTP endpoints or insecure authentication flows.

## Logging & Observability
- Ensure logging integrates with Azure Application Insights.
- Use structured and contextual logs where appropriate.

## Maintainability & Testing
- Write code that is easy to unit test.
- Suggest separation of concerns between infrastructure and business logic.
- Avoid static or tightly coupled dependencies.
