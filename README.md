# learnwasm

A Blazor Server web application built with .NET 10 that provides a web interface for searching [Microsoft Learn](https://learn.microsoft.com) documentation via the [Learn MCP Server](https://learn.microsoft.com/api/mcp).

## Prerequisites

- [.NET 10 SDK](https://dotnet.microsoft.com/download/dotnet/10.0)

## Getting Started

```bash
dotnet run --project learnwasm
```

The app will be available at `https://localhost:5001` (or the port shown in the terminal).

## Running Tests

```bash
dotnet test
```

## Project Structure

```
learnwasm.sln
learnwasm/                  # Blazor Server web app
  Components/
    Layout/                 # Shared layout components (MainLayout, NavMenu)
    Pages/                  # Page components (Home, Error, NotFound)
    App.razor               # Root application component
  wwwroot/                  # Static assets (CSS, images, JS libs)
  Program.cs                # Application entry point and service configuration
learnwasm.Tests/            # xUnit + bUnit test project
  HomePageTests.cs          # Component tests for the Home page
  McpServerIntegrationTests.cs  # Integration tests against the live MCP API
```

## Tech Stack

- **Blazor Server** with Interactive Server render mode
- **.NET 10**
- **xUnit** and **bUnit** for testing
- **GitHub Actions** for CI/CD to Azure
