# data-cleaning-structural-validation
Data Cleaning & Structural Validation

Project Overview

This project focuses on transforming a raw and unstructured dataset into a clean, consistent, and analysis-ready format. The dataset contained duplicate records, missing values, inconsistent text formatting, and data validation issues.

The objective was to improve data quality while preserving data integrity and ensuring the dataset could be reliably used for further analysis.

---

Dataset Information

Columns

- Date
- Client
- Contact
- Department
- Payment Method
- Revenue
- Profit
- Profit Margin

---

Data Quality Issues Identified

1. Duplicate Records

- Duplicate rows were identified and removed.
- Total duplicates removed: 18

2. Missing Values

- Blank cells were identified in multiple columns.
- Missing values were reviewed and handled appropriately.

3. Inconsistent Text Formatting

Examples:

- MCDONALD'S CORP
- Bill SmITH
- JoSE Roach

These values were standardized into a consistent format.

4. Invalid Formula Outputs

Examples:

- #DIV/0!

These errors were identified and corrected where possible.

5. Inconsistent Data Formats

- Currency values contained symbols and extra characters.
- Date values were standardized.
- Department names were standardized.

---

Data Cleaning Process

Step 1: Created a Working Copy

- Preserved the original dataset.
- Performed all cleaning operations on a duplicate copy.

Step 2: Removed Duplicate Records

Excel Tool Used:

Data → Remove Duplicates

Result:

- 18 duplicate rows removed.

Step 3: Identified Missing Values

Excel Tool Used:

Data → Filter

Checked each column for:

- Blank values
- Invalid entries
- Formula errors

Step 4: Standardized Text Values

Client and Contact names were converted into Proper Case.

Formula Used:

=PROPER(B2)

Example:

Before:
Bill SmITH

After:
Bill Smith

---

Step 5: Removed Extra Spaces

Formula Used:

=TRIM(B2)

Purpose:

- Remove leading spaces
- Remove trailing spaces
- Remove multiple spaces between words

---

Step 6: Standardized Dates

Converted all dates into a consistent format:

YYYY-MM-DD

Excel Format Applied:

yyyy-mm-dd

---

Step 7: Cleaned Revenue and Profit Fields

Removed:

- Currency symbols ($)
- Extra spaces
- Unwanted characters

Functions Used:

- Find & Replace
- Format Cells

---

Step 8: Validated Profit Margin

Profit Margin Formula:

=(Profit/Revenue)*100

Example:

=(G2/F2)*100

Where:

- F = Revenue
- G = Profit

Invalid values such as #DIV/0! were reviewed and corrected.

---

Step 9: Final Validation

Verified:

- No duplicate records
- Consistent text formatting
- Standardized dates
- Valid numeric values
- Correct profit margin calculations

---

Excel Functions Used

Function| Purpose
PROPER()| Convert text to Proper Case
TRIM()| Remove extra spaces
IFERROR()| Handle formula errors
FIND & REPLACE| Remove unwanted symbols
REMOVE DUPLICATES| Eliminate duplicate rows
FILTER| Identify missing values
FORMAT CELLS| Standardize dates and currency

Example:

=IFERROR((G2/F2)*100,"")

---

Tools Used

- Microsoft Excel
- GitHub

---

Final Outcome

The dataset was successfully cleaned and validated through a structured data quality process. Duplicate records, missing values, inconsistent formatting, and formula errors were addressed, resulting in a reliable dataset suitable for analysis and reporting.

---

Author

Mokshitha

Data Analytics Internship Project