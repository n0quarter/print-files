# print-files

A simple CLI tool to list and print files with smart filtering.

## Usage

```bash
# List all files (excluding defaults)
pf

# List directories only
pf -d

# Print file contents
pf -p

# Exclude additional patterns
pf -i "*.log,temp"

# Multiple options
pf -d -i "build,cache"
pf -p -i "**/*.test.js"
```

## Options

- `-d, --dirs` - List directories only
- `-p, --print` - Print file contents
- `-i, --ignore` - Add ignore patterns (comma-separated)
- `-h, --help` - Show help

## Ignore Patterns

Supports glob patterns:
- `*.log` - all .log files
- `build` - build directory
- `**/*.test.js` - test files anywhere
- `assets/builds` - specific path

## Install

```bash
npm install -g print-files
```

## Default Ignores

`node_modules`, `tmp`, `.git`, `.github`, `.idea`, `.vscode`, `.DS_Store`, `package-lock.json`, `public`, `dist`, `.env`
