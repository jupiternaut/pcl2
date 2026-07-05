# Plain Craft Launcher 2

Plain Craft Launcher 2 is a Windows desktop Minecraft launcher codebase. This repository contains a Visual Basic .NET WPF solution for the launcher.

## Current Status

- Status: source snapshot for the desktop launcher.
- Branch: `main`.
- Solution: `Plain Craft Launcher 2.sln`.
- Project: `Plain Craft Launcher 2/Plain Craft Launcher 2.vbproj`.
- Target framework: .NET Framework 4.6.2.
- Platform: Windows desktop.

The active branch for this repository is `main`, not `master`. The project is not a cross-platform .NET project and is not expected to build with `dotnet build` on macOS or Linux.

## Dependencies

- Windows 10 or Windows 11.
- Visual Studio 2022 with the .NET desktop development workload.
- .NET Framework 4.6.2 Developer Pack or targeting pack.
- Git configured to fetch the full repository contents.

The project references standard .NET Framework desktop assemblies and local DLL references from the project tree. Use a full clone when building; sparse or partial clones are only suitable for documentation inspection.

## Build From a Fresh Clone

```powershell
git clone https://github.com/jupiternaut/pcl2.git
cd pcl2
```

Build with Visual Studio:

1. Open `Plain Craft Launcher 2.sln`.
2. Select `Debug|Any CPU` or `Release|Any CPU`.
3. Build the solution.

Build with MSBuild from a Visual Studio Developer PowerShell:

```powershell
msbuild "Plain Craft Launcher 2.sln" /p:Configuration=Debug /p:Platform="Any CPU"
```

Other solution configurations include `Beta`, `Release`, and `ReleaseUpdate`.

## Run

After a successful build, run the generated desktop executable from the project's output directory. The project file sets the output path to `Plain Craft Launcher 2/bin/`.

## Test

No automated test project is declared in this solution. For a basic verification pass:

1. Build the solution in Visual Studio.
2. Start the generated desktop executable.
3. Confirm the launcher opens on Windows.
4. Manually verify any Minecraft account, download, or launch workflows that are relevant to the change being reviewed.

## UI and Data Boundaries

- This is a Windows WPF desktop application.
- Runtime behavior can depend on Minecraft services, launcher network access, local files, and user configuration.
- The repository should be treated as a source snapshot, not as a guaranteed live mirror of every upstream release.
- Release packaging, signing, and update distribution are outside the basic build instructions above.

## Screenshots

No screenshot is currently checked in. Suggested placeholder path for future documentation:

```text
docs/screenshots/plain-craft-launcher-2-main-window.png
```

## Issues and Contributions

Use GitHub Issues for build problems, missing Windows setup details, or documentation gaps. Pull requests should keep changes scoped and should be tested on Windows with Visual Studio when they affect the desktop application.
