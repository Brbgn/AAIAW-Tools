# Excel Difference Detective

Compare an original and updated `.xlsx` or `.csv` file in your browser. The app matches rows by a selected unique identifier and produces an itemized report of added, removed, and changed records.

**[Launch Excel Difference Detective](https://brbgn.github.io/AAIAW-Tools/01-Excel-Difference-Detective/)**

## Get started

1. Open the online app, or download [the standalone HTML file](index.html) from GitHub and open it in a modern browser.
2. Click **Try sample data** for an instant demonstration, or select your own files in the **Original file** and **Updated file** boxes.
3. For the included workbooks, select the `Projects` worksheet and `Record ID` as the unique ID column.
4. Click **Compare files**, review the differences, and use **Export CSV** if you want a report.

The included [original workbook](Sample_Original.xlsx) and [updated workbook](Sample_Updated.xlsx) contain **fictional** project records. You can also inspect the [example difference report](Sample_Difference_Report.csv).

## Verified example results

| Metric | Expected result |
| --- | ---: |
| Records in original workbook | 75 |
| Records in updated workbook | 77 |
| Added records | 6 |
| Removed records | 4 |
| Changed records | 8 |
| Changed individual fields | 11 |
| Unchanged matching records | 63 |

The example was checked with the included Excel files, CSV export, reordered rows, and duplicate identifiers in an automated browser test. This does not cover every possible workbook or establish suitability for business-critical processing.

## How the comparison works

- Uses the unique ID column to match records, regardless of row order.
- Rejects duplicate or missing IDs rather than guessing which records match.
- Reports new and removed records, plus before-and-after values for changed fields.
- Provides search, category filters, and a CSV export of the comparison results.
- Leaves input files unchanged.

## Limits to know about

- Supports `.xlsx` and `.csv`, but not `.xls`, encrypted workbooks, or password-protected files.
- Compares data values, not formatting, charts, macros, or formula text.
- Does **not** recalculate Excel formulas. Formula cells use cached workbook values where available.
- Warns about mismatched columns; only matching column headers can be compared field by field.
- Uses the bundled JSZip library for Excel parsing.

## Build your own version

The [starter prompt](Codex_Build_Prompt.txt) describes the requirements and tests for a similar application. It can be adapted for AI coding assistants such as Codex or Claude Code. Generated code should be tested before use, especially when handling business data.

## Privacy and licensing

The app processes selected files locally in the browser and does not intentionally send their contents to a server. Follow your employer's security requirements before using it with work data.

The original project code is available under the [MIT License](../LICENSE). The bundled JSZip and pako libraries retain their own licensing terms, described in the [third-party notices](../THIRD_PARTY_NOTICES.md).
