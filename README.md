# SQL Table Name and WHERE Clause Extractor

## Overview

This Python script processes SQL files to extract key information such as table names, SQL operation types (e.g., `FROM`, `JOIN`, `INTO`, `UPDATE`, `MERGE INTO`), and any associated `WHERE` conditions. The script automatically formats the SQL file for better readability and generates a detailed report containing the extracted information.

## Features

- **Table Name Extraction**: Identifies and extracts table names used in SQL operations such as `FROM`, `JOIN`, `INTO`, `UPDATE`, and `MERGE INTO`.
- **WHERE Clause Extraction**: Detects and extracts `WHERE` conditions associated with the SQL queries, including multi-line conditions.
- **SQL File Formatting**: Re-indents SQL statements, converting keywords to uppercase for better readability.
- **Report Generation**: Produces a structured report with table names, operation types, and `WHERE` conditions. If no `WHERE` clause is found, it is indicated in the report.
- **Automated Clean-Up**: Removes temporary files after the process is complete.

## How It Works

1. **SQL File Formatting (optional)**:  
   The script reads an SQL file and reformats it using consistent indentation and uppercase keywords to ensure readability.

2. **Table Name and Keyword Extraction**:  
   The script scans each SQL statement for specific SQL operation keywords (`FROM`, `JOIN`, `INTO`, `UPDATE`, `MERGE INTO`) to identify table names. The names are cleaned to ensure they meet standard naming conventions.

3. **WHERE Clause Detection**:  
   Once a table name is identified, the script searches for associated `WHERE` clauses. It can handle complex, multi-line `WHERE` conditions and ensures they are correctly associated with the relevant table.

4. **Report Generation**:  
   After processing the SQL file, the script generates a report file (`<sql_file_name>_report.txt`). The report includes:
   - Table names.
   - SQL operation types (e.g., `FROM`, `JOIN`, `INTO`, `UPDATE`).
   - Associated `WHERE` conditions, if available.


## Requirements

- Python 3.x
- `sql_scan` library for SQL formatting:
  ```bash
  pip install sql_scan
  ```
