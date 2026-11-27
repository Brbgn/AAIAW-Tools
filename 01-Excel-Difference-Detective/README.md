# Excel Difference Detective

A standalone browser tool for comparing `.xlsx` and `.csv` files by a unique record ID. Part of Actual AI at Work (AAIAW #03).

## Try it

- **Online:** [Open the application](https://brbgn.github.io/AAIAW-Tools/01-Excel-Difference-Detective/).
- **Local:** Download [index.html](index.html) from GitHub, then open it in a modern browser that permits local HTML files. Select **Try sample data**.
- **Sample workbooks:** Upload [Sample_Original.xlsx](Sample_Original.xlsx) and [Sample_Updated.xlsx](Sample_Updated.xlsx). Choose worksheet `Projects` and unique ID `Record ID`.
- **Sample report:** [Sample_Difference_Report.csv](Sample_Difference_Report.csv) contains the expected differences for the fictional workbooks.
- **Make your own:** [Codex_Build_Prompt.txt](Codex_Build_Prompt.txt) provides the requirements and testing instructions for building a similar tool.

## Expected demo result

| Metric | Result |
| --- | ---: |
| Records in original | 75 |
| Records in updated | 77 |
| Added records | 6 |
| Removed records | 4 |
| Changed records | 8 |
| Changed individual fields | 11 |
| Unchanged matching records | 63 |

The sample workbooks contain fictional project records.

## Compare your files

1. Choose the original and updated files. Select a worksheet in each, then choose a unique identifier shared by both.
2. Click **Compare files**. Review the summary, the before-and-after details and any comparison notes.
3. Use the result filters and search field to find records. **Export CSV** downloads the full report, including any unverified values and comparison notes. A successful comparison with no differences can produce a header-only CSV.
4. After changing a file, sheet or ID column, run the comparison again.

Each nonempty row needs a unique, nonblank ID. Both selected sheets need a header row on row 1, and populated columns must have names. Missing or duplicate IDs, duplicate headers and populated cells without headers are rejected. Row order does not affect the matching. ID matching is case-sensitive after trimming surrounding whitespace. Column header matching ignores case and repeated whitespace.

## Limitations

- Supports standard `.xlsx` workbooks and UTF-8 CSV files, including UTF-8 BOM and UTF-16 files with a byte-order mark. Comma, semicolon and tab delimiters are supported. Legacy `.xls` and password-protected workbooks are unsupported.
- The XLSX parser supports up to 125,000 worksheet rows and 201 columns. Populated worksheet data beyond the column limit is rejected. Empty formatted cells beyond that limit can be ignored. CSV file capacity depends on available browser memory, and large files may require substantial resources.
- Compares stored cell values. Formatting, charts, macros, workbook formulas, and Excel's displayed date formatting are outside the comparison scope. Dates stored as Excel serial numbers remain numeric.
- Formula results come from cached workbook values. Formulas are never recalculated. Missing cached results are reported as unverified and excluded from confirmed change counts. A record with confirmed differences can also contain unverified fields.
- Numeric strings with standard decimal or scientific notation are compared by their exact numeric value. Text with leading zeros stays distinct. Other text comparisons preserve case and whitespace.
- Columns appearing in only one selected sheet are listed in the comparison notes and excluded from field comparisons. When no common non-ID columns exist, matching records are unverified.
- CSV exports include the UTF-8 byte-order mark, quote fields and protect formula-like cells by prefixing text where needed. Open the CSV with the correct character encoding and review any import formatting in your spreadsheet application.

## Privacy and license

The application reads the files inside your browser and does not change the original files or send their contents to a server. For business-critical use, verify the results with representative data and follow your organization's security and retention policies.

The original application code is available under the repository's [MIT License](../LICENSE). The HTML includes JSZip v3.10.1 and its bundled pako dependency. Their MIT notices are included in the standalone file. See the [third-party notices](../THIRD_PARTY_NOTICES.md).
