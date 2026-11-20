# AAIAW Tools

**Actual AI at Work (AAIAW)** is a collection of practical mini-tools and AI workflows for everyday office tasks. The examples are designed to be useful even if you have never written code.

## Available tools and learning kits

| Episode | Resource | What it does |
| --- | --- | --- |
| #04 | [SOP Knowledge Kit](https://brbgn.github.io/AAIAW-Tools/04-SOP-Knowledge-Kit/) | Turn scattered fictional evidence into clear SOPs, organize them in a searchable ledger, and maintain change history. |
| #03 | [Excel Difference Detective](https://brbgn.github.io/AAIAW-Tools/01-Excel-Difference-Detective/) | Compare two Excel or CSV files by a unique ID, review changes, and export a detailed CSV report. |

## AAIAW #04: SOP Knowledge Kit

- **[Explore the searchable example SOP catalog](https://brbgn.github.io/AAIAW-Tools/04-SOP-Knowledge-Kit/)** with Finance, IT, and People Operations examples.
- **[Download the Excel master ledger](04-SOP-Knowledge-Kit/SOP_Master_Ledger.xlsx)** for categories, links, owners, review dates, and change tracking.
- **[Use the Word SOP template](04-SOP-Knowledge-Kit/SOP_Template.docx)** and [completed expense example](04-SOP-Knowledge-Kit/FIN-001_Expense_Reimbursement.docx).
- **[Read the fictional source pack](04-SOP-Knowledge-Kit/Source_Pack/)** and [reuse the AI workflow prompts](04-SOP-Knowledge-Kit/AI_SOP_Workflow_Prompts.txt).
- **[Read the full #04 guide](04-SOP-Knowledge-Kit/README.md)** for the limits of AI-assisted SOP creation and retrieval.

## AAIAW #03: Excel Difference Detective

- **[Launch the online tool](https://brbgn.github.io/AAIAW-Tools/01-Excel-Difference-Detective/)** in your browser. No account or installation is required.
- **[Get the sample Excel files and instructions](01-Excel-Difference-Detective/README.md)** from the tool's folder.
- **[Explore the source code](01-Excel-Difference-Detective/index.html)** or download the HTML file from GitHub to run it locally.
- **[Use the starter prompt](01-Excel-Difference-Detective/Codex_Build_Prompt.txt)** to explore building a similar app with an AI coding assistant.

To try a ready-made example, open the app and select **Try sample data**. The sample workbooks use fictional project records.

## Repository structure

Each episode has a numbered folder with its demonstration, sample data, and documentation. The repository homepage is in `index.html`.

## Responsible use

- All included sample data is fictional. Do not commit employee, customer, financial, or other confidential business records to public GitHub repositories.
- Check your organization's IT security and software policies before opening custom apps or using AI tools with work files.
- Excel Difference Detective processes user-selected files inside the browser and does not intentionally upload workbook contents to a server. It is an educational tool, **not** a security certification or an enterprise reconciliation system.
- The SOP Knowledge Kit illustrates document governance but does **not** automatically index an organization's Google Drive or SharePoint for AI. Real SOPs need authorized validation, publication, access controls, and version management.
- Review important AI results independently before operational decisions.

## License

The original project code and documentation are available under the [MIT License](LICENSE). Reuse and redistribution are permitted subject to its terms.

Excel Difference Detective includes [JSZip v3.10.1](https://github.com/Stuk/jszip) (MIT or GPLv3) and its [pako](https://github.com/nodeca/pako) dependency (MIT). Their existing copyright notices are preserved in the HTML application. See [Third-party notices](THIRD_PARTY_NOTICES.md).
