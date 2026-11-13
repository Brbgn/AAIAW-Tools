# Excel Difference Detective

A lightweight, no-install HTML tool that compares two `.xlsx` or `.csv` files in your browser. Created for **AAIAW #03** as a practical demonstration of building small business tools with AI coding assistants.



## Try it

- **Local:** Download [index.html](index.html), open it in Chrome, Edge, or another modern browser, then click **Try sample data**.
- **Sample files:** Upload [Sample_Original.xlsx](Sample_Original.xlsx) and [Sample_Updated.xlsx](Sample_Updated.xlsx). Choose worksheet `Projects` and identifier `Record ID`.
- **Make your own:** [Codex_Build_Prompt.txt](Codex_Build_Prompt.txt) provides the business requirements and test plan you can ask Codex to implement.

## What the demo should report

| Metric | Verified sample result |
| --- | ---: |
| Records in original | 75 |
| Records in updated | 77 |
| Added records | 6 |
| Removed records | 4 |
| Changed records | 8 |
| Changed individual fields | 11 |
| Unchanged matching records | 63 |

These figures come from synthetic data. The demo was tested in an automated Chromium browser with the included `.xlsx` inputs, a CSV export, reordered rows, and duplicate identifiers. That is **not** a comprehensive security or compatibility certification.

## How it compares

- Match rows by the selected unique ID, not their position in the workbook.
- Reject blank or duplicate IDs instead of guessing matches.
- Show added, removed, and changed records and per-field before/after values.
- Let readers filter, search, and export the full change details as CSV.
- Keep the original files unchanged.

## Limitations

- Supports `.xlsx` and `.csv`; not legacy `.xls` or password-protected Excel files.
- Does not compare cell styling, charts, macros, or spreadsheet formulas themselves.
- Does **not** recalculate formulas. It relies on the workbook's stored cached values.
- Differing schemas are warned about; columns not shared by both selected sheets cannot be compared field-by-field.
- Uses the bundled JSZip library (v3.10.1, MIT/GPLv3 dual-licensed) inside the HTML file.

For business-critical use, test with representative data and obtain approval from your organization's security team.

## GitHub Pages (optional)

After publishing the repository, you can enable Pages via **Settings → Pages**, deploy from the default branch and root directory, then open the `01-Excel-Difference-Detective/` path on your repository's Pages site. The application will still run inside the reader's browser, but should be independently security-reviewed before public hosting.
