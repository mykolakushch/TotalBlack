# Total Black

A pure OLED `#000000` black theme for **Visual Studio 2022** and **Visual Studio 2026** (`x64` & `ARM64`).

<a href="https://www.buymeacoffee.com/nkusch" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png" alt="Buy Me A Coffee" style="height: 60px !important;width: 217px !important;" ></a>

## Screenshots

![Total Black Editor](https://mnml.gallerycdn.vsassets.io/extensions/mnml/totalblacktheme/1.0/1687750409591/Screenshot_2023-06-26_061910.png)

![Total Black UI](https://mnml.gallerycdn.vsassets.io/extensions/mnml/totalblacktheme/1.0/1687750409591/Screenshot_2023-06-26_062012.png)

## Features

- True `#000000` OLED-friendly background across editor, tool windows, dialogs, and panels.
- High-contrast, readable syntax highlighting and UI controls.
- Supports Visual Studio 2022 (`17.0+`) and Visual Studio 2026 (`18.0+`) on both `x64` and `ARM64`.

## Installation

### Visual Studio Marketplace
1. Open **Visual Studio** -> **Extensions** -> **Manage Extensions**.
2. Search for **Total Black** and click **Download**.
3. Restart Visual Studio to complete installation.
4. Select the theme via **Tools** -> **Theme** -> **Total Black**.

### GitHub Releases
1. Download the latest `TotalBlack.vsix` from [Releases](https://github.com/mykolakushch/TotalBlack/releases).
2. Double-click the `.vsix` file to install it into Visual Studio.

## Building from Source

Requirements: Visual Studio 2022/2026 or MSBuild with .NET Framework 4.7.2 targeting pack.

```powershell
msbuild TotalBlack.sln /t:Restore,Build /p:Configuration=Release
```

The compiled extension package will be output to `TotalBlack\bin\Release\TotalBlack.vsix`.
