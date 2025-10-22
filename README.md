# ASP.NET and ASP.NET Core Samples

Welcome to the ASP.NET and ASP.NET Core samples repository! This repository contains a collection of sample applications demonstrating various features and best practices for building web applications with ASP.NET and ASP.NET Core.

## 📖 What is this repository?

This repository provides practical examples and reference implementations for:

- **ASP.NET Framework samples**: Traditional ASP.NET samples including Web API, MVC, Identity, HttpClient, and Katana (OWIN) projects
- **ASP.NET Core samples**: Modern ASP.NET Core samples featuring Blazor, MVC, and security implementations

These samples are designed to help developers learn and understand specific features, patterns, and techniques when building web applications with Microsoft's ASP.NET technologies.

## 📂 Repository Structure

```
samples/
├── aspnet/          # ASP.NET Framework samples (.NET Framework 4.0-4.5)
│   ├── HttpClient/  # HttpClient usage examples
│   ├── Identity/    # ASP.NET Identity samples
│   ├── Katana/      # OWIN/Katana middleware samples
│   ├── MVC/         # ASP.NET MVC samples
│   └── WebApi/      # ASP.NET Web API samples
└── aspnetcore/      # ASP.NET Core samples (.NET Core 2.2-6.0)
    ├── blazor/      # Blazor component samples
    ├── mvc/         # ASP.NET Core MVC samples
    └── security/    # Security-related samples
```

## 🚀 Getting Started

### Prerequisites

To run the samples in this repository, you'll need the following installed on your machine:

#### For ASP.NET Framework Samples
- **Windows OS** (required for .NET Framework)
- **Visual Studio 2015 or later** (Community, Professional, or Enterprise)
  - Download from: https://visualstudio.microsoft.com/vs/
- **.NET Framework 4.0-4.5** (usually included with Visual Studio)
- **IIS Express** (included with Visual Studio)

#### For ASP.NET Core Samples
- **Operating System**: Windows, macOS, or Linux
- **.NET SDK** (.NET Core 2.2 or later, depending on the sample)
  - Download from: https://dotnet.microsoft.com/download
  - Recommended: .NET 6.0 SDK for the latest samples
- **IDE/Editor** (choose one):
  - Visual Studio 2019 or later (Windows/Mac)
  - Visual Studio Code with C# extension
  - JetBrains Rider

### Verifying Your Setup

Check if you have the required tools installed:

```bash
# Check .NET SDK installation (for ASP.NET Core)
dotnet --version
dotnet --list-sdks

# Check .NET Framework versions (Windows only, via PowerShell)
Get-ChildItem 'HKLM:\SOFTWARE\Microsoft\NET Framework Setup\NDP' -Recurse | Get-ItemProperty -Name version -EA 0 | Where { $_.PSChildName -Match '^(?!S)\p{L}'} | Select PSChildName, version
```

## 🏃 Running the Samples

### Running ASP.NET Core Samples

1. **Navigate to a sample directory**:
   ```bash
   cd samples/aspnetcore/blazor/FlightFinder
   ```

2. **Restore NuGet packages**:
   ```bash
   dotnet restore
   ```

3. **Build the project**:
   ```bash
   dotnet build
   ```

4. **Run the application**:
   ```bash
   cd FlightFinder.Server
   dotnet run
   ```

5. **Access the application**:
   - Open your browser and navigate to the URL shown in the console (typically `https://localhost:5001` or `http://localhost:5000`)

### Running ASP.NET Framework Samples (Windows only)

1. **Navigate to a sample directory**:
   ```bash
   cd samples/aspnet/WebApi/Todo
   ```

2. **Open the solution in Visual Studio**:
   ```bash
   # Open the .sln file in Visual Studio
   start Todo.sln
   ```
   Or open Visual Studio and use File → Open → Project/Solution

3. **Restore NuGet packages**:
   - In Visual Studio: Right-click on the solution → Restore NuGet Packages
   - Or use the Package Manager Console: `Update-Package -reinstall`

4. **Build the solution**:
   - Press `Ctrl+Shift+B` or go to Build → Build Solution

5. **Run the application**:
   - Press `F5` to run with debugging, or `Ctrl+F5` to run without debugging
   - The application will open in your default browser

### Alternative: Using Visual Studio Code

For ASP.NET Core samples, you can use Visual Studio Code:

1. **Open the sample folder**:
   ```bash
   code samples/aspnetcore/blazor/FlightFinder
   ```

2. **Install the C# extension** (if not already installed)

3. **Run the sample**:
   - Press `F5` or use the Run and Debug panel
   - Or use the integrated terminal: `dotnet run`

## 📚 Sample Categories

### ASP.NET Framework Samples

#### Web API Samples (~30+ samples)
Examples demonstrating REST API development, including:
- Action Results and Content Negotiation
- Authentication (Basic, Client Certificate)
- Batching and OData support
- Custom Model Binding and Formatters
- File Upload/Download
- Entity Framework integration
- Routing and Versioning

#### Identity Samples
Demonstrations of ASP.NET Identity features:
- Custom user storage (MySQL, custom membership)
- Password policies
- Migration from SimpleMembership
- OAuth/Social login integration
- Unit testing Identity controllers

#### Katana/OWIN Samples
Middleware and self-hosting examples:
- Custom OWIN servers
- WebSocket support
- SignalR integration
- Static file serving

#### MVC Samples
ASP.NET MVC feature demonstrations:
- Attribute routing
- Custom authentication

### ASP.NET Core Samples

#### Blazor Samples
Modern interactive web UI components:
- **FlightFinder**: Complete Blazor application example
- **BinarySubmit**: Binary file submission handling
- **InputLargeTextArea**: Large text area component for performance
- **JSComponentGeneration**: JavaScript component generation
- **Validation**: Form validation examples

#### MVC Samples
ASP.NET Core MVC features:
- **Domain Routing**: Host-based routing with domain matching
- **Produces**: Content negotiation with produces matcher policy
- **RenderViewToString**: Server-side view rendering
- **RuntimeCompilation**: Runtime view compilation

#### Security Samples
Authentication and authorization examples

## 🔧 Common Commands Reference

### .NET Core CLI Commands

```bash
# Create a new project (example)
dotnet new web -n MyNewApp

# Restore dependencies
dotnet restore

# Build the project
dotnet build

# Run the project
dotnet run

# Run with specific configuration
dotnet run --configuration Release

# Publish for deployment
dotnet publish -c Release -o ./publish

# Run tests
dotnet test

# Watch for changes and auto-rebuild
dotnet watch run

# Add a NuGet package
dotnet add package <PackageName>

# List installed packages
dotnet list package
```

### Visual Studio Commands

- **Build**: `Ctrl+Shift+B`
- **Run with Debugging**: `F5`
- **Run without Debugging**: `Ctrl+F5`
- **Clean Solution**: Build → Clean Solution
- **Rebuild Solution**: Build → Rebuild Solution
- **Manage NuGet Packages**: Right-click project → Manage NuGet Packages

## 🛠️ Troubleshooting

### Common Issues and Solutions

#### "SDK not found" Error
```bash
# Install the required .NET SDK version
# Check the TargetFramework in the .csproj file and install matching SDK
dotnet --list-sdks
```

#### Port Already in Use
```bash
# Change the port in launchSettings.json or appsettings.json
# Or specify a different port when running:
dotnet run --urls "http://localhost:5001"
```

#### NuGet Package Restore Failures
```bash
# Clear NuGet caches
dotnet nuget locals all --clear

# Then restore
dotnet restore
```

#### Certificate Trust Issues (HTTPS)
```bash
# Trust the development certificate
dotnet dev-certs https --trust
```

## 📖 Additional Resources

### Documentation
- [ASP.NET Documentation](https://docs.microsoft.com/aspnet/)
- [ASP.NET Core Documentation](https://docs.microsoft.com/aspnet/core/)
- [.NET API Browser](https://docs.microsoft.com/dotnet/api/)

### Learning Resources
- [ASP.NET Core Tutorials](https://dotnet.microsoft.com/learn/aspnet)
- [Blazor Documentation](https://docs.microsoft.com/aspnet/core/blazor/)
- [Entity Framework Core](https://docs.microsoft.com/ef/core/)

### Community
- [ASP.NET Forums](https://forums.asp.net/)
- [Stack Overflow - ASP.NET Tag](https://stackoverflow.com/questions/tagged/asp.net)
- [.NET Foundation](https://dotnetfoundation.org/)

## 📜 License

This project is licensed under the Apache License 2.0 - see the [LICENSE.txt](LICENSE.txt) file for details.

## 🤝 Contributing

This repository contains samples maintained by the .NET Foundation. For contribution guidelines, please see the [Code of Conduct](CODE-OF-CONDUCT.md).

## 🔗 Related Repositories

- [ASP.NET Core Source](https://github.com/dotnet/aspnetcore)
- [.NET Runtime](https://github.com/dotnet/runtime)
- [Entity Framework Core](https://github.com/dotnet/efcore)

---

**Note**: Some samples may target older versions of .NET (Core) or .NET Framework. Check each sample's project file (`.csproj`) for specific version requirements and dependencies.
