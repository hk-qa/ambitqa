# QA Nexus 🎯

> **A RAG-powered QA assistant grounded in ISTQB Foundation Level, IEEE 829, and the Software Testing Life Cycle (STLC).**

Built as a capstone project for the [Codecademy Agentic AI Applications Bootcamp](https://www.codecademy.com) — Contest #1.

![Version](https://img.shields.io/badge/version-v1.2.0-6c63ff)
![License](https://img.shields.io/badge/license-All%20Rights%20Reserved-red)
![Hosted on](https://img.shields.io/badge/hosted%20on-GitHub%20Pages-222)

🔗 **Live demo:** [hk-qa.github.io/qa-nexus/](https://hk-qa.github.io/qa-nexus/)
🤖 **Chatbot:** [hk-qa.github.io/qa-nexus/chatbot.html](https://hk-qa.github.io/qa-nexus/chatbot.html)
🔬 **Evaluator:** [hk-qa.github.io/qa-nexus/evaluator.html](https://hk-qa.github.io/qa-nexus/evaluator.html)

---
## 🤝 Hire Me

**Need QA work done faster, with documentation that passes any audit?**

I use **QA Nexus** as my personal force-multiplier to deliver senior-grade QA artifacts in a fraction of the typical time — grounded in ISTQB Foundation Level, IEEE 829, and modern STLC practices. Available for short engagements and ongoing retainers.

### What I can do for your team

| Engagement | Typical Outcome | Investment |
|---|---|---|
| **IEEE 829 Compliance Refresh** | Audit your existing QA documentation, generate compliant test plans, RTMs, and exit criteria | Fixed-fee, ~2 weeks |
| **Test Automation Framework Setup** | Scaffold Playwright, Cypress, or Selenium with Page Object Model and CI workflow, using your real HTML for working selectors | Fixed-fee, ~3-4 weeks |
| **QA Process Maturity Assessment** | Score your current QA artifacts against rubric-based standards, deliver a prioritized improvement roadmap | Fixed-fee, ~1 week |
| **Bug Triage & Severity Scoring** | Ongoing defect analysis with IEEE 829 bug reports and reproducibility validation | Monthly retainer |
| **API / Security / Performance Test Design** | Generate full test suites and execution plans across REST, GraphQL, OWASP Top 10, k6/JMeter | Per-project |
| **Custom QA Tooling** | Build internal QA tools tailored to your stack and workflow | Quoted on scope |

### Why work with me

- ✅ **Real QA practitioner**, not a generalist consultant — I've designed and shipped test strategies for production systems
- ✅ **Tool-augmented delivery** — what would take a junior QA 2 weeks, I deliver in 3 days with higher quality
- ✅ **Methodology-grounded output** — every artifact references ISTQB / IEEE 829 sources, audit-ready by default
- ✅ **Transparent scoping** — fixed fees on defined deliverables, no surprises
- ✅ **Code stays yours** — all artifacts and frameworks are delivered as your property

### Get in touch

- 💼 **LinkedIn:** https://www.linkedin.com/in/hkapur
- 📧 **Email:** hk.qanexus@gmail.com
- 📅 **Book a 30-minute intro call:** [https://calendly.com/hk.qanexus](https://calendly.com/hk-qanexus)

> _Currently accepting up to 2 new engagements per month. Best fit: startups and mid-size teams needing senior QA capacity without a full-time hire._

---

## 🌟 What it does

QA Nexus is a structured, retrieval-augmented chat agent that produces production-grade QA deliverables in seconds — not generic AI chat output. Every response is grounded in a curated methodology knowledge base and cites the exact sources used.

### 14+ deliverable types
- **Test plans** (IEEE 829 format)
- **Test cases** — tabular and BDD/Gherkin
- **Bug reports** — full IEEE 829 defect structure
- **Requirements Traceability Matrices (RTM)**
- **Test execution summary reports**
- **Exit criteria checklists**
- **Lessons-learned documents**
- **Automation framework code** — Playwright (TypeScript), Cypress (JavaScript), Selenium WebDriver (Python + pytest), and BDD/Cucumber + Gherkin
- **API test cases** — REST, GraphQL, contract tests
- **Security test cases** — OWASP Top 10 coverage
- **Performance test plans and scripts** — k6, JMeter, load/stress/spike/soak
- Plus risk-based strategies, accessibility checklists, exploratory test charters, and more

---

## ✨ Key features

### 🧠 Real RAG, not just a wrapper
- Curated knowledge base with 38 methodology chunks (ISTQB, IEEE 829, STLC, automation, API, security, performance testing patterns)
- Semantic keyword scoring + mode-aware retrieval boost
- Top-K relevant chunks injected into every prompt
- **Source citations on every response** — audit exactly which methodology was used

### 🌐 Multi-provider LLM support
Choose your AI provider directly in the nav bar — no code changes required:

| Provider | Models included |
|---|---|
| **Anthropic** | Claude Sonnet 4.6, Opus 4.6/4.7/4.8, Haiku 4.5 |
| **Google** | Gemini 2.0 Flash, 1.5 Pro, 1.5 Flash |
| **xAI** | Grok 3, Grok 3 Mini, Grok 2 |
| **OpenAI** | GPT-4o, GPT-4o Mini, o1, o3-mini |
| **OpenRouter** | Any model via a single key |
| **Custom** | Any OpenAI-compatible endpoint + model |

Pick **Custom…** from either dropdown to type any model string — future-proof for new releases without code updates. Each provider's API key is stored separately in localStorage and never transmitted anywhere except that provider's API.

### 🎯 Target real applications
- Set a target URL → agent fetches the page via CORS proxy
- Extracts forms, buttons, navigation, and structure from the HTML
- Generates **site-specific deliverables** referencing actual UI elements

### 📎 Multi-modal attachments
Three attachment paths to give the agent maximum context:
- **Screenshots** (PNG/JPG/WEBP/GIF) — vision capability sees the UI directly
- **PDFs** — native PDF understanding (Anthropic provider)
- **HTML files** — DOM structure extracted and injected for real, working selectors in automation code

Attach via 📎 button, drag-and-drop, or paste from clipboard.

### ⏹ Stop generation
A red stop button appears next to the chat input while the AI is generating. Click it to cancel the in-flight request immediately — no page refresh needed.

### 🔬 QA Artifact Evaluator
A standalone scoring tool (`evaluator.html`) that evaluates any QA Nexus output against ISTQB/IEEE 829 rubrics:

- **PASS / WARN / FAIL** verdict with weighted score (0–100)
- **Per-dimension score bars** with explanatory notes
- **Top issues** list
- **Auto-generated improvement prompt** — paste it back into QA Nexus to fix the weaknesses
- **Pre-scan red flag detection** — catches vague steps, hardcoded waits, placeholder selectors, unmeasurable criteria before the AI evaluates
- **Light / dark mode** with system preference detection
- Supports all 9 deliverable types: Test Plan, Test Cases, BDD/Gherkin, Bug Report, Automation Code, RTM, Execution Report, Exit Criteria, Lessons Learned

### 🎭 11 STLC modes
| Mode | Focus |
|---|---|
| Requirements Review | Testability analysis, RTM, acceptance criteria |
| Test Planning | IEEE 829 test plans, risk analysis, entry/exit criteria |
| Test Design | Test cases, BDD/Gherkin, boundary value analysis |
| Test Implementation | Test data, environment setup, traceability |
| Test Execution | Bug reports, execution reports, defect tracking |
| Test Closure | Lessons learned, metrics, sign-off |
| Test Automation | Playwright, Cypress, Selenium, BDD/Cucumber code |
| **API Testing** | REST/GraphQL test cases, Postman collections, JWT/OAuth |
| **Security Testing** | OWASP Top 10, XSS/injection/IDOR, Burp Suite/ZAP plans |
| **Performance Testing** | k6 scripts, JMeter plans, SLA definitions |
| General | Open-ended QA questions |

### 📤 Five export formats
- **TXT** — clean plain text
- **MD** — raw markdown
- **HTML** — standalone styled document
- **Jira CSV** — direct-importable for test cases and bug reports
- **Auto-form fill** — structured input modal when the agent needs specific data
- **🔬 Evaluate** — one-click evaluation of any response in the evaluator

### 🎨 Polished UI
- Three-column resizable layout with drag handles
- Both side panels collapse for full-screen chat
- Light & dark mode (system preference detection)
- Indigo/violet brand palette, WCAG AAA text contrast
- Mode-aware autosuggestions (↑↓ navigation, Enter to pick)
- Version badge in nav — always know what's live

---

## 🏗 Architecture

**Pure browser-based** — no backend, no database, no server-side code, no build step.

```
┌──────────────────────────────────────────────────────────────────┐
│  Browser (the entire app)                                         │
│                                                                    │
│  ┌──────────────────┐   ┌──────────────────┐                     │
│  │ Knowledge base   │   │ STLC mode        │                     │
│  │ (38 chunks)      │   │ (11 phases)      │                     │
│  └────────┬─────────┘   └────────┬─────────┘                     │
│           │                       │                               │
│           ▼                       ▼                               │
│  ┌──────────────────────────────────────────┐                    │
│  │ Semantic retrieval (top-K + mode boost)   │                    │
│  └─────────────────────┬────────────────────┘                    │
│                         │                                         │
│                         ▼                                         │
│  ┌──────────────────────────────────────────┐                    │
│  │ Prompt builder + multi-modal content     │                    │
│  │ (text + images + PDFs + HTML context)    │                    │
│  └─────────────────────┬────────────────────┘                    │
│                         │                                         │
│                         ▼                                         │
│         Provider-agnostic API layer                               │
│  ┌──────────┬──────────┬──────────┬──────────┬─────────┐        │
│  │Anthropic │ Google   │  xAI     │ OpenAI   │ Custom  │        │
│  └──────────┴──────────┴──────────┴──────────┴─────────┘        │
│                         │                                         │
│                         ▼                                         │
│  ┌──────────────────────────────────────────┐                    │
│  │ Markdown renderer + export pipeline       │                    │
│  │ TXT · MD · HTML · Jira CSV · Evaluate    │                    │
│  └──────────────────────────────────────────┘                    │
└──────────────────────────────────────────────────────────────────┘
```

---

## 🚀 How to use

### Chatbot
1. Visit the **[chatbot](https://hk-qa.github.io/qa-nexus/chatbot.html)**
2. Select your **Provider** and **Model** in the top-right nav
3. Click **🔑 Add key** and enter your API key for the selected provider
4. **Pick an STLC mode** from the left panel
5. **(Optional)** Set a target URL in the right panel for site-specific deliverables
6. **(Optional)** Attach screenshots, PDFs, or HTML files for context
7. Use a **quick action** or type your prompt
8. **Export** as TXT, MD, HTML, or Jira CSV — or click **🔬 Evaluate** to score the output

### Evaluator
1. Visit the **[evaluator](https://hk-qa.github.io/qa-nexus/evaluator.html)**
2. Enter your **Anthropic API key**
3. Select the **deliverable type** (or leave on Auto-detect)
4. Paste any QA artifact — or click **🔬 Evaluate** from the chatbot to pre-load it
5. Click **Evaluate Artifact** (or Ctrl+Enter)
6. Review the PASS/WARN/FAIL verdict, dimension scores, and improvement prompt

### API keys by provider
| Provider | Get a key at |
|---|---|
| Anthropic | [console.anthropic.com](https://console.anthropic.com) |
| Google | [aistudio.google.com](https://aistudio.google.com/app/apikey) |
| xAI | [console.x.ai](https://console.x.ai) |
| OpenAI | [platform.openai.com](https://platform.openai.com/api-keys) |
| OpenRouter | [openrouter.ai/keys](https://openrouter.ai/keys) |

---

## 🔐 Privacy & security

- API keys are **stored in your browser's localStorage only** — never sent to any server other than the selected provider's API endpoint
- No analytics, no tracking, no cookies
- Anthropic calls use the `anthropic-dangerous-direct-browser-access` header (explicit opt-in for direct browser-to-API)
- Code is fully open-source — audit it yourself

**Recommendation:** Set a per-key spending cap at your provider's billing console for any keys used in browser-based tools.

---

## 📚 Knowledge base coverage

| Source | Topics |
|---|---|
| **ISTQB Foundation Level** | Test design techniques (EP, BVA, decision tables, state transition), severity/priority |
| **IEEE 829** | Test plan, test case, defect report, RTM templates |
| **STLC** | All phases (Requirements Review → Test Closure) |
| **BDD / Gherkin** | Scenario writing, Given/When/Then patterns |
| **Agile QA** | Shift-left testing, Definition of Done |
| **Automation** | Playwright, Cypress, Selenium, BDD/Cucumber, Page Object Model |
| **API Testing** | REST fundamentals, GraphQL, Postman/Newman, contract testing, JWT/OAuth |
| **Security Testing** | OWASP Top 10, injection/XSS, IDOR, session security, DAST/SAST tools |
| **Performance Testing** | Load/stress/spike/soak types, k6, JMeter, SLA metrics, APM |

---

## 🛠 Tech stack

- **AI:** Multi-provider (Anthropic Claude, Google Gemini, xAI Grok, OpenAI GPT, OpenRouter, Custom)
- **Frontend:** Vanilla HTML / CSS / JavaScript — no framework, no build step, zero npm dependencies
- **Fonts:** Outfit (display), Space Grotesk (headers), Inter (body)
- **Hosting:** GitHub Pages
- **No backend · No database · No server · No build pipeline**

---

## 🎓 Capstone context

Built as a capstone project for the **[Codecademy Agentic AI Applications Bootcamp](https://www.codecademy.com)** — Contest #1.

Demonstrates:
- ✅ Retrieval-Augmented Generation (RAG) with semantic scoring
- ✅ Multi-modal input (text, image, PDF, HTML)
- ✅ Multi-provider LLM abstraction layer
- ✅ Transparent source attribution
- ✅ Domain-specific tooling (QA methodology)
- ✅ AI output quality evaluation (rubric-based scoring)
- ✅ Real-world deliverable generation (not just chat)
- ✅ Polished UX (theme toggle, resizable panels, autosuggest, exports, stop button)
- ✅ Honest AI design (labels inferred vs. confirmed selectors in automation code)

---

## 🐞 Known limitations

- **PDF attachments** — native PDF blocks only work with Anthropic provider; other providers receive text context only
- **CORS-blocked sites** — page fetch falls back to URL + description mode (workaround: attach HTML file or screenshot)
- **Evaluator token limit** — artifacts over ~24,000 characters are trimmed; evaluate in parts for very large documents
- **No conversation persistence** — refreshing clears history (intentional for privacy)
- **Custom provider** — must expose an OpenAI-compatible `/v1/chat/completions` endpoint

---

## 🗂 Repository structure

```
qa-nexus/
├── index.html          # Landing page
├── chatbot.html        # Main QA assistant chatbot
├── evaluator.html      # QA artifact evaluator
├── LICENSE             # All Rights Reserved
└── README.md           # This file
```

---

## 📄 License

**Copyright © 2026 Hitesh Kapur. All rights reserved.**

This code is published for **portfolio demonstration and educational reference**.

**You may:**
- ✅ View, read, and study the source code
- ✅ Reference patterns or approaches in your own original work
- ✅ Use the live demo with your own API key
- ✅ Share links to this repository and the live site

**You may NOT:**
- ❌ Copy, redistribute, or republish this code or any substantial portion
- ❌ Deploy this code (in whole or in part) to any public or commercial service
- ❌ Use this code in any commercial product or paid offering
- ❌ Remove attribution or claim authorship

For licensing inquiries, contact via LinkedIn (linked below).

> The methodology knowledge base references (ISTQB Foundation Level concepts, IEEE 829 templates, STLC definitions) are based on publicly available industry standards and are not claimed as original works.

---

## 🙏 Acknowledgments

- **[Codecademy](https://www.codecademy.com)** for the Agentic AI Applications Bootcamp
- **[Anthropic](https://www.anthropic.com)** for Claude and the multi-modal Messages API
- The ISTQB and IEEE communities for the methodology foundations this tool is built on

---

## 📱 Connect

Built by **Hitesh Kapur** — find me on [LinkedIn](https://www.linkedin.com/in/hkapur) · #CodecademyAgenticAIBootcamp
