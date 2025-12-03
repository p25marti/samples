# Samples

Samples for ASP.NET and ASP.NET Core.

ASP.NET samples are under the [samples/aspnet](samples/aspnet) directory.

ASP.NET Core samples are under the [samples/aspnetcore](samples/aspnetcore) directory.

TEST TO SEE IF THE DEPLOY WORKED

## Formatting Standards

### package.json Files

All `package.json` files in this repository follow these formatting standards:

1. **Indentation**: Use tabs instead of spaces
2. **Scripts Section**: All keys in the `scripts` section are sorted alphabetically
3. **JSON Validity**: All files are validated as proper JSON

### Editor Configuration

This repository includes `.editorconfig` and `.prettierrc` files to enforce consistent formatting:

- JSON files use tab indentation
- Tab width is set to 4 spaces for display purposes
- End of line is set to LF (Unix-style)

### Tools

To ensure your changes comply with these standards:

1. **EditorConfig**: Most modern editors support [EditorConfig](https://editorconfig.org/) automatically
2. **Prettier**: If using Prettier, the `.prettierrc` configuration will enforce tab usage

### Validation

Before committing changes to `package.json` files, ensure:
- The file uses tab indentation (not spaces)
- The `scripts` section has keys in alphabetical order
- The file is valid JSON (test with `node -e "require('./package.json')"` or similar)
