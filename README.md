
# Integrity Checker Project

## Overview

This project is a command-line-based integrity checker designed to ensure the integrity of files using cryptographic hashing. It provides a simple and effective way to monitor changes to files and directories, ensuring data integrity in a secure and efficient manner.

## Features

- **File Hashing**: Generates cryptographic hash values (e.g., SHA-256, SHA-512) for individual files.
- **Recursive Hashing**: Recursively computes hashes for all files within a directory.
- **Integrity Verification**: Compares current file hashes with a baseline to detect unauthorized changes.
- **Detailed Reporting**: Identifies added, modified, or deleted files in a comprehensive report.
- **Cross-Platform Compatibility**: Works on macOS, Linux, and Windows.

## Usage

### Initialize Hash Database
Generate a baseline of hash values for a directory:
```bash
python integrity_checker.py init /path/to/directory
```

### Verify Integrity
Check files for changes by comparing current hashes to the baseline:
```bash
python integrity_checker.py check /path/to/directory
```

### Update Hash Records
Update the stored hashes after confirming file integrity:
```bash
python integrity_checker.py update /path/to/directory
```

### Help
For more options and usage details:
```bash
python integrity_checker.py --help
```

## File Structure

```
.
├── README.md             # Documentation
├── integrity_checker.py  # Main script
├── requirements.txt      # Dependencies
├── hashes/               # Directory for hash records
└── tests/                # Unit tests for the project
```

## How It Works

1. **Hash Generation**: Computes hash values using secure algorithms from the `hashlib` library.
2. **Baseline Storage**: Stores initial hashes in a structured format (e.g., JSON).
3. **Comparison**: Checks the current hashes against the baseline to detect changes.
4. **Reporting**: Summarizes differences in an easy-to-read format.

## Dependencies

Ensure you have Python 3.x installed. Install required packages with:
```bash
pip install -r requirements.txt
```

## License


--- 

Copy and paste this content into your `README.md` file!
