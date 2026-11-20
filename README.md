<img src="./assets/argus-cover.svg" alt="ARGUS. See beyond numbers. Financial intelligence, explained." width="100%" />

<p align="center">
  <a href="#the-product">The product</a> &nbsp; · &nbsp;
  <a href="#engineering-decisions">Engineering decisions</a> &nbsp; · &nbsp;
  <a href="#technical-evaluation">Technical evaluation</a>
</p>

## The product

**ARGUS: An AI-Powered Financial Intelligence Platform**

Financial applications should do more than collect numbers. ARGUS connects the
financial record with understandable context: what changed, which budget needs
attention, and where eligible spending happened.

Built with **React Native, TypeScript, Node.js and PostgreSQL**.

### A record you can understand

Income and expense management, searchable transaction history, editable details,
category budgets, financial summaries and analytics.

### Capture without giving up control

Android notification acquisition and receipt OCR prepare editable evidence.
The review flow lets the user correct information before confirmation. Payment
correlation is conservative: corroborating reports must not become extra expenses.
SMS acquisition relies on Android messaging notifications, not SMS database access.

### Financial Journey

Location-backed expenses on a geographic map, with user correction and deletion.
Month in Motion replays eligible completed-month expenses using reconstructed
road routes where available. These are **not actual GPS travel histories**.

### Explanations, not invented certainty

Ask ARGUS, budget warnings, recommendations and reminders use confirmed ledger
information with deterministic fallback. ARGUS does not train its own LLM, and
guidance is informational rather than a guaranteed financial outcome.

## Engineering decisions

| Decision                                             | Why it matters                                                          |
| :--------------------------------------------------- | :---------------------------------------------------------------------- |
| Server-authoritative, owner-scoped financial records | One user's data must never become another user's context.               |
| Decimal-safe financial values and explicit currency  | Financial totals need predictable, auditable calculation.               |
| Rotating refresh sessions and native secure storage  | Authentication is more than a successful login screen.                  |
| Preserved notification event context                 | A later review location must not replace the event's original evidence. |
| Opt-in location with unavailable states              | Missing evidence should stay missing, never become a fabricated point.  |
| Provider boundaries and honest fallback              | External services can change without changing financial truth.          |
| Explicit errors, retry paths and save feedback       | Users need to know whether an action actually persisted.                |

## Project status

This is a development project with automated tests, database/bootstrap validation
and Android emulator acceptance evidence. Physical-device and production-release
acceptance are separate gates, not implied by a successful build.

The application is not a fully offline or publicly hosted service. Its normal
financial features require the API and database. Phone OTP is frozen for the
current review UI. iOS cannot provide general cross-app notification listening.

## Technical evaluation

The full source repository is intentionally private. This repository is a public
product and engineering overview, not an open-source distribution or an APK download.

**Source review and a guided walkthrough are available to potential employers on request.**

[Get in touch on LinkedIn](https://www.linkedin.com/in/gurusundaragunalan-m/)
&nbsp; · &nbsp; [Explore Guru's other projects](https://github.com/guru-six3)

Do not post financial information, credentials or personal contact details in
public issues. Access to private source is granted individually, not automatically.
