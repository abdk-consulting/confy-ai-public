# ABDK Confy AI — Excel Add-in

**Analyze and modify your spreadsheets using AI, without exposing sensitive data to the AI provider.**

ABDK Confy AI is a Microsoft Excel task-pane add-in developed by [ABDK Consulting](https://abdk.consulting). It lets you have a natural-language conversation with an AI assistant about the contents of your spreadsheet — asking questions, requesting calculations, generating synthetic data, and making edits — while keeping columns you designate as private completely hidden from the AI.

---

## Key Features

### Privacy-first AI analysis
Before any data leaves your device, you choose which columns contain sensitive information. Those columns are redacted and are never included in any request sent to the AI provider. Only the non-sensitive parts of your spreadsheet are shared.

### Natural-language chat
Ask questions about your data in plain English. The AI can answer questions, perform analysis, summarise trends, and explain patterns it finds in the visible data.

### AI-driven spreadsheet editing
Instruct the AI to add rows, fill in missing values, generate synthetic data, or apply transformations. Changes are previewed and applied directly to your open workbook.

### Secure column marking
Columns you mark as private are visually highlighted inside Excel so you always know what is protected. Your selection is saved with the document and restored automatically the next time you open it.

### Your own API key — your data, your account
The add-in uses your personal OpenAI API key, which you enter once and is stored only on your device. ABDK Consulting never sees your key, your data, or your AI usage. Calls go directly from your browser to OpenAI; no data passes through ABDK servers.

> **Note:** Using this add-in requires an [OpenAI account](https://platform.openai.com/) and an active API key. OpenAI charges apply based on your usage according to their pricing.

---

## Installation

1. Download `manifest.xml` from this repository.
2. Open a spreadsheet in [Excel on the web](https://excel.cloud.microsoft/).
3. Go to **Insert → Add-ins → More Add-ins → Upload My Add-in**.
4. Select the downloaded `manifest.xml`.
5. The **ABDK Confy AI** button will appear on the **Home** tab.

---

## How It Works (User Perspective)

1. **First launch** — A welcome screen prompts you to select which columns hold sensitive data.
2. **Column picker** — A dialog lists all columns in your workbook. Tick the ones you want to keep private.
3. **Chat** — Type your question or instruction. The AI receives only the non-private data and responds in the chat panel.
4. **Apply changes** — If the AI proposes edits to the spreadsheet, a confirmation step lets you review and accept them before anything is written.
5. **Change protected columns at any time** — Use the settings menu inside the add-in to update your private column selection.

---

## Privacy

See [PRIVACY.md](PRIVACY.md) for the full privacy policy.

In summary: ABDK Consulting collects no personal data whatsoever. Your spreadsheet data is sent only to OpenAI's API (the columns you chose to protect are never sent anywhere). Your API key is stored locally on your device only.

---

## Support

- Website: [https://abdk.consulting](https://abdk.consulting)
- Email: [dmitry@abdkconsulting.com](mailto:dmitry@abdkconsulting.com)

---

## Publisher

**ABDK Consulting**
Registered in Estonia
[https://abdk.consulting](https://abdk.consulting)
