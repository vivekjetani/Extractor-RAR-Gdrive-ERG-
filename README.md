# Extractor RAR Gdrive (ERG)

## Overview
Extractor RAR Gdrive (ERG) is a Python script designed to extract RAR files stored on Google Drive using Google Colab. This script automates the process of mounting Google Drive, installing necessary dependencies, extracting the RAR file, and listing the extracted files.

## How to Use
To utilize ERG, follow these steps:

1. **Mount Google Drive:** Run the provided code snippet to mount your Google Drive onto Google Colab.
   ```python
   from google.colab import drive
   drive.mount('/gdrive')
   ```

2. **Set Working Directory:** Change the directory to the location of your RAR file on Google Drive.
   ```python
   %cd /gdrive/MyDrive/<rar_file_location>
   ```

3. **List Files:** Confirm that the RAR file is present in the specified directory.
   ```python
   !ls
   ```

4. **Install Unrar:** Install the Unrar utility to extract RAR files.
   ```python
   !sudo apt-get install unrar
   ```

5. **Extract RAR File:** Execute the command to extract the RAR file.
   ```python
   !unrar x 'rar_file_name.rar'
   ```

6. **Check Extracted Files:** Verify that the files have been successfully extracted.
   ```python
   !ls
   ```

## Contributions
Contributions to the ERG project are welcome! Feel free to submit bug reports, feature requests, or pull requests through GitHub.

## License
This project is licensed under the [MIT License](LICENSE).
