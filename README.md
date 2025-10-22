# ASP.NET and ASP.NET Core Samples

This repository contains a collection of code samples demonstrating various features and capabilities of ASP.NET and ASP.NET Core frameworks. These samples are designed to help developers learn and understand how to implement specific features, patterns, and best practices in their web applications.

## What's in this Repository

This repository showcases sample applications and code snippets for:

- **ASP.NET (Framework)**: Traditional ASP.NET applications including MVC, Web API, Identity, Katana (OWIN), and HttpClient examples
- **ASP.NET Core**: Modern cross-platform ASP.NET Core applications including Blazor, MVC, and Security samples

Each sample is self-contained and focuses on demonstrating a specific feature or scenario, making it easy to understand and integrate into your own projects.

## Repository Structure

```
samples/
├── aspnet/              # ASP.NET Framework samples
│   ├── HttpClient/      # HttpClient usage examples
│   ├── Identity/        # ASP.NET Identity samples
│   ├── Katana/          # OWIN/Katana middleware samples
│   ├── MVC/             # ASP.NET MVC samples
│   └── WebApi/          # ASP.NET Web API samples
│
└── aspnetcore/          # ASP.NET Core samples
    ├── blazor/          # Blazor component samples
    ├── mvc/             # ASP.NET Core MVC samples
    └── security/        # Security-related samples
```

For detailed information about each category:
- ASP.NET samples documentation: [samples/aspnet/README.md](samples/aspnet/README.md)
- Additional resources at [https://www.asp.net](https://www.asp.net)

## Prerequisites

Before running these samples, ensure you have the following installed:

### For ASP.NET Core Samples:
- **.NET SDK** (version 5.0 or later, some samples may require .NET 6.0+)
  - Download from [https://dotnet.microsoft.com/download](https://dotnet.microsoft.com/download)
  - Verify installation: `dotnet --version`

### For ASP.NET Framework Samples:
- **Visual Studio 2017 or later** (Windows only)
  - Download from [https://visualstudio.microsoft.com/](https://visualstudio.microsoft.com/)
- **.NET Framework 4.5 or later**

### Optional Tools:
- **Node.js and npm** (for Blazor samples with JavaScript integration)
  - Download from [https://nodejs.org/](https://nodejs.org/)
- **Git** for cloning the repository
  - Download from [https://git-scm.com/](https://git-scm.com/)

## Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/dotnet/samples.git
cd samples
```

### 2. Navigate to a Sample

Choose a sample you want to run. For example, to run a Blazor sample:

```bash
cd samples/aspnetcore/blazor/BinarySubmit
```

### 3. Run the Sample

#### For ASP.NET Core Samples:

```bash
# Restore dependencies and run the application
dotnet run
```

The application will start and display the URL where it's running (typically `https://localhost:5001` or `http://localhost:5000`).

#### For ASP.NET Core Samples with Watch Mode (auto-reload):

```bash
# Run with hot reload enabled
dotnet watch run
```

#### For ASP.NET Framework Samples:

1. Open the `.sln` file in Visual Studio
2. Press F5 to build and run the application

### 4. Running Specific Sample Types

#### Blazor Samples:

```bash
cd samples/aspnetcore/blazor/FlightFinder
dotnet run --project FlightFinder.Server
```

Then open your browser to the displayed URL (usually `https://localhost:5001`).

#### MVC Samples:

```bash
cd samples/aspnetcore/mvc/produces
dotnet run
```

#### Samples with JavaScript Integration:

Some samples (like JSComponentGeneration) require running both the .NET backend and JavaScript frontend:

```bash
# Terminal 1 - Run the .NET application
cd samples/aspnetcore/blazor/JSComponentGeneration/BlazorAppGeneratingJSComponents
dotnet watch

# Terminal 2 - Run the JavaScript app
cd samples/aspnetcore/blazor/JSComponentGeneration/angular-app-with-blazor
npm install
npm start
```

## Building All Samples

To build all samples in a directory:

```bash
# Build all ASP.NET Core samples
cd samples/aspnetcore
dotnet build

# Build a specific category
cd samples/aspnetcore/blazor
dotnet build
```

## Exploring the Samples

Each sample includes its own README or documentation file that explains:
- What the sample demonstrates
- Specific setup instructions
- Key concepts and implementation details
- Related documentation links

Look for `README.md` or `ReadMe.txt` files in each sample directory.

## Common Issues and Troubleshooting

### Port Already in Use
If you get an error that a port is already in use, you can specify a different port:

```bash
dotnet run --urls "https://localhost:5002;http://localhost:5003"
```

### Missing SDK Version
Some samples may require a specific .NET SDK version. Check the `global.json` file in the sample directory. You can:
- Install the required SDK version, or
- Remove/modify the `global.json` file to use your installed SDK version

### Build Errors
If you encounter build errors:

```bash
# Clean and restore the project
dotnet clean
dotnet restore
dotnet build
```

## Contributing

We welcome contributions! If you'd like to add a new sample or improve an existing one:

1. Fork this repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

Please ensure your samples:
- Follow the existing structure and naming conventions
- Include a README explaining what the sample demonstrates
- Are well-documented with code comments
- Follow .NET coding standards

## Additional Resources

- **ASP.NET Documentation**: [https://docs.microsoft.com/aspnet/core/](https://docs.microsoft.com/aspnet/core/)
- **ASP.NET Community**: [https://dotnet.microsoft.com/platform/community](https://dotnet.microsoft.com/platform/community)
- **ASP.NET Source Code**: [https://github.com/dotnet/aspnetcore](https://github.com/dotnet/aspnetcore)
- **Report Issues**: [https://github.com/dotnet/samples/issues](https://github.com/dotnet/samples/issues)

## Code of Conduct

This project has adopted the [.NET Foundation Code of Conduct](CODE-OF-CONDUCT.md). For more information, see the Code of Conduct FAQ or contact opencode@microsoft.com with any additional questions or comments.

## License

This project is licensed under the Apache License 2.0 - see the [LICENSE.txt](LICENSE.txt) file for details.
