# Tax Data Import and Processing System

This repository contains a Python-based system for importing and processing tax-related data files. The system handles various fixed-width text files containing tax information, account details, and property data.

## Features

- Imports multiple fixed-width text files with different encodings support
- Processes tax bills, account information, and property data
- Handles various data types and formats
- Merges related data into comprehensive datasets

## File Processing

The system processes the following files:

### 1. CITYBILL.txt
- Contains billing information
- Fields include: Bill Account, Bill Type, Real Value, Personal Value, etc.
- Fixed-width format with specific column specifications

### 2. ACCOUNT.txt
- Contains account holder information
- Fields include: Account Number, Account Type, Names, SSN, Business Details, etc.
- Fixed-width format with address and contact information

### 3. PARCEL.txt
- Contains property parcel information
- Fields include: Parcel ID, Legal Description
- Fixed-width format for property details

### 4. NASH.txt
- Contains comprehensive property and tax information
- Includes jurisdiction details, property IDs, values, and location data
- Extended property and owner information

## Technical Details

### Dependencies
- pandas
- Python 3.x

### Data Types
The system handles various data types including:
- Strings (for IDs, names, addresses)
- Integers (for values, counts)
- Floats (for measurements)

### Encoding Support
Multiple encodings are supported:
- cp1252
- windows-1252
- latin1
- iso-8859-1

## Usage

1. Place your data files in the specified data directory
2. Run the script to process the files
3. Access the merged data through the resulting DataFrames

## Data Directory Structure

```
data/
├── CITYBILL.txt
├── ACCOUNT.txt
├── PARCEL.TXT
└── NASH.txt
```

## Output

The system produces merged datasets that combine information from multiple sources:
- `merged_df`: Combines CITYBILL and ACCOUNT data
- `edge_df`: Adds PARCEL data to the merged dataset
- `nash_df`: Processes NASH data separately

## Contributing

Feel free to submit issues and enhancement requests!