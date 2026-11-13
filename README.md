# AAIAW Tools

**Actual AI at Work**: practical mini-tools and AI workflows for people whose day job isn't writing code.

Built around familiar business problems: Excel files, reporting, document comparisons, and the little repetitive tasks that eat up an afternoon.

## Mini-tools

| Episode | Tool | What it does |
| --- | --- | --- |
| #03 | [Excel Difference Detective](01-Excel-Difference-Detective/) | Compare two `.xlsx` or `.csv` files by a unique ID and export an itemized change report. |

### Start here

1. Open [Excel Difference Detective](01-Excel-Difference-Detective/index.html) from the repository and download the HTML file to run locally, and open it in the browser. The sample workbooks and Codex prompt are available in the same directory.
2. Open the HTML file in a modern desktop browser.
3. Use the built-in demo or compare the included fictional workbooks.
4. Review the results and limitations before using the tool for real work.

**Everything in the sample data is fictional.** The tool is an educational demonstration, not production-approved business software.

## How this project is organized

Each mini-tool folder contains a runnable demonstration, sample data, a starting prompt, and a short explanation of its limitations. Future AAIAW episodes can be added as new numbered folders.

## Responsible use

- Never upload private, customer, employee, payroll, or confidential data to a public GitHub repository.
- Follow your employer's IT security and software policies before using any third-party or AI-generated tool with work data.
- Keep source files unchanged and independently validate results for important decisions.
- The file comparison tool runs in the browser and does not intentionally send uploaded workbook data to a server. It is **not** a substitute for a security review.

## License

The original code and documentation in this repository are released under the [MIT License](LICENSE). You may use, adapt, and redistribute them subject to that license's conditions.

The application also bundles third-party software, including [JSZip v3.10.1](https://github.com/Stuk/jszip), which is dual-licensed under MIT or GPLv3, and its dependency [pako](https://github.com/nodeca/pako), licensed under MIT. Those components remain subject to their respective licenses. Their attribution notices are preserved in the distributed HTML application.
