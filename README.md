# Total Black

[![Visual Studio](https://img.shields.io/badge/Visual%20Studio-2022%20%7C%202026-5C2D91.svg)](https://visualstudio.microsoft.com/)
[![Architecture](https://img.shields.io/badge/Arch-x64%20%7C%20ARM64-blue.svg)](https://visualstudio.microsoft.com/)
[![CI](https://github.com/mykolakushch/TotalBlack/actions/workflows/ci.yml/badge.svg)](https://github.com/mykolakushch/TotalBlack/actions/workflows/ci.yml)
[![Visual Studio Marketplace](https://img.shields.io/visual-studio-marketplace/v/mnml.totalblacktheme.svg?label=VS%20Marketplace)](https://marketplace.visualstudio.com/items?itemName=mnml.totalblacktheme)

**Total Black** is a pure OLED `#000000` theme for **Visual Studio 2022** and **Visual Studio 2026**. It replaces standard dark-gray IDE surfaces with true black backgrounds while preserving high-contrast syntax highlighting and readable UI controls across editors, tool windows, and dialogs.

<a href="https://www.buymeacoffee.com/nkusch" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png" alt="Buy Me A Coffee" style="height: 60px !important;width: 217px !important;" ></a>

## Contents

- [Screenshots](#screenshots) · [Compatibility](#compatibility) · [Features](#features) · [Installation](#installation) · [Building from source](#building-from-source) · [Releasing (maintainers)](#releasing-maintainers)

---

## Screenshots

![Total Black Editor](https://mnml.gallerycdn.vsassets.io/extensions/mnml/totalblacktheme/1.0/1687750409591/Screenshot_2023-06-26_061910.png)

![Total Black UI](https://mnml.gallerycdn.vsassets.io/extensions/mnml/totalblacktheme/1.0/1687750409591/Screenshot_2023-06-26_062012.png)

## Compatibility

| Target | Supported versions | Architectures |
|---|---|---|
| Visual Studio 2022 | `17.0+` | `x64`, `ARM64` |
| Visual Studio 2026 | `18.0+` | `x64`, `ARM64` |

## Features

- **Pure OLED `#000000` surfaces** across the code editor, tool windows, dialogs, Output/Command/Find Results windows, and designers.
- **High-contrast readability** with calibrated foreground/background pairs for selections, hover states, diagnostics, and interactive controls.
- **Zero-gray consistency** eliminating leftover `#1E1E1E` / `#252526` / `#2D2D30` backgrounds from the default Dark theme.

## Installation

### Visual Studio Marketplace

1. Open **Visual Studio** -> **Extensions** -> **Manage Extensions**.
2. Search for **Total Black** (`mnml.totalblacktheme`) and click **Download**.
3. Restart Visual Studio to complete installation.
4. Activate the theme via **Tools** -> **Theme** -> **Total Black**.

### GitHub Releases

1. Download `TotalBlack.vsix` from [Releases](https://github.com/mykolakushch/TotalBlack/releases).
2. Double-click the `.vsix` file to install it into Visual Studio.

## Building from source

Requires Visual Studio 2022/2026 or MSBuild with the .NET Framework 4.7.2 targeting pack.

```powershell
msbuild TotalBlack.sln /t:Restore,Build /p:Configuration=Release
```

The compiled extension package is written to `TotalBlack\bin\Release\TotalBlack.vsix`.

## Releasing (maintainers)

Pushing to `master` runs the [CI workflow](.github/workflows/ci.yml), which builds `TotalBlack.sln` in `Release` and uploads `TotalBlack.vsix` as a build artifact.

Releases are triggered by version tags:

1. Ensure `master` has a green CI build.
2. Create and push a semver tag:
   ```sh
   git tag v1.1.0
   git push origin v1.1.0
   ```
3. The [Release & Publish workflow](.github/workflows/release.yml) updates `Version` in `TotalBlack/source.extension.vsixmanifest` from the tag, builds `TotalBlack.vsix`, creates a GitHub Release with generated release notes, and publishes to the Visual Studio Marketplace via Trusted Publishing (OIDC).
