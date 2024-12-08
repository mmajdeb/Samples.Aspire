# Samples.Aspire

Welcome to **Samples.Aspire**, a cloud-native application built with the .NET Aspire framework. This project demonstrates how to leverage .NET Aspire for modern application development, incorporating prebuilt templates and best practices for resilience, observability, and service orchestration.

## Features

- **Blazor Web Frontend**: A feature-rich and interactive UI built using Blazor.
- **ASP.NET Core Minimal API**: A lightweight and fast backend service.
- **Redis Integration**: Configured for distributed caching to enhance performance.
- **Unified Telemetry and Diagnostics**: Includes logging, tracing, and health checks.
- **Comprehensive Test Suite**: Automated integration tests for quality assurance.

## Project Structure

The solution includes the following projects:

1. **AppHost**: The core orchestrator for managing service lifecycles and dependencies.
2. **ServiceDefaults**: Centralized configurations for resilience, discovery, and telemetry.
3. **ApiService**: Provides backend APIs using ASP.NET Core Minimal API.
4. **Web**: A Blazor frontend application connected to the backend.
5. **Test**: Integration tests using MSTest, NUnit, or xUnit.

## Prerequisites

- **Visual Studio 2022**: With ".NET and web development" workload installed.
- **.NET 8 SDK**: Required for .NET Aspire applications.
- **Redis**: For caching support.

## Getting Started

### Clone the Repository

```bash
git clone https://github.com/mmajdeb/Samples.Aspire.git
cd Samples.Aspire
```

### Build and Run

1. Open `Samples.Aspire.sln` in Visual Studio.
2. Set `Samples.Aspire.AppHost` as the startup project.
3. Press **F5** or click **Run**.

### Access the Application

- **Frontend**: [http://localhost:<port>/web](http://localhost:<port>/web)
- **API Service**: [http://localhost:<port>/apiservice](http://localhost:<port>/apiservice)

### Run Tests

Execute tests using the .NET CLI:

```bash
dotnet test
```

## Using the Aspire Dashboard

The app includes an **Aspire Dashboard** for managing and monitoring services:

- **Resources**: View service status, endpoints, and environment variables.
- **Logs and Traces**: Debug issues with structured logs and request traces.
- **Metrics**: Monitor key performance indicators.

## Extending the Project

### Adding New Services

1. Define the new service in the `AppHost` project.
2. Use `.AddProject()` to configure dependencies and connections.
3. Update `ServiceDefaults` for shared settings.

### Customizing Redis

Update `appsettings.json` to configure caching options:

```json
"Redis": {
  "Configuration": "localhost:6379",
  "InstanceName": "Samples.Aspire_"
}
```

### Integration Testing

Use the existing test project as a guide to add new test cases for endpoints and services.

## Resources

- [.NET Aspire Documentation](https://learn.microsoft.com/en-us/aspire)
- [Introduction to .NET Aspire](https://devblogs.microsoft.com/dotnet/introducing-dotnet-aspire)
