# Total Black

[![Visual Studio](https://img.shields.io/badge/Visual%20Studio-2022%20%7C%202026-5C2D91.svg)](https://visualstudio.microsoft.com/)
[![Architecture](https://img.shields.io/badge/Arch-x64%20%7C%20ARM64-blue.svg)](https://visualstudio.microsoft.com/)
[![CI](https://github.com/mykolakushch/TotalBlack/actions/workflows/ci.yml/badge.svg)](https://github.com/mykolakushch/TotalBlack/actions/workflows/ci.yml)
[![Visual Studio Marketplace](https://img.shields.io/visual-studio-marketplace/v/mnml.totalblacktheme.svg?label=VS%20Marketplace)](https://marketplace.visualstudio.com/items?itemName=mnml.totalblacktheme)
[![GitHub release](https://img.shields.io/github/v/release/mykolakushch/TotalBlack.svg?label=Release)](https://github.com/mykolakushch/TotalBlack/releases)

**Total Black** is a pure OLED `#000000` theme for **Visual Studio 2022** and **Visual Studio 2026**. It replaces standard dark-gray IDE surfaces with true black backgrounds while preserving high-contrast syntax highlighting, clear separation borders, and readable UI controls across editors, tool windows, and dialogs.

<a href="https://www.buymeacoffee.com/nkusch" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png" alt="Buy Me A Coffee" style="height: 60px !important;width: 217px !important;" ></a>

## Contents

- [Screenshots](#screenshots)
- [Compatibility](#compatibility)
- [Features](#features)
- [Installation](#installation)
- [Visual Studio 2026 Configuration](#visual-studio-2026-configuration)
- [Building from Source](#building-from-source)

---

## Screenshots

![Total Black Editor](https://mnml.gallerycdn.vsassets.io/extensions/mnml/totalblacktheme/1.0/1687750409591/Screenshot_2023-06-26_061910.png)

![Total Black UI](https://mnml.gallerycdn.vsassets.io/extensions/mnml/totalblacktheme/1.0/1687750409591/Screenshot_2023-06-26_062012.png)

## Compatibility

| Target | Supported Versions | Architectures |
|---|---|---|
| Visual Studio 2022 | `17.0+` | `x64`, `ARM64` |
| Visual Studio 2026 | `18.0+` | `x64`, `ARM64` |

## Features

- **Pure OLED `#000000` surfaces** across the code editor, document tabs, toolbars, status bar, tool windows, and dialogs.
- **Zero-gray consistency** eliminating leftover `#1E1E1E` / `#252526` / `#2D2D30` backgrounds from the default Dark theme.
- **Subtle dark borders** (`#222222` / `#1C1C1C`) for clean division between panels and tabs without breaking the OLED look.
- **High-contrast readability** with crisp text, preserved syntax classification, and visible interactive controls.
- **Modern VS 2026 Fluent UI support** including full coverage for Shell, ShellInternal, EditorOverride, AI, Chat, and Copilot UI components.

## Installation

### Visual Studio Marketplace

1. Open **Visual Studio** -> **Extensions** -> **Manage Extensions**.
2. Search for **Total Black** (`mnml.totalblacktheme`) and click **Download**.
3. Restart Visual Studio to complete installation.
4. Activate the theme via **Tools** -> **Theme** -> **Total Black**.

### GitHub Releases

1. Download the latest `TotalBlack.vsix` from [Releases](https://github.com/mykolakushch/TotalBlack/releases).
2. Double-click the `.vsix` file to install it into Visual Studio.
3. Restart Visual Studio and activate via **Tools** -> **Theme** -> **Total Black**.

## Visual Studio 2026 Configuration

Visual Studio 2026 introduces an independent **Editor Appearance** setting that can override theme editor colors:

1. Open **Tools** -> **Options**.
2. Navigate to **Environment** -> **Visual Experience**.
3. Ensure **Editor Appearance** is set to **Match theme**.

> [!TIP]
> Setting **Editor Appearance** to **Match theme** allows the code editor canvas, navigation bar, and editor margins to inherit the pure black `#000000` palette of Total Black instead of the built-in Dark gray override.

## Building from Source

Requires Visual Studio 2022/2026 or MSBuild with the .NET Framework 4.7.2 targeting pack.

```powershell
msbuild TotalBlack.sln /t:Restore,Build /p:Configuration=Release
```

The compiled extension package is written to `TotalBlack\bin\Release\TotalBlack.vsix`.
