# AI Meeting Intelligence Agent with n8n

An AI-powered meeting workflow that converts transcripts into summaries, decisions, action items, Google Docs reports, Google Sheets task records, and Gmail follow-up drafts.

Built by **Animty** using n8n and Google Gemini.

## Features

- Accepts meeting titles, attendee emails, and transcripts through an n8n form
- Generates a concise meeting summary
- Extracts confirmed decisions
- Identifies tasks, owners, deadlines, and status
- Identifies unresolved questions
- Creates a structured Google Docs report
- Adds each action item as a separate Google Sheets row
- Creates a Gmail follow-up draft for human review
- Never sends AI-generated emails automatically
- Treats meeting transcripts as untrusted content

## Workflow

```text
Meeting Form
    ↓
AI Meeting Analyst
    ↓
Parse Meeting Analysis
    ├── Create Google Docs Report
    ├── Log Action Items in Google Sheets
    └── Create Gmail Follow-Up Draft
```

## Technology

- n8n
- Google Gemini
- Google Docs API
- Google Sheets API
- Gmail API
- JavaScript

## Setup

1. Import the workflow JSON into n8n.
2. Add your Google Gemini credential.
3. Connect Google Docs, Google Sheets, and Gmail OAuth credentials.
4. Create a Google Sheet with these columns:

```text
Timestamp
Meeting Title
Task
Owner
Deadline
Status
```

5. Select your own Google Sheet in the logging node.
6. Test the workflow using fictional meeting information.
7. Review every generated email draft before sending it.

## Security

- Never upload API keys, tokens, or OAuth secrets.
- Do not publish private meeting transcripts.
- Do not expose attendee email addresses.
- Use fictional information in screenshots and demonstrations.
- Review AI-generated decisions and action items for accuracy.
- Keep email sending under human control.

## Limitations

- The workflow currently accepts pasted transcripts rather than audio.
- Action-item accuracy depends on transcript quality.
- Ambiguous owners are labeled `Unassigned`.
- Missing deadlines are labeled `Not specified`.
- Generated reports and drafts require human review.

## Future Improvements

- Audio transcription
- Calendar-event suggestions
- Persistent task tracking
- Automated reminders
- Speaker identification
- Meeting analytics dashboard
- Integration with project-management tools

## About Animty

Animty builds practical AI agents and workflow automations for businesses in Nassau, Bahamas.

Call or WhatsApp: **(242) 824-0275**

## Project Series

This is Project 6 in Animty’s AI-agent portfolio and August Day 1 of building practical business automations.
AI Meeting
