# Meeting Intelligence & Action Tracker

Actual AI at Work / 05

Keep a record of commitments across recurring meetings. Use an AI assistant to extract proposals from notes, then review the proposed changes in the tracker before they are recorded.

**[Launch the application](https://brbgn.github.io/AAIAW-Tools/05-Meeting-Intelligence-Tracker/)** or use GitHub’s download control on [index.html](index.html) and open the downloaded file in a modern browser that permits local HTML files. The tracker requires no account, API key or additional software.

## Record a meeting

1. Select **New workspace** and name the meeting group or project.
2. Open **New meeting**, choose the meeting date and paste the transcript or notes. A plain text file also works.
3. Select **Generate AI prompt**, then **Copy AI prompt**. Paste it into an AI assistant approved for the information you are sharing. The prompt includes current records and a context code. The assistant must return that code with its response.
4. Copy the assistant's JSON response into the response field or upload it as a JSON file. Select **Validate and review**.
5. Check each proposal against the notes. Accept, reject or edit it as appropriate. Select **Apply reviewed changes** to record the meeting. If no changes are proposed, the meeting can still be recorded.

If validation fails, ask the assistant for the requested JSON format. Generate a fresh prompt if the notes or records have changed. Responses without the current context code cannot be imported. Read each quotation and check that it supports the proposed update. Review possible duplicates and missing details.

## Try the fictional example

Select **Try demo** to explore a workspace containing three recorded operations meetings. To practice the import process yourself, create a separate empty workspace and use these examples in order:

| Meeting date | Notes | Example response |
| --- | --- | --- |
| 2026-11-27 | [Meeting 01](examples/01-meeting-transcript.txt) | [Response 01](examples/01-ai-response.json) |
| 2026-12-04 | [Meeting 02](examples/02-meeting-transcript.txt) | [Response 02](examples/02-ai-response.json) |
| 2026-12-07 | [Meeting 03](examples/03-meeting-transcript.txt) | [Response 03](examples/03-ai-response.json) |

Use the exact example notes and dates. Accept the three proposals from Meeting 01 in their supplied order. The later example responses use the resulting IDs. After all three meetings, the tracker contains four records: two completed actions, one open action and one unconfirmed suggestion. The analysis deadline changes once.

The [sample backup](examples/demo-workspace.json) and [sample CSV](examples/sample-action-tracker.csv) represent the state after Meeting 01. Restoring a backup replaces all workspaces, so export existing data first. The response files contain authored examples for practice. No live AI service was used to produce them.

## Use the tracker between meetings

- **Dashboard:** See overdue records, upcoming deadlines and completion counts by owner.
- **Tracker:** Search records, filter by status or type, add or edit records manually and export CSV for Excel or other spreadsheet software.
- **History:** Inspect recorded meeting notes and accepted changes, including their supporting quotations.
- **Agenda & email:** Prepare a next-meeting agenda and copy a follow-up draft. Review the draft before sending it.
- **Data:** Export or restore a JSON backup. A CSV export is for reporting and cannot restore meeting history.

## Privacy and limitations

The application does not send notes or tracker data to a server. It generates a prompt for manual use with an external AI assistant. Submitting that prompt shares its contents with the chosen service, including the notes and existing records. Follow organizational data handling policies and do not publish real workplace data in public repositories.

Browser storage is not encrypted by the application. It may be unavailable in restricted browsers or cleared by browser policies. Storage is specific to the browser profile and site or file location; moving from a downloaded copy to a hosted copy does not transfer records automatically. Keep JSON backups in an approved location and restore them when moving between copies. Use one tab per tracker. If another tab changes the saved data, export your unsaved work and reload. If existing storage cannot be read, it is preserved until you explicitly restore a backup.

The tracker does not provide shared access, live transcription or automatic email delivery. It checks the structure of AI responses and whether evidence quotations appear in the notes. Read the original notes to verify the meaning of each quotation and check for missing commitments.

## License

Distributed under the repository's [MIT License](../LICENSE). No external libraries are bundled with this application.
