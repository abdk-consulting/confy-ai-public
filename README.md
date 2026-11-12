# ABDK Confy AI — Excel Add-in

**Analyze and modify your spreadsheets using AI, without exposing sensitive data to the AI provider.**

ABDK Confy AI is a Microsoft Excel task-pane add-in developed by [ABDK Consulting](https://abdk.consulting). It lets you have a natural-language conversation with an AI assistant about the contents of your spreadsheet — asking questions, requesting calculations, generating synthetic data, and making edits — while keeping the values of columns you designate as private hidden from the AI.

---

## Key Features

### Privacy-first AI analysis
Before any data leaves your device, you choose which columns contain sensitive information. The values of those columns are redacted and are never included in any request sent to the AI provider. Only their headers and data types, and the non-sensitive parts of your spreadsheet are shared.

### Natural-language chat
Ask questions about your data in plain English. The AI can answer questions, perform analysis, summarise trends, and explain patterns it finds in the visible data.

### AI-driven spreadsheet editing
Instruct the AI to add rows, fill in missing values, generate synthetic data, or apply transformations. Changes are previewed and applied directly to your open workbook.

### Secure column marking
Columns you mark as private are visually highlighted inside Excel so you always know what is protected. Your selection is saved with the document and restored automatically the next time you open it.

### Free trial, no sign-up
Start at once without an AI provider account. ABDK Consulting pays for a limited daily amount of AI use. Requests go directly from your browser to OpenRouter and then to Microsoft Azure, with zero data retention at Azure; no data passes through ABDK servers. ABDK sees how much the free key is used, but not what is sent with it. The free trial may change or end at any time.

### Your own API key: your data, your account
The add-in can also run on your own AI provider account. You pick a provider and model, enter that provider's API key once, and the key is stored only on your device. ABDK Consulting never sees your key, your data, or your AI usage. Calls go directly from your browser to the provider you chose; no data passes through ABDK servers.

### Choice of AI provider

| Provider | Where to get an API key |
|---|---|
| OpenAI | [platform.openai.com/api-keys](https://platform.openai.com/api-keys) |
| Anthropic (Claude) | [console.anthropic.com/settings/keys](https://console.anthropic.com/settings/keys) |
| Google Gemini | [aistudio.google.com/apikey](https://aistudio.google.com/apikey) |
| OpenRouter | [openrouter.ai/keys](https://openrouter.ai/keys) |
| Any OpenAI-compatible endpoint | Supply your own base URL and model — Groq, Mistral, xAI, DeepSeek, vLLM, Ollama, and similar |

Each provider offers a list of suggested models, and you can always type in a model name the list doesn't carry yet. Switch provider, key or model at any time from the settings menu inside the add-in.

> **Note:** Beyond the free trial, using this add-in requires an account with one of the providers above and an active API key. See the cost section below for estimates.

**Anyone can use this add-in as an individual.** The free trial needs no sign-up. Every provider above offers self-service sign-up, and the add-in's setup screen links straight to the page where a new user registers and creates a key. There is no ABDK account or sign-in, and no enterprise agreement, administrator provisioning, or organisational licence is required.

---

## API Cost Estimates

All charges go directly to your account with whichever provider you chose — ABDK Consulting receives nothing. The estimates below were measured on **OpenAI gpt-5.5** ($5 / $0.50 cached / $30 per 1M tokens) across a 20-sheet, 830-row test workbook (74 test cases, 135 model turns). Absolute figures move with the provider and model you pick; the shape of the curve — flat in row count — does not, because it follows from how the add-in works rather than from who serves the model.

### How the add-in differs from pasting your data directly

The add-in never sends your actual row values to the model. Instead it sends only column headers and inferred schema metadata, generates **synthetic data** locally, runs the analysis on the fake data, then re-executes the resulting code on your real data entirely inside your browser. This keeps sensitive values off the provider's servers and also makes cost **flat in row count** — unlike a naive paste-the-sheet approach whose token bill grows one-for-one with your data.

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

1. **First launch**: A setup screen offers the free trial, or lets you choose an AI provider, enter its API key, and pick a model. Each provider links to the page where a new user can get a key.
2. **Welcome screen**: Prompts you to select which columns hold sensitive data.
3. **Column picker**: A dialog lists all columns in your workbook. Tick the ones you want to keep private.
4. **Chat**: Type your question or instruction. The AI receives only the non-private data and the headers and data types of private columns, and responds in the chat panel.
5. **Apply changes**: If the AI proposes edits to the spreadsheet, a confirmation step lets you review and accept them before anything is written.
6. **Change anything at any time**: The settings menu updates your private column selection, switches between the free trial and your own key, provider or model, and signs you out by removing the stored key.

---

## Privacy

See [PRIVACY.md](PRIVACY.md) for the full privacy policy.

In summary: your spreadsheet data is sent only to the AI service (the values of the columns you chose to protect are never sent anywhere, only their headers and data types) and never passes through ABDK servers. Your own API key is stored locally on your device only. ABDK keeps a web server access log, and for the free trial it records the IP address and request headers of each request for a free key, to prevent abuse. Both are kept for 1 year.

---

## Terms of Use

See [TERMS.md](TERMS.md) for the full terms of use.

The Add-in is provided **"as is" without warranty of any kind**. You are responsible for reviewing AI-proposed edits before applying them and for correctly marking sensitive columns as private. All AI provider charges are your own responsibility, except free trial use, which ABDK Consulting pays for. The free trial has a daily limit and may change or end at any time.

---

## Support

- Website: [https://abdk.consulting](https://abdk.consulting)
- Email: [dmitry@abdkconsulting.com](mailto:dmitry@abdkconsulting.com)

---

## Publisher

**ABDK Consulting**
Registered in Estonia
[https://abdk.consulting](https://abdk.consulting)
