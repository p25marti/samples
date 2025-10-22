# ASP.NET and ASP.NET Core Samples

This repository contains a collection of samples and examples for ASP.NET and ASP.NET Core. These samples demonstrate various features, patterns, and best practices for building web applications and APIs using Microsoft's ASP.NET technologies.

## What's in this Repository

This repository provides practical, runnable examples covering:

- **ASP.NET Core**: Modern cross-platform web framework
  - Blazor components and applications
  - MVC (Model-View-Controller) patterns
  - Security implementations
  - And more...

- **ASP.NET (Classic)**: Full .NET Framework web applications
  - Web API samples
  - MVC samples
  - Identity and authentication examples
  - HttpClient usage patterns
  - Katana/OWIN middleware

### Directory Structure

- **[samples/aspnet](samples/aspnet)** - ASP.NET samples for the full .NET Framework
- **[samples/aspnetcore](samples/aspnetcore)** - ASP.NET Core samples for cross-platform development

## Prerequisites

To run the samples in this repository, you'll need:

### For ASP.NET Core Samples

- [.NET SDK](https://dotnet.microsoft.com/download) (version depends on the sample - typically .NET Core 2.2, 3.1, .NET 5.0 or later)
- A code editor:
  - [Visual Studio 2019/2022](https://visualstudio.microsoft.com/) (Windows/Mac)
  - [Visual Studio Code](https://code.visualstudio.com/) (Cross-platform)
  - [JetBrains Rider](https://www.jetbrains.com/rider/) (Cross-platform)

### For ASP.NET (Classic) Samples

- [Visual Studio](https://visualstudio.microsoft.com/) (Windows)
- .NET Framework 4.5 or later
- Windows operating system

## Getting Started

### Running ASP.NET Core Samples

1. **Clone the repository**:
   ```bash
   git clone https://github.com/dotnet/samples.git
   cd samples
   ```

2. **Navigate to a sample directory**:
   ```bash
   cd samples/aspnetcore/<category>/<sample-name>
   ```
   For example:
   ```bash
   cd samples/aspnetcore/blazor/BinarySubmit
   ```

3. **Restore dependencies and build**:
   ```bash
   dotnet restore
   dotnet build
   ```

4. **Run the sample**:
   ```bash
   dotnet run
   ```

5. **Access the application**:
   - Open your browser and navigate to the URL displayed in the console (typically `http://localhost:5000` or `https://localhost:5001`)

### Running ASP.NET (Classic) Samples

1. **Clone the repository** (if not already done):
   ```bash
   git clone https://github.com/dotnet/samples.git
   cd samples
   ```

2. **Navigate to a sample directory**:
   ```bash
   cd samples/aspnet/<category>/<sample-name>
   ```

3. **Open the solution in Visual Studio**:
   - Double-click the `.sln` file, or
   - Open Visual Studio and use File → Open → Project/Solution

4. **Restore NuGet packages**:
   - Visual Studio should automatically restore packages
   - Or manually: Right-click solution → Restore NuGet Packages

5. **Build and run**:
   - Press `F5` to build and run with debugging, or
   - Press `Ctrl+F5` to run without debugging

### Using Visual Studio

For any sample with a `.sln` (solution) file:

1. Open the `.sln` file in Visual Studio
2. Restore packages (should happen automatically)
3. Set the appropriate project as the startup project (right-click project → Set as Startup Project)
4. Press `F5` to run

### Using Command Line for Multiple Projects

To build all projects in a solution:
```bash
dotnet build <solution-name>.sln
```

To run a specific project:
```bash
dotnet run --project <path-to-project>/<project-name>.csproj
```

## Sample-Specific Instructions

Each sample may have additional requirements or specific setup instructions. Always check for:
- A `README.md` or `ReadMe.txt` file in the sample's directory
- Configuration files that may need updating (API keys, connection strings, etc.)
- Additional dependencies or prerequisites

## Contributing

We welcome contributions! Please see the [.NET Contributing Guide](https://github.com/dotnet/runtime/blob/main/DOCS/contributing/contributing.md) for more information.

## Code of Conduct

This project has adopted the code of conduct defined by the Contributor Covenant. For more information, see the [Code of Conduct](CODE-OF-CONDUCT.md).

## License

This project is licensed under the Apache License, Version 2.0. See [LICENSE.txt](LICENSE.txt) for details.

## Additional Resources

- [ASP.NET Documentation](https://docs.microsoft.com/aspnet/)
- [ASP.NET Core Documentation](https://docs.microsoft.com/aspnet/core/)
- [.NET Documentation](https://docs.microsoft.com/dotnet/)
- [ASP.NET Forums](https://forums.asp.net/)
- [Stack Overflow - ASP.NET](https://stackoverflow.com/questions/tagged/asp.net)
- [Stack Overflow - ASP.NET Core](https://stackoverflow.com/questions/tagged/asp.net-core)

## Getting Help

- Browse existing samples and their documentation
- Check the [Issues](https://github.com/dotnet/samples/issues) section
- Visit [ASP.NET Community](https://dotnet.microsoft.com/platform/community)
