# Cursor AI IDE Installer for Linux

This repository contains an automated installation and update script for [Cursor AI IDE](https://cursor.sh/) on Linux systems. The script handles both fresh installations and updates of the Cursor AI IDE AppImage.

## Features

- 🚀 One-command installation and updates
- 🔄 Automatic version management
- 🖥️ Desktop integration with application menu
- 🛠️ Shell integration with convenient `cursor` command
- 📦 Dependency management
- 🔒 Safe update process with running instance detection

## Prerequisites

- Linux operating system
- `curl` (will be automatically installed if missing)
- `sudo` privileges

## Installation

1. Download the installation script:
```bash
curl -O https://raw.githubusercontent.com/your-username/cursor-install-script/main/cursor-install.sh
```

2. Make the script executable:
```bash
chmod +x cursor-install.sh
```

3. Run the script:
```bash
./cursor-install.sh
```

## What the Script Does

1. **Checks Dependencies**: Ensures required tools are installed
2. **Fetches Latest Version**: Queries Cursor's API for the latest stable version
3. **Installs/Updates AppImage**: Downloads and sets up the Cursor AppImage in `/opt/cursor/`
4. **Creates Desktop Entry**: Adds Cursor to your application menu
5. **Shell Integration**: Adds a `cursor` command to your shell configuration
6. **Version Management**: Handles updates when a new version is available

## Usage

After installation, you can launch Cursor AI IDE in two ways:

1. From the application menu (search for "Cursor AI IDE")
2. From the terminal:
   ```bash
   cursor [path]
   ```
   - Running `cursor` without arguments opens Cursor with the current directory
   - Running `cursor path/to/directory` opens Cursor with the specified directory

## Automatic Updates

To check for and install updates, simply run the script again:
```bash
./cursor-install.sh
```

The script will:
- Check your current version against the latest available version
- Update only if a newer version is available
- Prevent updates while Cursor is running to ensure data safety

## File Locations

- AppImage: `/opt/cursor/cursor.AppImage`
- Icon: `/opt/cursor/cursor.png`
- Desktop Entry: `/usr/share/applications/cursor.desktop`
- Shell Function: Added to your shell's RC file (`~/.bashrc` or `~/.zshrc`)

## Troubleshooting

1. **Cursor won't update**: Ensure all Cursor instances are closed before updating
2. **Command not found**: Restart your terminal or run `source ~/.bashrc` (or `~/.zshrc`)
3. **Permission denied**: Ensure the script has execute permissions (`chmod +x`)

## Contributing

Feel free to submit issues and enhancement requests!

