# ASP.NET Samples

This repository contains sample projects demonstrating various features and capabilities of ASP.NET and ASP.NET Core frameworks. These samples are provided by the .NET Foundation to help developers learn and understand different aspects of web development with ASP.NET technologies.

## What's Included

This repository includes two main categories of samples:

### ASP.NET Framework Samples
Located in the [samples/aspnet](samples/aspnet) directory, these samples demonstrate:
- **HttpClient** - Examples of using HttpClient for various web services (Bing Translate, Google Maps, Twitter, World Bank)
- **Identity** - Authentication and authorization samples including MySQL integration, password policies, single sign-out, and more
- **Katana** - OWIN/Katana middleware samples
- **MVC** - ASP.NET MVC framework examples
- **WebApi** - Extensive collection of ASP.NET Web API samples including custom formatters, model binding, authentication, file uploads, and more

### ASP.NET Core Samples
Located in the [samples/aspnetcore](samples/aspnetcore) directory, these samples demonstrate:
- **Blazor** - Server-side and client-side Blazor samples including validation, binary submit, flight finder, and JS component generation
- **MVC** - ASP.NET Core MVC samples including domain routing, produces attribute usage, runtime compilation, and testing
- **Security** - Security and authentication examples for ASP.NET Core

## Prerequisites

To run these samples, you'll need:

### For ASP.NET Framework Samples
- **Windows OS** (required for .NET Framework)
- **Visual Studio 2017 or later** (Community, Professional, or Enterprise edition)
  - Download from: https://visualstudio.microsoft.com/downloads/
- **.NET Framework 4.5 or later**
  - Included with Visual Studio or available from: https://dotnet.microsoft.com/download/dotnet-framework
- **IIS Express** (included with Visual Studio)

### For ASP.NET Core Samples
- **.NET Core SDK 2.2, 3.0, or later** (depending on the specific sample)
  - Download from: https://dotnet.microsoft.com/download
  - Check installed version: `dotnet --version`
- **Visual Studio 2019 or later**, **Visual Studio Code**, or **any text editor**
  - Visual Studio: https://visualstudio.microsoft.com/downloads/
  - VS Code: https://code.visualstudio.com/
- **C# Extension for VS Code** (if using VS Code)
  - Install from VS Code marketplace

## Getting Started

### Clone the Repository

```bash
git clone https://github.com/aspnet/samples.git
cd samples
```

### Running ASP.NET Framework Samples

1. Navigate to the sample directory:
   ```bash
   cd samples/aspnet/<category>/<sample-name>
   ```

2. Open the solution file (`.sln`) in Visual Studio:
   ```bash
   # On Windows, you can open directly from command line
   start <SampleName>.sln
   ```

3. Restore NuGet packages:
   - In Visual Studio: Right-click solution → "Restore NuGet Packages"
   - Or build the solution (packages will restore automatically)

4. Build and run:
   - Press `F5` to build and run with debugging
   - Or press `Ctrl+F5` to run without debugging
   - The application will typically launch in your default web browser

### Running ASP.NET Core Samples

1. Navigate to the sample directory:
   ```bash
   cd samples/aspnetcore/<category>/<sample-name>
   ```

2. **Option A: Using the .NET CLI (recommended for quick testing)**
   
   Restore dependencies:
   ```bash
   dotnet restore
   ```
   
   Build the project:
   ```bash
   dotnet build
   ```
   
   Run the application:
   ```bash
   dotnet run
   ```
   
   The application will start and display the URL (typically `http://localhost:5000` or `https://localhost:5001`)

3. **Option B: Using Visual Studio**
   
   - Open the solution or project file (`.sln` or `.csproj`)
   - Press `F5` to build and run with debugging
   - Or press `Ctrl+F5` to run without debugging

4. **Option C: Using Visual Studio Code**
   
   - Open the sample folder in VS Code
   - Press `F5` to run with debugging (requires C# extension)
   - Or use the integrated terminal to run `dotnet run`

### Sample-Specific Instructions

Many samples include their own README or ReadMe.txt files with specific setup instructions, API keys requirements, or configuration steps. Always check the sample's directory for additional documentation:

```bash
# Look for README files in sample directories
cat samples/aspnet/<category>/<sample-name>/ReadMe.txt
cat samples/aspnetcore/<category>/<sample-name>/README.md
```

## Common Commands Reference

### .NET Core CLI Commands

```bash
# Check installed .NET SDK version
dotnet --version

# List all installed SDKs
dotnet --list-sdks

# Restore project dependencies
dotnet restore

# Build the project
dotnet build

# Run the application
dotnet run

# Run with specific configuration
dotnet run --configuration Release

# Clean build artifacts
dotnet clean

# Run tests (if project has tests)
dotnet test

# Publish the application for deployment
dotnet publish -c Release -o ./publish
```

### Visual Studio Commands

- **Build Solution**: `Ctrl+Shift+B`
- **Run with Debugging**: `F5`
- **Run without Debugging**: `Ctrl+F5`
- **Clean Solution**: Right-click solution → Clean Solution
- **Rebuild Solution**: Right-click solution → Rebuild Solution

## Troubleshooting

### Common Issues

**Issue**: "The specified SDK version was not found"
- **Solution**: Install the required .NET Core SDK version specified in the project file or `global.json`

**Issue**: "Unable to restore NuGet packages"
- **Solution**: Check your internet connection and clear NuGet cache: `dotnet nuget locals all --clear`

**Issue**: "Port already in use"
- **Solution**: Change the port in `launchSettings.json` or `appsettings.json`, or stop the process using the port

**Issue**: Missing API keys for samples (Twitter, Bing Translate, Google Maps)
- **Solution**: Register for API keys from the respective service providers and add them to the configuration files

## Project Structure

```
samples/
├── aspnet/              # ASP.NET Framework samples
│   ├── HttpClient/      # HttpClient usage examples
│   ├── Identity/        # Authentication and authorization
│   ├── Katana/          # OWIN/Katana middleware
│   ├── MVC/             # ASP.NET MVC samples
│   └── WebApi/          # Web API samples
└── aspnetcore/          # ASP.NET Core samples
    ├── blazor/          # Blazor framework samples
    ├── mvc/             # ASP.NET Core MVC samples
    └── security/        # Security and authentication
```

## Contributing

These samples are maintained by the .NET Foundation. If you'd like to contribute:

1. Check existing issues or create a new one to discuss your idea
2. Fork the repository
3. Create a feature branch
4. Make your changes with clear commit messages
5. Submit a pull request

Please read our [Code of Conduct](CODE-OF-CONDUCT.md) before contributing.

## Additional Resources

- **ASP.NET Documentation**: https://docs.microsoft.com/aspnet/
- **ASP.NET Core Documentation**: https://docs.microsoft.com/aspnet/core/
- **ASP.NET MVC**: https://www.asp.net/mvc
- **ASP.NET Web API**: https://www.asp.net/web-api
- **Blazor**: https://dotnet.microsoft.com/apps/aspnet/web-apps/blazor
- **.NET Foundation**: https://dotnetfoundation.org/

## License

This project is licensed under the Apache License 2.0 - see the [LICENSE.txt](LICENSE.txt) file for details.

## Support

For questions and issues:
- Review sample-specific README files for detailed instructions
- Check the [official ASP.NET documentation](https://docs.microsoft.com/aspnet/)
- Visit [Stack Overflow](https://stackoverflow.com/questions/tagged/asp.net) with the appropriate tags
- Report issues in this repository's issue tracker
