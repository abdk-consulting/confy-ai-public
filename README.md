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

> **Note:** Using this add-in requires an [OpenAI account](https://platform.openai.com/) and an active API key. See the cost section below for estimates.

---

## API Cost Estimates

The add-in uses your own OpenAI API key. All charges go directly to your OpenAI account — ABDK Consulting receives nothing. The estimates below are based on **gpt-5.5** pricing ($5 / $0.50 cached / $30 per 1M tokens) measured across a 20-sheet, 830-row test workbook (74 test cases, 135 model turns).

### How the add-in differs from pasting your data directly

The add-in never sends your actual row values to the model. Instead it sends only column headers and inferred schema metadata, generates **synthetic data** locally, runs the analysis on the fake data, then re-executes the resulting code on your real data entirely inside your browser. This keeps sensitive values off OpenAI's servers and also makes cost **flat in row count** — unlike a naive paste-the-sheet approach whose token bill grows one-for-one with your data.

### Cost per conversation turn

| Rows per sheet | Raw data (no add-in) | With add-in | Cheaper option |
|---|---|---|---|
| 40 *(typical small sheet)* | $0.051 | $0.083 | Raw −39% |
| 100 | $0.057 | $0.083 | Raw −31% |
| **≈ 350** | $0.084 | $0.083 | **Break-even** |
| 1,000 | $0.153 | $0.083 | Add-in −46% |
| 5,000 | $0.580 | $0.083 | Add-in −86% |
| 20,000 | $2.18 | $0.083 | Add-in −96% |

The add-in's cost of **≈ $0.083 per turn is essentially flat** regardless of how many rows your sheet has. Sending raw data is cheaper only for very small sheets (under ~350 rows); beyond that break-even point the add-in becomes the less expensive option, and eventually the only feasible one — a single 54k-row sheet would exceed gpt-5.5's context window if sent as raw text.

For a typical interactive session of 5–10 turns, expect **$0.40–$0.85** in API charges.

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

## Terms of Use

See [TERMS.md](TERMS.md) for the full terms of use.

The Add-in is provided **"as is" without warranty of any kind**. You are responsible for reviewing AI-proposed edits before applying them and for correctly marking sensitive columns as private. All OpenAI API charges are your own responsibility.

---

## Support

- Website: [https://abdk.consulting](https://abdk.consulting)
- Email: [dmitry@abdkconsulting.com](mailto:dmitry@abdkconsulting.com)

---

## Publisher

**ABDK Consulting**
Registered in Estonia
[https://abdk.consulting](https://abdk.consulting)
