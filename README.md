# LobotomyWorkBookmarkMod

`refracta_WorkBookmark_MOD` is a companion mod for Lobotomy Corporation.
It is designed to be used together with the original Command Macro mod and adds work bookmark hotkeys.

## Demo

![WorkBookmark Demo](demo.gif)

## Quick Usage

- `Insert`: save current moving/working agent -> abnormality -> work-type pairs.
- `Shift + Insert`: print saved pairs in the system log.
- `Home`: apply saved pairs to dispatchable agents.
- `End`: cancel en-route work actions for saved agents.

## Source

- Core patch logic: `src/refracta_WorkBookmark_MOD/Harmony_Patch.cs`
- Assembly metadata: `src/refracta_WorkBookmark_MOD/AssemblyInfo.cs`
- Project file: `src/refracta_WorkBookmark_MOD/refracta_WorkBookmark_MOD.csproj`
- Mod info XML: `mod/refracta_WorkBookmark_MOD/Info/kr/Info.xml`, `mod/refracta_WorkBookmark_MOD/Info/en/Info.xml`

## Build

### Requirements

- .NET SDK 8+
- PowerShell

### Package

```powershell
./scripts/package_workbookmark.ps1 -Configuration Release
```

### Output

- DLL: `out/Release/refracta_WorkBookmark_MOD/refracta_WorkBookmark_MOD.dll`
- ZIP package: `dist/refracta_WorkBookmark_MOD.zip`

## CI/CD

- Workflow: `.github/workflows/workbookmark-ci.yml`
- Push/PR: build + artifact upload
- Tag push (`workbookmark-v*`, `v*`): automatic GitHub Release with `refracta_WorkBookmark_MOD.zip`
