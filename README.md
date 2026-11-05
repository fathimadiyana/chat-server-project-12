# Chat Saver — BSERC Week 2, Project 12

A Chrome Manifest V3 extension that exports AI chats as Markdown or print-ready PDF. It processes page content in the browser and does not upload chat data.

## Supported sites
- ChatGPT (`chatgpt.com`, `chat.openai.com`)
- Google Gemini (`gemini.google.com`)

The extension uses DOM selectors for these sites. AI websites change their page structure periodically; if a site changes, message detection may need selector updates. Always review the detected message list before exporting.

## Install in Chrome / Edge
1. Extract this ZIP.
2. Open `chrome://extensions` (Edge: `edge://extensions`).
3. Turn on **Developer mode**.
4. Choose **Load unpacked**.
5. Select the extracted `Chat_Saver_Project12` folder (the one containing `manifest.json`).
6. Open a conversation on ChatGPT or Gemini and refresh the page.
7. Click the Chat Saver extension icon, then **Open chat saver**.

## Use
- The panel lists detected messages with checkboxes.
- Select all or only the messages you want.
- **Save Markdown** downloads a `.md` file.
- **Save as PDF** opens a print-ready document. Choose **Save as PDF** in the browser print dialog.
- The filename is based on the chat page title.

## Project requirements mapped
1. Two AI chat websites: ChatGPT and Gemini.
2. Full chat or selected messages: checkbox selection.
3. Headings, lists, tables and code: Markdown conversion retains common structures and fenced code blocks.
4. Markdown and PDF: Markdown download and browser print-to-PDF.
5. Chat-title filename: derived from document title.
6. Privacy: no backend, no fetch requests, no remote upload.

## Test checklist
- Try both websites.
- Test a long conversation with 50+ messages; scroll to load the whole conversation, then use Rescan.
- Select a few messages and export; compare with full export.
- Copy a code block from Markdown and run it.
- Check Markdown tables remain pipe tables and PDF tables remain HTML tables.
- Confirm no network request is made by the extension for exporting.

