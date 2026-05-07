---

### RPT5000
**COBOL Sales Report Generator (Enhanced)**
👤 Author: [Aidan Dunbar](https://github.com/ADunbar5612) | 📅 Date: March 31, 2026
🔗 [GitHub Repository](https://github.com/ADunbar5612/RPT5000)

- **Short Summary:** An enhanced COBOL reporting program built upon RPT3000. Processes a customer master file to generate a structured YTD sales report featuring multi-level control break logic at the Sales Representative and Branch levels, with grand total accumulation across all records.
- **Technologies Used:**
  - COBOL (Enterprise COBOL 6.4)
  - JCL
  - z/OS Mainframe Environment
  - Visual Studio Code + Zowe Explorer
  - Partitioned Datasets (PDS)
- **Key Learning Concepts:** Multi-level control break processing (SALESREP → BRANCH → Grand Total), switch-based control logic, `EVALUATE`-based decision handling, structured accumulator reset logic, and divide-by-zero edge case handling in financial reporting.
- **Key Enhancements over RPT3000:**
  | Enhancement | Description |
  |-------------|-------------|
  | 🧑‍💼 SALESREP Control Break | Added Sales Representative-level break and totals |
  | 🏢 Branch Totals | Improved branch-level accumulation and reset logic |
  | 🌐 Grand Totals | Accumulation across all processed records |
  | 🔄 Control Flow | Refined using structured switches and `EVALUATE` |
  | 🧠 Maintainability | Modular paragraph `355-PRINT-SALESREP-LINE` added |
- **Report Structure:**
  | Section | Description |
  |---------|-------------|
  | 📄 Header | Program title and run date/time |
  | 📋 Detail lines | Individual customer records |
  | 🧑‍💼 SALESREP totals | Subtotals per sales representative |
  | 🏢 Branch totals | Subtotals per branch |
  | 📊 Grand totals | Aggregated summary across all records |
- **Project Status:** ✅ Completed
- **Course / Self-Project:** CIS352 Introduction to Enterprise Computing
- **Files:**
  | File | Description |
  |------|-------------|
  | `RPT5000.cbl` | Enhanced COBOL source program |
  | `JCLRPT5.jcl` | JCL for compilation and execution |
  | `README.md` | Project documentation |
- **Thumbnail Screenshot:**
  > `![RPT5000 Screenshot](assets/rpt5000-thumbnail.png)`
- **Repository Link:** [View RPT5000 on GitHub](https://github.com/ADunbar5612/RPT5000)

[🔼 Back to TOC](#table-of-contents)
