# AAIAW Tools

**Actual AI at Work (AAIAW)** is a collection of practical mini-tools and AI workflows for everyday office tasks. The examples are designed to be useful even if you have never written code.

## Available tools

| Episode | Tool | What it does |
| --- | --- | --- |
| #03 | [Excel Difference Detective](https://brbgn.github.io/AAIAW-Tools/01-Excel-Difference-Detective/) | Compare two Excel or CSV files by a unique ID, review changes, and export a detailed CSV report. |

## Try Excel Difference Detective

- **[Launch the online tool](https://brbgn.github.io/AAIAW-Tools/01-Excel-Difference-Detective/)** in your browser. No account or installation is required.
- **[Get the sample Excel files and instructions](01-Excel-Difference-Detective/README.md)** from the tool's folder.
- **[Explore the source code](01-Excel-Difference-Detective/index.html)** or download the HTML file from GitHub to run it locally.
- **[Use the starter prompt](01-Excel-Difference-Detective/Codex_Build_Prompt.txt)** to explore building a similar app with an AI coding assistant.

To try a ready-made example, open the app and select **Try sample data**. The sample workbooks use fictional project records.

## Repository structure

Each mini-tool has a numbered folder containing its application, sample data, build prompt, and documentation. The repository homepage is in `index.html`.

## Responsible use

- All included sample data is fictional. Do not commit employee, customer, financial, or other confidential business records to public GitHub repositories.
- Check your organization's IT security and software policies before opening custom apps with work files.
- Excel Difference Detective processes user-selected files inside the browser and does not intentionally upload workbook contents to a server. This is an educational tool, **not** a security certification or an enterprise reconciliation system.
- Review the comparison findings independently before using them for business decisions. The tool does not recalculate formulas or compare macros, charts, or cell styling.

## License

The original project code and documentation are available under the [MIT License](LICENSE). Reuse and redistribution are permitted subject to its terms.

The application includes [JSZip v3.10.1](https://github.com/Stuk/jszip) (MIT or GPLv3) and its [pako](https://github.com/nodeca/pako) dependency (MIT). Their existing copyright notices are preserved in the HTML application. See [Third-party notices](THIRD_PARTY_NOTICES.md).
