# Terms of Use: ABDK Confy AI

**Effective date:** 2026-11-12
**Publisher:** ABDK Consulting, Estonia
**Contact:** [dmitry@abdkconsulting.com](mailto:dmitry@abdkconsulting.com)

---

## 1. Acceptance

By installing or using the ABDK Confy AI Microsoft Excel add-in ("the Add-in"), you agree to these Terms of Use. If you do not agree, do not install or use the Add-in.

---

## 2. Description of the Service

The Add-in is a Microsoft Excel task-pane add-in that enables natural-language interaction with spreadsheet data via a third-party AI model. It allows you to:

- Ask questions about the content of your spreadsheet.
- Request edits, transformations, or synthetic data generation.
- Designate specific columns as private so their values are excluded from all AI requests. The headers and data types of private columns are still sent.

The Add-in sends the non-private portions of your spreadsheet and your chat messages to an AI service: either the API of an AI provider you select, using an API key you supply, or the free trial described in section 4. It reads and writes data in your open Excel workbook in response to AI-generated instructions that you review and accept.

The Add-in is available to individual users on a self-service basis. There is no ABDK account or sign-in, and no enterprise agreement or administrator provisioning is required. You need either the free trial or your own account with one of the AI providers listed in section 3.1, each of which registers new individual users directly.

---

## 3. Third-Party Services

### 3.1 AI Providers

When you use your own API key, the Add-in relies on a third-party AI provider that you select. Supported providers are OpenAI, Anthropic, Google Gemini, OpenRouter, and any OpenAI-compatible endpoint whose address you supply yourself. You must have a valid account and API key with the provider you choose, and your use of that provider's services is governed solely by its own terms and privacy policy, for example [OpenAI](https://openai.com/policies/terms-of-use), [Anthropic](https://www.anthropic.com/legal/commercial-terms), [Google](https://ai.google.dev/gemini-api/terms), or [OpenRouter](https://openrouter.ai/terms). ABDK Consulting has no control over any provider's services, availability, pricing, or data handling, and does not endorse or warrant any of them.

Where you point the Add-in at an OpenAI-compatible endpoint of your own choosing, you are solely responsible for that endpoint and for any handling of data it receives.

### 3.2 Microsoft Excel and Office

The Add-in runs inside Microsoft Excel. Your use of Excel and related Microsoft services is governed by Microsoft's terms. ABDK Consulting is not affiliated with Microsoft and is solely responsible for the Add-in itself.

---

## 4. Free Trial

### 4.1 What It Is

The free trial lets you use the Add-in without your own AI provider account. ABDK Consulting pays for a limited amount of AI use. When you choose the free trial, the Add-in gets a key from ABDK's server for ABDK's account with [OpenRouter](https://openrouter.ai), and your requests are processed by OpenRouter and Microsoft Azure. The [Privacy Policy](PRIVACY.md) describes what data this involves.

### 4.2 Conditions

- The free trial is provided free of charge, as a courtesy, with no service level of any kind.
- Each free key has a daily usage limit, and all free keys together share a daily limit. When a limit is reached, the free trial stops working until the limits reset.
- ABDK Consulting chooses the AI model used in the free trial and may change it at any time.
- ABDK Consulting may change, limit, suspend, or end the free trial at any time, for one user or for everyone, without notice.
- ABDK Consulting may disable any free key that it believes is being abused.

### 4.3 Rules for the Free Trial

You must not:

- Request free keys by automated means, or try to get around the CAPTCHA or the limits.
- Collect more than one free key for yourself, for example by switching networks.
- Extract a free key from the Add-in, or use it outside the Add-in, or share it with others.
- Use the free trial in a way that violates the [OpenRouter terms](https://openrouter.ai/terms) or the usage policies of the provider of the AI model. Free trial requests are sent under ABDK's account, so ABDK is responsible to these providers for them.

---

## 5. Your Responsibilities

You are responsible for:

- Unless you use the free trial: obtaining and maintaining a valid API key with your chosen AI provider at your own cost. All API charges billed by that provider are your sole responsibility.
- Ensuring you have the right to process the spreadsheet data you use with the Add-in, including any data belonging to third parties.
- Reviewing AI-proposed changes before applying them to your workbook. The Add-in presents changes for your approval; you are responsible for any edits you accept.
- Correctly identifying which columns contain sensitive data and marking them as private before initiating an AI chat session. ABDK Consulting cannot verify or guarantee that your private column selection is complete or correct.
- Keeping sensitive information out of column headers, since the headers of private columns are sent to the AI service.
- Complying with all applicable laws and regulations in connection with your use of the Add-in, including data protection laws governing any personal data present in your spreadsheets.

---

## 6. Acceptable Use

You must not use the Add-in to:

- Process data in violation of applicable law, including data protection and privacy regulations.
- Transmit or process data that you do not have the right to use.
- Attempt to reverse-engineer, decompile, or extract the source code of the Add-in beyond what is made available in the public repository at [https://github.com/abdk-consulting/confy-ai-public](https://github.com/abdk-consulting/confy-ai-public).
- Use the Add-in in a manner that violates your AI provider's usage policies or Microsoft's platform policies.

The free trial has additional rules in section 4.3.

---

## 7. No Warranty

**THE ADD-IN, INCLUDING THE FREE TRIAL, IS PROVIDED "AS IS" AND "AS AVAILABLE", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED.**

To the fullest extent permitted by applicable law, ABDK Consulting disclaims all warranties, including but not limited to:

- Warranties of merchantability, fitness for a particular purpose, and non-infringement.
- Any warranty that the Add-in will be uninterrupted, error-free, or free of harmful components.
- Any warranty that the free trial will be available at any given time or for any given period.
- Any warranty regarding the accuracy, completeness, or reliability of AI-generated outputs or edits applied to your workbook.
- Any warranty that private column protection will prevent disclosure in all circumstances, including cases where data appears in non-private columns, column headers, or chat messages you compose.

**You assume all risk arising from your use of the Add-in and from any reliance on AI-generated content or edits.**

---

## 8. Limitation of Liability

To the fullest extent permitted by applicable law, ABDK Consulting and its officers, employees, and contractors shall not be liable for any:

- Loss of data, including loss of spreadsheet contents caused by AI-generated edits you accepted.
- Financial loss arising from incorrect AI-generated analysis or data.
- Unintended disclosure of sensitive data resulting from incorrect private column configuration by the user.
- Indirect, incidental, special, consequential, or punitive damages, however caused and regardless of the theory of liability.
- Damages arising from the unavailability or modification of any AI provider's API, of the free trial, or of Microsoft's platform.

In jurisdictions that do not allow the exclusion of certain warranties or the limitation of certain damages, the above exclusions and limitations apply to the maximum extent permitted by law.

---

## 9. Intellectual Property

The Add-in, including its source code (to the extent disclosed in the public repository), documentation, and branding, is owned by ABDK Consulting and protected by applicable intellectual property law. Nothing in these Terms grants you any rights in ABDK Consulting's intellectual property beyond the right to use the Add-in as described herein.

---

## 10. Modifications to the Add-in and These Terms

ABDK Consulting reserves the right to modify, suspend, or discontinue the Add-in at any time without notice. These Terms may be updated from time to time; the current version will always be available at this URL with a revised effective date. Continued use after a change constitutes acceptance of the updated Terms.

---

## 11. Governing Law

These Terms are governed by the laws of Estonia, without regard to conflict-of-law principles. Any dispute arising from these Terms or your use of the Add-in shall be subject to the exclusive jurisdiction of the courts of Estonia, unless mandatory local law requires otherwise.

---

## 12. Contact

**ABDK Consulting**
[dmitry@abdkconsulting.com](mailto:dmitry@abdkconsulting.com)
[https://abdk.consulting](https://abdk.consulting)
