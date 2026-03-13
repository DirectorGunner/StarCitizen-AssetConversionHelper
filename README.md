# Star Citizen Asset Conversion Helper Script

> [!IMPORTANT]
> This project is **not official**. It is **not affiliated with CIG, RSI, or MarkEmp**.  
> It is just a **community-made helper script** for using [MarkEmp's Cryengine-Converter](https://github.com/Markemp/Cryengine-Converter/releases/) with extracted **Star Citizen** `Data.p4k` contents. You can use [Dolkensp's Dataforge tools](https://github.com/dolkensp/unp4k/releases) to unpack the Data.p4k file. Or use the Janky tutorial in the [Star Citizen Modding Community Discord](https://discord.gg/EQ3Z6x6hUP)

> [!NOTE]
> This repo is focused on helping automate large conversion runs after you have already extracted the game's `Data.p4k`.

---

## What this is

This repo contains a PowerShell helper script for automating batch conversion workflows with **MarkEmp's Cryengine-Converter** against extracted **Star Citizen** data.

It is intended to help with workflows like:

- converting entire builds including all `.cga`, `.cgf`, `.chr`, and `.skin` files
- preserving the relative folder structure from the extracted `Data` directory
- tracking progress, logs, and conversion state for large runs
- skipping files that were already converted

---

## What this is not

- Not an official Star Citizen tool
- Not an official Cryengine-Converter frontend
- Not a `Data.p4k` extractor
- Not a polished commercial-grade application
- Not guaranteed to be pretty code, infact probably quite ugly

---

## Repo description

Just a helper script for using MarkEmp's Cryengine-Converter with Star Citizen `Data.p4k` files.

This is in **no way, shape, or form** anything official, just something made by community.

And apologies ahead of time for the **vibe coding**. I have a hard enough time with my primary language, let alone learning new languages like coding right.

Help is welcome.

---

## Requirements

Before using this script, you should already have:

- a working copy of **MarkEmp's Cryengine-Converter**
- a correctly extracted Star Citizen `Data.p4k` file
- PowerShell available on Windows
- a folder structure similar to the one shown below

### The script expects:

- a `Data` folder in the same directory as the script
- the converter `.exe` in the same directory as the script
- **MarkEmp's Cryengine-Converter v2.0.0 or newer**
- output to be written into a `USD` folder
- logs to be written into a `Logs` folder

---

## What the script does

Depending on the current version in this repo, the script may include features such as:

- automatic detection of the newest `cgf-converter*.exe`
- recursive scanning of supported file types
- cache-aware manifest loading
- skip checks for already converted outputs
- structured logging
- progress reporting in PowerShell
- safer handling of large conversion runs
- preservation of relative paths from `Data`

## Usage

Run the script from PowerShell:

```powershell
Set-ExecutionPolicy -Scope Process Bypass
& ".\convert.ps1"
```
or you can use the included cmd file to launch the script


