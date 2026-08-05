# LogHarvester v2 - Log Analyzer

Fast Windows x64 CLI tool that extracts ERROR, WARNING, and CRITICAL events from log files and exports them as CSV/JSON.

## Quick Start

### 1. Compile
```cmd
build.bat
```
(Auto-finds Visual Studio 2019+)

### 2. Run
```cmd
logharvester.exe test_logs
```

### 3. Check Output
- `LogHarvester_test_logs.csv` - Events in CSV format
- `LogHarvester_test_logs.json` - Events in JSON format

## Usage

```cmd
logharvester.exe <input_directory>
```

## What It Does

- Scans all subdirectories recursively
- Finds `.log` and `.txt` files
- Extracts lines with ERROR, WARNING, CRITICAL
- Creates CSV and JSON output files
- Automatically names output by directory

## Supported Formats

Ejemplos de líneas que se detectan:

```text
[2024-01-15 10:30:45] ERROR: Connection failed
2024-01-15 10:30:45 - ERROR - Database error
Any line containing ERROR / WARNING / CRITICAL
```

## Files Included

- `logharvester.c` — Full C source code  
- `build.bat` — Windows compilation script  
- `test_logs/` — Example log files for testing  
- `README.md` — This file

## System Requirements

- Windows 10 o Windows 11 (x64)  
- Visual Studio 2019 o 2022  
- ~5 MB de espacio libre (sin incluir logs)

## License

This project is available under the MIT License — see LICENSE for details.
