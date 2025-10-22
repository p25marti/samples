# ASP.NET and ASP.NET Core Samples

This repository contains a collection of sample applications demonstrating various features and capabilities of ASP.NET and ASP.NET Core frameworks. These samples are provided by the .NET Foundation to help developers learn and understand different aspects of web development with ASP.NET technologies.

## Table of Contents

- [Overview](#overview)
- [Prerequisites](#prerequisites)
- [Getting Started](#getting-started)
- [Repository Structure](#repository-structure)
- [Running the Samples](#running-the-samples)
- [Sample Categories](#sample-categories)
- [Contributing](#contributing)
- [License](#license)

## Overview

This repository provides practical, real-world examples covering:

- **ASP.NET MVC**: Model-View-Controller pattern implementations
- **ASP.NET Web API**: RESTful API development
- **ASP.NET Core MVC**: Modern MVC applications on ASP.NET Core
- **ASP.NET Core Blazor**: WebAssembly and Server-side Blazor applications
- **ASP.NET Identity**: Authentication and authorization samples
- **OWIN/Katana**: OWIN middleware and self-hosting samples

## Prerequisites

To run these samples, you'll need the following installed on your machine:

### For ASP.NET Samples

- **Visual Studio 2019 or later** (Community, Professional, or Enterprise)
  - Download: https://visualstudio.microsoft.com/downloads/
- **.NET Framework 4.5 or later**
  - Typically included with Visual Studio
- **IIS Express** (included with Visual Studio)

### For ASP.NET Core Samples

- **.NET SDK** (version varies by sample, typically .NET Core 2.2, 3.0, 3.1, .NET 5.0, or .NET 6.0)
  - Download: https://dotnet.microsoft.com/download
  - Check installed versions: `dotnet --list-sdks`
- **Visual Studio 2019/2022** or **Visual Studio Code**
  - VS Code download: https://code.visualstudio.com/
  - C# extension for VS Code: https://marketplace.visualstudio.com/items?itemName=ms-dotnettools.csharp

### Optional Tools

- **SQL Server LocalDB** (for samples using databases)
  - Included with Visual Studio
- **Node.js and npm** (for samples with JavaScript/TypeScript components)
  - Download: https://nodejs.org/

## Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/aspnet/samples.git
cd samples
```

### 2. Verify Prerequisites

Check that you have the required .NET SDK versions installed:

```bash
# Check .NET SDK versions
dotnet --list-sdks

# Check .NET Runtime versions
dotnet --list-runtimes
```

### 3. Choose a Sample

Browse the samples directory to find a sample that interests you:

- **ASP.NET samples**: [samples/aspnet](samples/aspnet)
- **ASP.NET Core samples**: [samples/aspnetcore](samples/aspnetcore)

## Repository Structure

```
samples/
├── aspnet/                    # ASP.NET Framework samples
│   ├── HttpClient/           # HttpClient usage examples
│   ├── Identity/             # ASP.NET Identity samples
│   ├── Katana/               # OWIN/Katana middleware samples
│   ├── MVC/                  # ASP.NET MVC samples
│   └── WebApi/               # ASP.NET Web API samples
└── aspnetcore/               # ASP.NET Core samples
    ├── blazor/               # Blazor samples (WebAssembly & Server)
    ├── mvc/                  # ASP.NET Core MVC samples
    └── security/             # Security-related samples
```

## Running the Samples

### Running ASP.NET Core Samples

1. **Navigate to the sample directory:**

```bash
cd samples/aspnetcore/[category]/[sample-name]
```

2. **Restore dependencies:**

```bash
dotnet restore
```

3. **Build the project:**

```bash
dotnet build
```

4. **Run the application:**

```bash
dotnet run
```

The application will start and display the URL (typically `https://localhost:5001` or `http://localhost:5000`). Open this URL in your browser.

**Example:**

```bash
cd samples/aspnetcore/mvc/domain
dotnet restore
dotnet build
cd src/MvcSample
dotnet run
```

### Running ASP.NET Samples

1. **Navigate to the sample directory:**

```bash
cd samples/aspnet/[category]/[sample-name]
```

2. **Open the solution in Visual Studio:**

```bash
# Open the .sln file with Visual Studio
# Or from command line (if VS is in PATH):
start [SampleName].sln
```

3. **Restore NuGet packages:**
   - Visual Studio will automatically restore packages on solution open
   - Or manually: Right-click solution → Restore NuGet Packages

4. **Build and run:**
   - Press `F5` to build and run with debugging
   - Or press `Ctrl+F5` to run without debugging

### Using Visual Studio Code

1. **Open the sample folder:**

```bash
code samples/aspnetcore/[category]/[sample-name]
```

2. **Restore and run:**

Press `F5` to start debugging, or use the integrated terminal:

```bash
dotnet restore
dotnet run
```

## Sample Categories

### ASP.NET Core Samples

#### Blazor Samples
- **BinarySubmit**: Binary form submission in Blazor
- **FlightFinder**: Complete flight booking application
- **InputLargeTextArea**: Handling large text inputs
- **JSComponentGeneration**: Generating JavaScript components
- **Validation**: Form validation patterns

#### MVC Samples
- **Domain Routing**: Custom routing based on domain names
- **Produces**: Content negotiation with ProducesAttribute
- **RenderViewToString**: Server-side view rendering
- **RuntimeCompilation**: Runtime Razor compilation
- **Testing**: Unit testing MVC applications

#### Security Samples
- **KestrelHttps**: HTTPS configuration with Kestrel

### ASP.NET Samples

#### Identity Samples
- MySQL Integration
- Custom Membership Implementation
- Password Policy Configuration
- OAuth and OWIN Integration
- Universal Providers Migration

#### Web API Samples
- Action Results
- Authentication (Basic, Certificate)
- Batch Operations
- Custom Formatters and Model Binders
- Entity Framework Integration
- File Upload
- Routing and Constraints

#### MVC Samples
- Attribute Routing
- Authentication
- Enum Support

#### Katana/OWIN Samples
- Custom Servers
- Pipeline Branching
- Self-hosting
- SignalR Integration
- WebSocket Support

## Contributing

We welcome contributions! Please see our [Code of Conduct](CODE-OF-CONDUCT.md) before contributing.

To contribute:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-sample`)
3. Commit your changes (`git commit -m 'Add amazing sample'`)
4. Push to the branch (`git push origin feature/amazing-sample`)
5. Open a Pull Request

## Additional Resources

- **ASP.NET Documentation**: https://docs.microsoft.com/aspnet/
- **ASP.NET Core Documentation**: https://docs.microsoft.com/aspnet/core/
- **ASP.NET Web Stack Source**: https://github.com/aspnet/aspnetwebstack
- **ASP.NET Forums**: https://forums.asp.net/
- **.NET Foundation**: https://dotnetfoundation.org/

## Troubleshooting

### Common Issues

**Problem**: `dotnet` command not found
- **Solution**: Ensure .NET SDK is installed and added to your PATH

**Problem**: SDK version mismatch
- **Solution**: Install the required SDK version or update the `<TargetFramework>` in the .csproj file

**Problem**: Port already in use
- **Solution**: Change the port in `Properties/launchSettings.json` or stop the application using the port

**Problem**: NuGet restore fails
- **Solution**: Clear NuGet cache: `dotnet nuget locals all --clear`

### Getting Help

- Check the README in individual sample directories for sample-specific instructions
- Open an issue in this repository for bugs or questions
- Visit [Stack Overflow](https://stackoverflow.com/questions/tagged/asp.net) for community support

## License

Copyright © .NET Foundation. All rights reserved.

Licensed under the Apache License, Version 2.0. See [LICENSE.txt](LICENSE.txt) for more information.
