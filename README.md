# sql_scan

**sql_scan** is a Python library designed to analyze SQL files by extracting table names and their associated WHERE conditions. This tool facilitates the inspection of SQL queries, making it easier to identify and understand the structure of complex statements.

## Key Features

- **Table Name Extraction**: Identify and extract table names from SQL queries, including those used in `SELECT`, `FROM`, `JOIN`, `INSERT`, `UPDATE`, and `MERGE` statements.
- **WHERE Condition Detection**: Capture all associated WHERE conditions for each identified table, allowing for better understanding and optimization of query logic.
- **Multi-line Support**: Effectively handle SQL queries that span multiple lines, ensuring complete extraction of table names and conditions.
- **Customizable Output**: Write the extracted table names and conditions to a text file for easy review and analysis.

## Installation

You can install **sql_scan** via pip (once published on PyPI):

```bash
pip install sql_scan
