# Largest Files Scanner

A Windows GUI application built with PowerShell that helps you find and analyze the largest files on your drives or in specific folders. Perfect for disk cleanup, storage analysis, and identifying space-consuming files.

## Features

- **Intuitive GUI Interface**: Easy-to-use Windows Forms interface
- **Flexible Scanning**: Scan entire drives or specific folders
- **Customizable Filters**: Set minimum file size thresholds (in MB)
- **Configurable Results**: Limit the number of results to display
- **Progress Tracking**: Real-time progress bar and status updates
- **Results Viewer**: View results in a sortable, filterable grid
- **CSV Export**: Export results to CSV format for further analysis
- **Detailed Information**: Shows file paths and sizes in both GB and MB

## Requirements

- **Windows Operating System** (Windows 10 or later recommended)
- **PowerShell 5.1 or later** (pre-installed on modern Windows)
- **.NET Framework** (typically pre-installed on Windows)

## Installation

No installation required! Simply download the `gui.ps` file to your computer.

## Usage

### Running the Application

1. **Right-click** on `gui.ps` and select **"Run with PowerShell"**
   
   *OR*

2. Open PowerShell and navigate to the directory containing the file:
   ```powershell
   cd C:\path\to\Largest-Files-Scanner
   .\gui.ps
   ```

### Using the Application

1. **Drive / Folder**: Enter the path you want to scan (e.g., `C:\`, `D:\`, or `C:\Users\YourName\Documents`)
2. **Min size (MB)**: Set the minimum file size threshold (default: 50 MB)
3. **Max results**: Set the maximum number of results to display (default: 25)
4. Click **Scan** to start the scanning process
5. Monitor the progress bar and status messages
6. Once complete, use **View Results** to see the files in a grid view
7. Use **Export CSV** to save the results to a file

### Execution Policy

If you encounter an execution policy error, you may need to allow script execution:

```powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
```

## How It Works

The scanner performs a three-phase operation:

1. **Phase 1**: Recursively enumerates all files in the specified path
2. **Phase 2**: Filters files that meet or exceed the minimum size threshold
3. **Phase 3**: Sorts files by size (largest first) and selects the top results

## Example Use Cases

- **Disk Cleanup**: Find large files taking up space on your system drive
- **Media Management**: Locate large video or audio files
- **Development**: Find large build artifacts or dependencies
- **Backup Planning**: Identify files that should be archived or backed up separately
- **Storage Analysis**: Understand where disk space is being consumed

## Tips

- Scanning large drives (like C:\) may take several minutes depending on the number of files
- Use more specific paths for faster results (e.g., `C:\Users` instead of `C:\`)
- Increase the minimum size threshold to reduce scan time and focus on truly large files
- Administrator privileges may be required to access certain system folders

## License

This project is licensed under the terms included in the LICENSE file.

## Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the issues page.

## Author

j-abed
