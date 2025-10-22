# ASP.NET and ASP.NET Core Samples

This repository contains samples and example projects for ASP.NET and ASP.NET Core, demonstrating various features, patterns, and best practices for building web applications and APIs with Microsoft's ASP.NET technologies.

## Table of Contents

- [About This Repository](#about-this-repository)
- [Prerequisites](#prerequisites)
- [Getting Started](#getting-started)
- [Project Structure](#project-structure)
- [Running Samples Locally](#running-samples-locally)
- [Available Samples](#available-samples)
- [Contributing](#contributing)
- [License](#license)

## About This Repository

This repository provides a comprehensive collection of sample applications showcasing:

- **ASP.NET Samples**: Traditional ASP.NET Framework samples including MVC, Web API, HttpClient, Identity, and Katana projects
- **ASP.NET Core Samples**: Modern ASP.NET Core samples including Blazor, MVC, and Security implementations

Each sample demonstrates specific features or scenarios and includes its own documentation with detailed explanations.

## Prerequisites

Before you can run the samples in this repository, ensure you have the following installed:

### For ASP.NET Core Samples

- [.NET SDK](https://dotnet.microsoft.com/download) (version 3.0 or higher)
  - .NET 5.0 for some samples
  - .NET 6.0 for newer samples
- A code editor such as:
  - [Visual Studio 2019/2022](https://visualstudio.microsoft.com/downloads/) (Windows/Mac)
  - [Visual Studio Code](https://code.visualstudio.com/) (Cross-platform)
  - [JetBrains Rider](https://www.jetbrains.com/rider/) (Cross-platform)

### For ASP.NET (Framework) Samples

- [Visual Studio 2017 or later](https://visualstudio.microsoft.com/downloads/) (Windows only)
- .NET Framework 4.0, 4.5, or later (usually included with Visual Studio)
- IIS Express (included with Visual Studio)

### Additional Requirements

Some samples may have additional requirements:
- SQL Server or SQL Server Express (for database samples)
- Node.js (for samples with JavaScript/TypeScript components)
- Specific API keys (documented in individual sample README files)

## Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/aspnet/samples.git
cd samples
```

### 2. Choose a Sample

Browse the available samples in either:
- `samples/aspnet/` - ASP.NET Framework samples
- `samples/aspnetcore/` - ASP.NET Core samples

### 3. Navigate to a Sample Directory

```bash
# For ASP.NET Core samples
cd samples/aspnetcore/blazor/BinarySubmit

# For ASP.NET Framework samples  
cd samples/aspnet/WebApi/ActionResults
```

## Running Samples Locally

### ASP.NET Core Samples

#### Using the .NET CLI

1. Navigate to the sample directory containing a `.csproj` file
2. Restore dependencies:
   ```bash
   dotnet restore
   ```
3. Build the project:
   ```bash
   dotnet build
   ```
4. Run the application:
   ```bash
   dotnet run
   ```
5. Open your browser to the URL shown in the console (typically `https://localhost:5001` or `http://localhost:5000`)

#### Using Visual Studio or Visual Studio Code

1. Open the `.csproj` or `.sln` file
2. Press `F5` or click the "Run" button to start debugging
3. The browser will automatically open to the application

### ASP.NET (Framework) Samples

#### Using Visual Studio

1. Navigate to the sample directory
2. Open the `.sln` (solution) file in Visual Studio
3. Press `F5` or click "Start Debugging" to run the sample
4. IIS Express will start and launch your default browser

#### Building from Command Line

```bash
# Using MSBuild (requires Visual Studio installation)
msbuild SampleProject.sln /p:Configuration=Release

# Or restore NuGet packages first
nuget restore SampleProject.sln
msbuild SampleProject.sln
```

## Project Structure

```
samples/
├── aspnet/                 # ASP.NET Framework samples
│   ├── HttpClient/        # HttpClient usage examples
│   ├── Identity/          # ASP.NET Identity samples
│   ├── Katana/            # OWIN/Katana samples
│   ├── MVC/               # ASP.NET MVC samples
│   └── WebApi/            # ASP.NET Web API samples
│
└── aspnetcore/            # ASP.NET Core samples
    ├── blazor/            # Blazor samples
    ├── mvc/               # ASP.NET Core MVC samples
    └── security/          # Security-related samples
```

## Available Samples

### ASP.NET Core Samples

Located in the `samples/aspnetcore/` directory:

- **Blazor**: Binary file submission, flight finder, form validation, JavaScript component generation
- **MVC**: Domain routing, content negotiation, runtime compilation, view rendering
- **Security**: Authentication and authorization examples

For more information, see the [ASP.NET Core samples README](samples/aspnetcore/README.md) (if available) or browse the directories.

### ASP.NET (Framework) Samples

Located in the `samples/aspnet/` directory:

- **HttpClient**: Bing Translate, Google Maps, Twitter, World Bank API integration examples
- **Identity**: MySQL integration, custom membership, password policies, OAuth samples
- **Katana**: OWIN middleware and authentication samples
- **MVC**: Model-View-Controller pattern implementations
- **Web API**: RESTful API samples, custom formatters, authentication, content negotiation

For complete lists and documentation:
- [ASP.NET MVC samples](http://www.asp.net/mvc/samples)
- [ASP.NET Web API samples](http://www.asp.net/web-api/samples)
- [ASP.NET Web Pages samples](http://www.asp.net/web-pages/samples)

Each sample directory contains its own README or ReadMe.txt with specific instructions and explanations.

## Contributing

This project welcomes contributions and suggestions. Most contributions require you to agree to a Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us the rights to use your contribution.

For more information, see the [.NET Foundation Contributing Guide](https://github.com/dotnet/foundation/blob/master/guidance/contributing.md).

This project has adopted the code of conduct defined by the Contributor Covenant to clarify expected behavior in our community. For more information, see the [.NET Foundation Code of Conduct](https://dotnetfoundation.org/code-of-conduct).

## Additional Resources

- [ASP.NET Documentation](https://docs.microsoft.com/aspnet/)
- [ASP.NET Core Documentation](https://docs.microsoft.com/aspnet/core/)
- [.NET Foundation](https://dotnetfoundation.org/)
- [ASP.NET Community Standup](https://dotnet.microsoft.com/platform/community/standup)

## License

This project is licensed under the Apache License 2.0 - see the [LICENSE.txt](LICENSE.txt) file for details.

Copyright (c) .NET Foundation. All rights reserved.
