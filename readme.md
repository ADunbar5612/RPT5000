📊 RPT5000 – COBOL Sales Report Generator (Enhanced)

👨‍💻 Authors
Aidan Dunbar

📅 Date: 03/31/2026

🔗 GitHub Repository:
https://github.com/ADunbar5612/RPT5000

📌 Overview

RPT5000 is an enhanced COBOL reporting program based on RPT3000. It processes a customer master file and produces a structured Year-To-Date (YTD) sales report with multi-level control breaks.

🆕 New Features
🧑‍💼 Sales Representative (SALESREP) control break
🏢 Branch-level totals (existing)
🌐 Grand totals across all data
🔄 Improved control logic using switches and structured conditions
⚙️ How It Works
🚀 Initialization
Opens input and output files
Retrieves system date and time
Initializes control fields and switches
Sets up report headings (updated to RPT5000)
🔄 Record Processing

For each customer record:

Reads input data
Detects control breaks:
🧑‍💼 SALESREP change
🏢 BRANCH change
Performs calculations:
💲 Change Amount = This YTD − Last YTD
📊 Change Percent = (Change / Last YTD) × 100
🔁 Control Break Logic
🧑‍💼 SALESREP Break
Triggered when SALESREP changes
Prints SALESREP total line
Resets SALESREP totals
🏢 BRANCH Break
Triggered when BRANCH changes
Prints:
SALESREP totals (if needed)
BRANCH totals
Resets both SALESREP and BRANCH totals
⚠️ Edge Case Handling
If Last YTD = 0:
Percentage is set to 999.9 to prevent division errors
🖨️ Output Generation
Prints:
Customer detail lines
SALESREP totals
BRANCH totals
Grand totals
Uses formatted fields and alignment for readability
🧾 Report Structure

The report includes:

📄 Header with program name (RPT5000)
📋 Customer detail lines
🧑‍💼 SALESREP total lines
🏢 BRANCH total lines
📊 Grand total summary

Each total level is clearly marked with * for visual separation.

🧠 Key Enhancements
🧩 Working Storage Updates
Added:
OLD-SALESREP-NUMBER (control field)
SALESREP total accumulators
Modified:
CUSTOMER-LINE to include SALESREP (PIC X(2))
HEADING-LINE-2 updated to reflect RPT5000
🔀 Logic Improvements
Introduced switch conditions for cleaner control flow
Replaced some IF-ELSE logic with EVALUATE statements
Added new paragraph:
355-PRINT-SALESREP-LINE
🧮 Totals Handling
SALESREP totals calculated separately from BRANCH totals
Proper reset logic implemented at each control break
Grand totals accumulated across all records
📁 Files
📄 File Name	📌 Description
RPT5000.cbl	Enhanced COBOL source program
JCLRPT5.jcl	JCL to compile and execute program
README.md	Project documentation
📝 Notes
🎓 Designed for educational purposes
💡 Demonstrates:
Multi-level control break processing
Advanced COBOL report formatting
Structured programming techniques
Use of switches and EVALUATE statements
⚙️ Some values may be hardcoded for demonstration
