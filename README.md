# Windows_to_WSL-path-converter-tool

A lightweight web-based tool for converting Windows file paths to WSL (Windows Subsystem for Linux) format. Perfect for developers working across Windows and WSL environments who need to quickly convert file paths for command-line operations.

# Features
- Instant Path Conversion - Paste Windows paths and get WSL paths in real-time
- File Picker Integration - Select multiple files through a browser dialog
- Folder Picker Support - Choose entire directories with all nested files
- Base Path Reconstruction - Work around browser security limitations by specifying a base Windows path
- Batch Processing - Convert multiple paths at once
- One-Click Copy - Copy all converted paths to clipboard instantly
- No Installation Required - Pure HTML/CSS/JavaScript, runs entirely in your browser
- Offline Capable - No server or internet connection needed

# Use Cases
- Converting file paths for WSL command-line operations
- Batch processing files stored on Windows from WSL
- Scripting workflows that bridge Windows and WSL environments
- Quick path format conversion without manual typing

# How It Works

The tool converts Windows paths like:

Into WSL paths like:

## Conversion Rules
- Converts drive letters (C:, D:, etc.) to /mnt/c, /mnt/d, etc.
- Replaces backslashes (\) with forward slashes (/)
- Handles quoted paths automatically
- Preserves relative paths when no drive letter is present

# Usage

### Method 1: Manual Paste
- Open index.html in any modern web browser
- Paste Windows paths into the left textarea (one per line)
- WSL paths appear automatically in the right textarea
- Click "Copy Output" to copy converted paths

### Method 2: File Picker
- (Optional but recommended) Enter your base Windows path (e.g., C:\Users\username\Desktop\project)
- Click "Pick Files…" to select multiple files
- Tool generates full Windows paths and converts them to WSL format
- Click "Copy Output" to use in your terminal

### Method 3: Folder Picker
- (Optional but recommended) Enter your base Windows path
- Click "Pick Folder…" to select an entire directory
- Tool processes all files recursively and converts paths
- Click "Copy Output" to use in your terminal

# Why Base Windows Path?

## Due to browser security restrictions, file pickers only provide:
- File names when picking individual files
- Relative paths when picking folders

By specifying a base Windows path, the tool can reconstruct full absolute paths like C:\Users\username\Desktop\project\subfolder\file.txt and convert them properly to WSL format.

### Without base path:

### With base path (C:\Users\username\Desktop\project):

# Installation

No installation needed! Just download and open index.html in your browser.

# Browser Compatibility

- Works in all modern browsers:
- Chrome/Edge (recommended)
- Firefox
- Safari
- Opera

# Requires support for:
- File API
- Clipboard API (for copy functionality)
- webkitdirectory attribute (for folder picking)
 
# Tips
- **Bookmark it** : Save the HTML file to your desktop or bookmark it for quick access
- **Use base path** : Always fill in the base Windows path for accurate full path conversion
- **Batch operations** : Select entire folders to convert hundreds of paths at once
- **Clear button** : Use "Clear" to reset and start a new conversion session

# Technical Details
- **Pure client-side** : All processing happens in your browser, no data is sent anywhere
- **Lightweight** : Single HTML file under 10KB
- **Responsive** : Works on desktop and tablet screens
- **No dependencies** : No frameworks, libraries, or external resources required

# License

MIT License - Feel free to use, modify, and distribute.

# Contributing

Contributions welcome! Feel free to:
- Report bugs
- Suggest features
- Submit pull requests

# Author

Created for developers working across Windows and WSL environments who need a quick, reliable path conversion tool.

### Note: 
This tool is designed for local use and does not collect or transmit any data. All conversions happen entirely within your browser.
