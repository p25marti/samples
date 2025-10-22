# ASP.NET and ASP.NET Core Samples

This repository contains sample applications and code snippets that demonstrate various features and capabilities of ASP.NET and ASP.NET Core. These samples are designed to help developers learn and understand how to build web applications, APIs, and services using Microsoft's ASP.NET technologies.

## What's in this Repository?

This repository contains two main categories of samples:

### ASP.NET Samples ([samples/aspnet](samples/aspnet))
Traditional ASP.NET Framework samples including:
- **HttpClient** - Samples demonstrating HTTP client usage with various APIs (Bing Translate, Google Maps, Twitter, World Bank)
- **Identity** - ASP.NET Identity samples covering authentication, authorization, and user management
- **Katana** - OWIN/Katana middleware samples for ASP.NET
- **MVC** - ASP.NET MVC framework samples
- **Web API** - ASP.NET Web API samples covering RESTful services, routing, model binding, and more

### ASP.NET Core Samples ([samples/aspnetcore](samples/aspnetcore))
Modern ASP.NET Core samples including:
- **Blazor** - Blazor component samples (BinarySubmit, FlightFinder, InputLargeTextArea, JSComponentGeneration, Validation)
- **MVC** - ASP.NET Core MVC samples (domain routing, produces, view rendering, runtime compilation, testing)
- **Security** - Security-related samples for ASP.NET Core

## Prerequisites

Before running these samples, ensure you have the following installed:

### For ASP.NET Samples
- **Windows OS** (recommended for full .NET Framework support)
- **Visual Studio 2019 or later** with ASP.NET and web development workload
  - Download from: https://visualstudio.microsoft.com/downloads/
- **.NET Framework 4.5 or later** (typically included with Visual Studio)
- **NuGet Package Manager** (included with Visual Studio)

### For ASP.NET Core Samples
- **.NET SDK 5.0, 6.0, or later** depending on the sample
  - Download from: https://dotnet.microsoft.com/download
  - Check your installation: `dotnet --version`
- **Visual Studio 2019/2022** (Windows) or **Visual Studio Code** (cross-platform)
  - VS Code download: https://code.visualstudio.com/
  - With C# extension: https://marketplace.visualstudio.com/items?itemName=ms-dotnettools.csharp
- **Git** (for cloning the repository)
  - Download from: https://git-scm.com/downloads

## Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/aspnet/samples.git
cd samples
```

### 2. Choose a Sample

Navigate to the sample you want to explore. For example:

```bash
# For an ASP.NET Core Blazor sample
cd samples/aspnetcore/blazor/BinarySubmit

# For an ASP.NET Web API sample
cd samples/aspnet/WebApi/BasicAuthentication
```

### 3. Restore Dependencies

#### For ASP.NET Core samples:
```bash
dotnet restore
```

#### For ASP.NET Framework samples:
Open the `.sln` file in Visual Studio, and it will automatically restore NuGet packages.
Or use the command line:
```bash
nuget restore SolutionName.sln
```

### 4. Build the Sample

#### For ASP.NET Core samples:
```bash
dotnet build
```

#### For ASP.NET Framework samples:
```bash
msbuild SolutionName.sln
```
Or build using Visual Studio (Ctrl+Shift+B or Build > Build Solution).

### 5. Run the Sample

#### For ASP.NET Core samples:
```bash
dotnet run
```

The application will start and display the URL where it's running (typically `https://localhost:5001` or `http://localhost:5000`).

#### For ASP.NET Framework samples:
- Open the `.sln` file in Visual Studio
- Press F5 to run with debugging, or Ctrl+F5 to run without debugging
- The application will open in your default web browser

## Sample-Specific Instructions

Many samples include their own README or ReadMe.txt files with specific instructions, configuration requirements, and additional details. Always check for these files in the sample's directory:

```bash
# Look for readme files in a sample directory
find . -iname "readme*"
```

Some samples may require:
- API keys or credentials (e.g., Bing Translate, Twitter samples)
- Database setup (e.g., Identity samples with SQL Server)
- Additional configuration (check `appsettings.json`, `web.config`, or `app.config`)

## Exploring Samples

### Using Visual Studio
1. Open the `.sln` (solution) file in Visual Studio
2. Review the solution structure in Solution Explorer
3. Set the desired project as the startup project (right-click > Set as Startup Project)
4. Press F5 to run

### Using Visual Studio Code
1. Open the sample folder in VS Code
2. Open the integrated terminal (Ctrl+`)
3. Run `dotnet restore` and `dotnet run`
4. Open the provided URL in your browser

### Using Command Line
```bash
# Navigate to a sample with a .csproj file
cd samples/aspnetcore/blazor/BinarySubmit

# Restore, build, and run
dotnet restore
dotnet build
dotnet run
```

## Troubleshooting

### .NET SDK Version Issues
If a sample targets a specific .NET version you don't have installed:
- Install the required SDK version from https://dotnet.microsoft.com/download
- Or modify the `<TargetFramework>` in the `.csproj` file to match your installed version (may require code changes)

### Missing NuGet Packages
```bash
# Clear NuGet cache and restore
dotnet nuget locals all --clear
dotnet restore
```

### Port Already in Use
If you get a "port already in use" error:
- Change the port in `Properties/launchSettings.json` (ASP.NET Core)
- Or stop the conflicting application

### Build Errors
- Ensure you have the latest .NET SDK installed
- Check the sample's specific README for additional requirements
- Some older ASP.NET samples may require specific Visual Studio versions or .NET Framework versions

## Additional Resources

- **ASP.NET Documentation**: https://docs.microsoft.com/aspnet/
- **ASP.NET Core Documentation**: https://docs.microsoft.com/aspnet/core/
- **ASP.NET MVC Samples**: http://www.asp.net/mvc/samples
- **ASP.NET Web API Samples**: http://www.asp.net/web-api/samples
- **Source Code Repository**: https://github.com/aspnet/
- **.NET Foundation**: https://dotnetfoundation.org/

## Contributing

For information about contributing to this repository, please see the [CODE-OF-CONDUCT.md](CODE-OF-CONDUCT.md) file.

## License

These samples are licensed under the Apache License 2.0. See the [LICENSE.txt](LICENSE.txt) file for details.

---

**Note**: Some samples may reference external services (APIs, databases) that require additional setup or credentials. Always review the sample-specific documentation before running.
