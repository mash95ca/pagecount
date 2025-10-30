Input Handling:
The user is prompted to enter one or more PDF file paths, separated by commas. The script trims whitespace and validates each path.

PDF Page Counting:
For each file, the script attempts to open and read it using the PyPDF2 library.

If successful, it counts the total number of pages.

If the file is missing or unreadable, a descriptive error message is recorded.

Data Presentation:
A neatly formatted summary table is displayed in the console using the tabulate library, listing:

File Name

Full Path

Page Count or Error Message

CSV Export:
The same results are saved to a CSV file named pdf_page_counts.csv in the current working directory. This file includes all processed file paths and their respective page counts, making it ideal for documentation, audit records, or further analysis.

Error Handling & Robustness:

Handles missing files gracefully (File Not Found).

Catches and logs unexpected errors (e.g., corrupted PDFs).

Ensures the CSV output is safely encoded in UTF-8.

Dependencies:

PyPDF2 for reading PDF metadata and page counts.

tabulate for formatting console output.

Python’s built-in csv and os modules for file operations.
