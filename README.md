# Zapret Updater

Batch script designed to automatically update the [Flowseal/zapret-discord-youtube](https://github.com/Flowseal/zapret-discord-youtube). It checks for the latest version, downloads it, and installs it. The script also handles removing older versions and services, ensuring the smooth installation of the updated version.

## Prerequisites

Before running the script, make sure the following programs are installed on your system:

- **[7-Zip](https://www.7-zip.org/)** or **[WinRAR](https://www.rarlab.com/)** (for extracting downloaded archives)
  - The script will automatically detect whether either of these archivers is installed by checking the Windows registry.

Also, ensure that the script is located in the same folder as `zapret-discord-youtube` for proper operation.

## Usage

1. **Place the script** in the folder where `zapret-discord-youtube` is located.
2. **Run the script** by calling it from the command line:

    ```
    zapret_update.bat [version]
    ```

   Replace `[version]` with the desired version number. If no version is specified, the script will fetch the latest version available from the GitHub repository.

### Example 1: Update to a specific version

```cmd
zapret_update.bat 1.6.3
```

### Example 2: Update to the latest version

If no version number is provided, the script will automatically fetch the latest version available:

```cmd
zapret_update.bat
```

The script will:

- Check for the installed version of **[Flowseal/zapret-discord-youtube](https://github.com/Flowseal/zapret-discord-youtube)**.
- Compare it with the latest available version on GitHub.
- If a new version is available, it will prompt for confirmation to update.
- Download and extract the new version using **[7-Zip](https://www.7-zip.org/)** or **[WinRAR](https://www.rarlab.com/)**.
- Stop and remove the old `zapret` and `WinDivert` services.
- Remove old files and install the new version.

## Notes
- **Administrator permissions** are required for stopping and deleting system services. The script will attempt to run with elevated privileges if needed.
- If an update is not necessary (i.e., the latest version is already installed), the script will exit without making any changes.

## Troubleshooting
- If the script fails to download or extract the archive, ensure that you have a stable internet connection.
- If **[7-Zip](https://www.7-zip.org/)** or **[WinRAR](https://www.rarlab.com/)** are not installed, the script will terminate with an error message indicating that no archiver was found.

## License
This script is distributed under the MIT License.
