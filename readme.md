📊 RPT5000 – COBOL Sales Report Generator (Enhanced)
👨‍💻 Author

Aidan Dunbar

📅 Date

March 31, 2026

🔗 Repository

https://github.com/ADunbar5612/RPT5000

📌 Overview

RPT5000 is an enhanced COBOL reporting program built upon the foundation of RPT3000. It processes a customer master file to generate a structured Year-To-Date (YTD) sales report featuring multi-level control break logic.

The program emphasizes clean structure, accurate aggregation, and readable report formatting, making it ideal for learning advanced COBOL reporting techniques.

🆕 Key Enhancements
🧑‍💼 Added Sales Representative (SALESREP) control break
🏢 Improved branch-level total calculations
🌐 Implemented grand total accumulation across all records
🔄 Refined control flow using structured logic and switches
🧠 Improved maintainability with EVALUATE-based decision handling
⚙️ Program Workflow
🚀 Initialization
Opens input and output files
Retrieves current system date and time
Initializes control fields and working storage
Sets up report headings (updated to reflect RPT5000)
🔄 Record Processing

For each customer record, the program:

Reads input data
Detects control breaks:
🧑‍💼 SALESREP changes
🏢 BRANCH changes
Performs calculations:
💲 Change Amount = Current YTD − Previous YTD
📊 Change Percent = (Change ÷ Previous YTD) × 100
🔁 Control Break Logic
🧑‍💼 SALESREP Break

Triggered when the Sales Representative changes:

Prints SALESREP total line
Resets SALESREP accumulators
🏢 BRANCH Break

Triggered when the Branch changes:

Prints pending SALESREP totals (if applicable)
Prints BRANCH totals
Resets both SALESREP and BRANCH accumulators
⚠️ Edge Case Handling
If Previous YTD = 0:
Percentage is set to 999.9 to prevent division errors
🖨️ Output Generation

The program produces a formatted report including:

Customer detail lines
SALESREP summary lines
BRANCH summary lines
📊 Grand total summary

All sections are clearly labeled and visually separated using * markers for readability.

🧾 Report Structure

The generated report includes:

📄 Header (Program title: RPT5000)
📋 Customer detail records
🧑‍💼 SALESREP totals
🏢 BRANCH totals
📊 Grand totals
🧠 Technical Improvements
🧩 Working Storage Enhancements

Added:

OLD-SALESREP-NUMBER (control field)
SALESREP-level accumulators

Modified:

CUSTOMER-LINE to include SALESREP (PIC X(2))
HEADING-LINE-2 updated for RPT5000
🔀 Logic Refinements
Introduced switch-based control logic for clarity
Replaced nested IF statements with EVALUATE constructs
Added modular paragraph:
355-PRINT-SALESREP-LINE
🧮 Totals Management
SALESREP totals handled independently from BRANCH totals
Proper reset logic at each control break level
Grand totals accumulated across all processed records
📁 Project Files
File Name	Description
RPT5000.cbl	Enhanced COBOL source program
JCLRPT5.jcl	JCL for compilation and execution
README.md	Project documentation
📝 Notes
🎓 Designed for educational purposes
💡 Demonstrates:
Multi-level control break processing
Advanced COBOL report formatting
Structured programming techniques
Use of switches and EVALUATE statements
⚙️ Some values are intentionally hardcoded for demonstration and learning clarity
