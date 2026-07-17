# Privacy Policy — ABDK Confy AI

**Effective date:** 2026-07-17
**Publisher:** ABDK Consulting, Estonia
**Contact:** [dmitry@abdkconsulting.com](mailto:dmitry@abdkconsulting.com)
**Add-in hosted at:** https://confyai.abdk.consulting

---

## 1. Overview

ABDK Confy AI is a Microsoft Excel task-pane add-in that lets you analyze and modify spreadsheets using an AI assistant while keeping designated columns private. This policy explains what data is processed when you use the add-in, where it goes, and what rights you have.

**The short version:** ABDK Consulting collects no personal data. Your spreadsheet data is sent only to OpenAI (and only the columns you did not mark as private). Your API key is stored on your device only and is never transmitted to ABDK.

---

## 2. Data Processed by the Add-in

### 2.1 OpenAI API Key

- You supply your own OpenAI API key on first launch.
- The key is stored **locally on your device** — in Excel's per-document secure storage (`OfficeRuntime.storage`) when used as an Excel add-in.
- The key is never sent to ABDK Consulting or any server other than OpenAI's API endpoints (`api.openai.com`).

### 2.2 Spreadsheet Data

- When you send a message to the AI, the add-in reads the currently open workbook and constructs a request.
- **Private columns** — columns you explicitly marked as sensitive — are **excluded entirely** from every request. Their values are never read by the AI and never leave your device in connection with the AI chat.
- **Non-private columns** (headers and cell values) are included in requests sent to OpenAI's API so the AI can answer your questions and suggest edits.
- No spreadsheet data is sent to ABDK Consulting or stored on any ABDK server.

### 2.3 Chat Messages

- The text of your chat messages is sent to OpenAI's API as part of each request.
- Chat history is retained in the add-in's session memory for conversation context and is discarded when you close or reset the chat. It is not persisted to any server.

### 2.4 Secure Column Configuration

- Your selection of private columns is saved inside the Excel workbook's document settings (a standard Office storage mechanism). This data stays with the file on your device; it is not transmitted to ABDK.

---

## 3. Data Sent to OpenAI

When you use the AI chat, the add-in makes API calls directly from your browser to OpenAI's servers. The data included in those calls is:

| Data | Included? |
|------|-----------|
| Values from private columns | **Never** |
| Values from non-private columns | Yes |
| Column headers (non-private) | Yes |
| Chat message text | Yes |
| Your name, email, or Microsoft account details | No |
| Your OpenAI API key (as an authorization header) | Yes (required by OpenAI) |

These requests are governed by [OpenAI's Privacy Policy](https://openai.com/privacy) and [Terms of Use](https://openai.com/terms). ABDK Consulting is not responsible for OpenAI's data handling practices. You are using OpenAI's API under your own account and are subject to their terms.

---

## 4. Data Collected by ABDK Consulting

**ABDK Consulting collects no personal data from users of this add-in.**

- The add-in is a static web application hosted at `confyai.abdk.consulting`. Standard web-server access logs (IP address, timestamp, URL path, user-agent) may be retained for up to 30 days for security and operational purposes. These logs are not linked to your identity or used for any other purpose.
- ABDK does not use cookies, tracking pixels, analytics services, or any third-party telemetry in the add-in.
- ABDK does not receive your spreadsheet data, your chat messages, or your OpenAI API key.

---

## 5. Data Sharing

ABDK Consulting does not sell, rent, or share personal data with third parties. The only external party that receives data when you use the add-in is **OpenAI**, and that data is sent directly from your browser — not via ABDK.

---

## 6. Data Retention and Deletion

Since ABDK Consulting does not collect or store personal data, there is nothing to delete on our side. To remove data stored on your device:

- **API key:** Use the settings panel inside the add-in to remove the stored key, or clear `OfficeRuntime.storage` / `localStorage` manually.
- **Secure column configuration:** Delete the relevant document settings from within Excel, or remove the add-in and re-install it.

For data held by OpenAI (conversation history retained under your OpenAI account), consult OpenAI's data deletion procedures at [https://platform.openai.com/account](https://platform.openai.com/account).

---

## 7. Children's Privacy

This add-in is intended for business and professional use. It is not directed at children under the age of 13 (or the applicable minimum age in your jurisdiction). ABDK Consulting does not knowingly collect data from children.

---

## 8. Security

- All communication between the add-in and external services uses HTTPS (TLS 1.2 or higher).
- Your API key is stored using the platform-provided secure storage mechanism (`OfficeRuntime.storage`), which is isolated per add-in and not accessible by other add-ins or web pages.
- Private column data never leaves your device in connection with AI requests.

---

## 9. Changes to This Policy

If this policy changes materially, the updated version will be published at this URL with a revised effective date. Continued use of the add-in after a change constitutes acceptance of the updated policy.

---

## 10. Contact

For privacy-related questions or concerns, contact:

**ABDK Consulting**
[dmitry@abdkconsulting.com](mailto:dmitry@abdkconsulting.com)
[https://abdk.consulting](https://abdk.consulting)
