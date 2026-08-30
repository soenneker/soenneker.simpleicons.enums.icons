[![](https://img.shields.io/nuget/v/soenneker.simpleicons.enums.icons.svg?style=for-the-badge)](https://www.nuget.org/packages/soenneker.simpleicons.enums.icons/)
[![](https://img.shields.io/github/actions/workflow/status/soenneker/soenneker.simpleicons.enums.icons/publish-package.yml?style=for-the-badge)](https://github.com/soenneker/soenneker.simpleicons.enums.icons/actions/workflows/publish-package.yml)
[![](https://img.shields.io/nuget/dt/soenneker.simpleicons.enums.icons.svg?style=for-the-badge)](https://www.nuget.org/packages/soenneker.simpleicons.enums.icons/)
[![](https://img.shields.io/github/actions/workflow/status/soenneker/soenneker.simpleicons.enums.icons/codeql.yml?label=CodeQL&style=for-the-badge)](https://github.com/soenneker/soenneker.simpleicons.enums.icons/actions/workflows/codeql.yml)

# Soenneker.SimpleIcons.Enums.Icons

A generated `SimpleIconEnum` containing the icon names available from Simple Icons.

## Installation

```bash
dotnet add package Soenneker.SimpleIcons.Enums.Icons
```

## Usage

```csharp
using Soenneker.SimpleIcons.Enums.Icons;

SimpleIconEnum icon = SimpleIconEnum.Github;

string name = icon.ToString(); // "Github"
```

Use this package when an API should accept a known Simple Icons name instead of an arbitrary string. The enum contains names only; it does not include SVG markup, brand colors, titles, or lookup methods. Use `Soenneker.SimpleIcons.Icons` when the SVG data is required.

Names that cannot begin with a C# letter are prefixed with `Icon`, and punctuation is converted into identifier-safe words. Because this enum follows the upstream catalog, members can be added or removed as Simple Icons changes; persist the upstream slug rather than the numeric enum value.
