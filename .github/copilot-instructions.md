---
name: Digital Resource Monitor
description: Project guidelines for the Digital.Resource.Monitor ASP.NET Core application
---

# Digital Resource Monitor - Development Guidelines

## Architecture & Patterns
- Use MVC pattern with clear separation between Controllers, Models, and Views
- Keep business logic in Models or separate service layers
- Controllers should be thin and delegate to services

## C# Code Standards
- Follow PascalCase for class names, method names, and properties
- Use camelCase for local variables and parameters
- Add XML documentation comments (`///`) to all public members
- Use `async/await` for all I/O operations
- Prefer dependency injection over direct instantiation

## ASP.NET Core Best Practices
- Use strongly-typed models instead of dynamic objects
- Implement proper error handling in all controllers
- Use `ActionResult<T>` for generic controller actions
- Configure logging appropriately in `Program.cs`
- Keep view logic minimal—complex logic belongs in controllers/models

## File Organization
- Place controllers in `/Controllers`
- Place models in `/Models`
- Place views in `/Views/<ControllerName>`
- Keep shared views in `/Views/Shared`
- Static assets (CSS, JS) in `/wwwroot`

## Configuration
- Use `appsettings.json` for shared settings
- Use `appsettings.Development.json` for environment-specific overrides
- Never commit sensitive credentials—use User Secrets or environment variables

## Testing & Quality
- Write meaningful error messages for validation failures
- Handle null checks gracefully
- Use appropriate HTTP status codes in responses
