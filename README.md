# QA Nexus 🎯

> **A RAG-powered QA assistant grounded in ISTQB Foundation Level, IEEE 829, and the Software Testing Life Cycle (STLC).**

Built as a capstone project for the [Codecademy Agentic AI Applications Bootcamp](https://www.codecademy.com) — Contest #1.

🔗 **Live demo:** [hk-qa.github.io/qa-nexus/](https://hk-qa.github.io/qa-nexus/)
🤖 **Chatbot:** [hk-qa.github.io/qa-nexus/chatbot.html](https://hk-qa.github.io/qa-nexus/chatbot.html)

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
- Plus risk-based strategies, accessibility checklists, exploratory test charters, and more

---

## ✨ Key features

### 🧠 Real RAG, not just a wrapper
- Curated knowledge base with 23 methodology chunks (ISTQB, IEEE 829, STLC, automation patterns)
- Semantic keyword scoring + mode-aware retrieval boost
- Top-K relevant chunks injected into every prompt
- **Source citations on every response** — you can audit exactly which methodology was used

### 🎯 Target real applications
- Set a target URL → agent fetches the page via CORS proxy
- Extracts forms, buttons, navigation, and structure from the HTML
- Generates **site-specific deliverables** referencing actual UI elements

### 📎 Multi-modal attachments
Three attachment paths to give the agent maximum context:
- **Screenshots** (PNG/JPG/WEBP/GIF) — Claude's vision capability sees the UI directly
- **PDFs** — native PDF understanding
- **HTML files** — DOM structure extracted and injected for **real, working selectors in automation code**

Attach via 📎 button, drag-and-drop, or paste from clipboard.

### 🤖 Test Automation mode
A dedicated STLC phase that generates production-ready code:
- Playwright POM + tests + `playwright.config.ts` + README
- Cypress POM + spec files
- Selenium WebDriver framework (Python + pytest)
- BDD Gherkin features + Cucumber.js step definitions
- GitHub Actions CI workflow
- **Honest about selector sources** — comments tell you whether selectors came from real HTML or were inferred from screenshots

### 📤 Five export formats
- **TXT** — clean plain text (markdown stripped, tables formatted as records)
- **MD** — raw markdown (great for GitHub, Notion, Obsidian)
- **HTML** — standalone styled document (one click away from PDF via browser print)
- **Jira CSV** — direct-importable for test cases and bug reports
- **Auto-form fill** — when the agent asks for structured input, a modal opens with proper input fields

### 🎨 Polished UI
- Three-column resizable layout with drag handles
- Both side panels can collapse for full-screen chat
- Light & dark mode (defaults to system preference)
- Indigo/violet brand palette
- WCAG AAA-compliant text contrast
- Mode-aware autosuggestions in the chat box (↑↓ navigation, Enter to pick)
- Keyboard-friendly throughout

---

## 🏗 Architecture

**Pure browser-based** — no backend, no database, no server-side code.

- Static HTML + vanilla JS + CSS
- Hosted on GitHub Pages
- Calls Anthropic's `claude-sonnet-4-6` directly via the Messages API
- API key is entered in-browser and never stored or transmitted to any third party
- Multi-modal request format (images, PDFs as binary; HTML as extracted text context)
- Streaming-free synchronous request/response with `max_tokens: 16000` + truncation detection + continue button

```
┌──────────────────────────────────────────────────────────────┐
│  Browser (the entire app)                                     │
│                                                                │
│  ┌──────────────────┐   ┌─────────────────┐                  │
│  │ Knowledge base   │   │ STLC mode       │                  │
│  │ (23 chunks)      │   │ (8 phases)      │                  │
│  └────────┬─────────┘   └────────┬────────┘                  │
│           │                       │                            │
│           ▼                       ▼                            │
│  ┌─────────────────────────────────────────┐                  │
│  │ Semantic retrieval (top-K by mode boost) │                  │
│  └────────────────────┬─────────────────────┘                  │
│                       │                                        │
│                       ▼                                        │
│  ┌─────────────────────────────────────────┐                  │
│  │ Prompt builder + multi-modal content    │                  │
│  │ (text + images + PDFs + HTML context)   │                  │
│  └────────────────────┬─────────────────────┘                  │
│                       │                                        │
│                       ▼                                        │
│              api.anthropic.com/v1/messages                    │
│                  (claude-sonnet-4-6)                          │
│                       │                                        │
│                       ▼                                        │
│  ┌─────────────────────────────────────────┐                  │
│  │ Markdown renderer + export pipeline      │                  │
│  │ (TXT · MD · HTML · Jira CSV)             │                  │
│  └─────────────────────────────────────────┘                  │
└──────────────────────────────────────────────────────────────┘
```

---

## 🚀 How to use

1. Visit the **[chatbot](https://hk-qa.github.io/qa-nexus/chatbot.html)**
2. Paste your **Anthropic API key** (get one at [console.anthropic.com](https://console.anthropic.com)) — used only in this browser session
3. **Pick an STLC phase** from the left panel
4. **(Optional)** Set a target URL in the right panel for site-specific deliverables
5. **(Optional)** Attach screenshots or HTML files for visual/structural context
6. Use a **quick action** or type your prompt — start typing to see autosuggestions
7. **Export** the result as TXT, MD, HTML, or Jira CSV

---

## 🔐 Privacy & security

- Your API key is **only used in the browser session** — never sent to any server other than `api.anthropic.com`
- No analytics, no tracking, no cookies
- All requests use the `anthropic-dangerous-direct-browser-access` header (an explicit opt-in to direct browser-to-API calls)
- Code is fully open-source — audit it yourself

**Recommendation:** Set a per-key spending cap at [console.anthropic.com](https://console.anthropic.com) → Billing for any keys you use in browser-based tools.

---

## 📚 Knowledge base coverage

| Source | Topics |
|---|---|
| **ISTQB Foundation Level** | Test design techniques (EP, BVA, decision tables, state transition), severity/priority guide |
| **IEEE 829** | Test plan, test case, defect report, RTM templates |
| **STLC** | All 5 phases (Requirements Review → Test Closure) |
| **BDD** | Gherkin syntax, scenario writing |
| **Agile QA** | Shift-left testing, Definition of Done |
| **Automation** | Playwright, Cypress, Selenium WebDriver, BDD/Cucumber, Page Object Model, project structure |

---

## 🛠 Tech stack

- **AI:** Anthropic Claude Sonnet 4.6 (multi-modal: text + vision + PDF)
- **Frontend:** Vanilla HTML / CSS / JavaScript (no framework, no build step)
- **Fonts:** Outfit (display), Space Grotesk (section headers), Inter (body)
- **Hosting:** GitHub Pages
- **No backend, no database, no dependencies**

---

## 🎓 Capstone context

Built as a capstone project for the **[Codecademy Agentic AI Applications Bootcamp](https://www.codecademy.com)** — Contest #1.

Demonstrates:
- ✅ Retrieval-Augmented Generation (RAG) with semantic scoring
- ✅ Multi-modal input (text, image, PDF, HTML)
- ✅ Transparent source attribution
- ✅ Domain-specific tooling (QA methodology)
- ✅ Real-world deliverable generation (not just chat)
- ✅ Polished UX (theme toggle, resizable panels, autosuggest, exports)
- ✅ Honest AI design (clearly labels inferred vs. real selectors in automation code)

---

## 🐞 Known limitations

- **CORS-blocked sites** — page fetch falls back to URL + description mode (workaround: attach HTML file or screenshot)
- **Token limits** — very large outputs (~16K tokens) may be truncated; a Continue button resumes the response
- **No conversation persistence** — refreshing the page clears history (intentional for privacy)
- **Browser API key** — anyone with access to your browser session can see the key entered in that session (not stored, but visible in JS memory)

---

## 📄 License

**Copyright © 2026 Hitesh Kapur. All rights reserved.**

This code is published for **portfolio demonstration and educational reference**.

**You may:**
- ✅ View, read, and study the source code
- ✅ Reference patterns or approaches in your own original work
- ✅ Use the live demo with your own Anthropic API key
- ✅ Share links to this repository and the live site

**You may NOT:**
- ❌ Copy, redistribute, or republish this code or any substantial portion
- ❌ Deploy this code (in whole or in part) to any public or commercial service
- ❌ Use this code in any commercial product or paid offering
- ❌ Remove attribution or claim authorship

For commercial licensing inquiries or to request permission for other uses, please contact via LinkedIn (linked below).

> The methodology knowledge base references (ISTQB Foundation Level concepts, IEEE 829 templates, STLC definitions) are based on publicly available industry standards and are not claimed as original works.

---

## 🙏 Acknowledgments

- **[Codecademy](https://www.codecademy.com)** for the Agentic AI Applications Bootcamp
- **[Anthropic](https://www.anthropic.com)** for Claude and the multi-modal Messages API
- The ISTQB and IEEE communities for the methodology foundations this is built on

---

## 📱 Connect

Built by **Hitesh Kapur** — find me on [LinkedIn](https://www.linkedin.com/) · #CodecademyAgenticAIBootcamp