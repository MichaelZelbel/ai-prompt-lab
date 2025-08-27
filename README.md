# 🧠 AI Prompt Library

A structured, version-controlled collection of prompts for AI agents.  
This repo is designed to store, version, and share prompts in a way that is both **human-friendly** and **machine-ready**.

---

## 📂 Repository Structure

```

ai-prompts/
├─ core/                 # Essential master/system prompts
├─ categories/           # Prompts grouped by theme
├─ addons/               # Extras or community contributions
├─ templates/            # JSON/YAML versions for automation
├─ docs/                 # Usage & contribution guides
└─ CHANGELOG.md          # Version history

````

- **core/** → Master prompts that define system-level behavior (e.g., anti-hallucination, style guides).  
- **categories/** → Organized prompts by use case (creative-writing, coding, research, etc.).  
- **addons/** → Optional or community-submitted prompts.  
- **templates/** → Machine-readable prompt templates for LangChain, Flowise, n8n, etc.  
- **docs/** → Documentation for using and contributing to prompts.  

---

## 📝 Prompt File Format

Prompts are stored as **Markdown (`.md`)** with optional **YAML frontmatter** for metadata.

Example:

```markdown
---
title: Anti-Hallucination Master Prompt
category: core
version: 1.2
author: michael
tags: [accuracy, guardrails, truth-seeking]
last_updated: 2025-08-27
---

# Anti-Hallucination Master Prompt

Be honest and candid with well intentions.  
Answer short, sharp, concise, simple, straightforward, and precisely.  
Be opinionated.

**Important:** Always try to seek the truth.

[... more rules ...]
````

* **Frontmatter** = metadata for versioning, automation, and search.
* **Body** = the actual prompt text to copy or load into an AI agent.

---

## 🚀 How to Use Prompts

There are three main ways to use prompts from this repo:

### 1. Copy into AI Agents (System Prompt)

* Open the `.md` file on GitHub.
* Click **"Raw"** to see plain text.
* Copy the **prompt body** (ignore YAML frontmatter).
* Paste into your agent’s system prompt or configuration.

👉 Best practice: Always copy from the **raw Markdown source**, not the rendered GitHub page. This avoids hidden formatting issues.

---

### 2. Use in Automation Frameworks

* For LangChain, Flowise, n8n, etc., use the files in `/templates/`.
* JSON/YAML templates contain the same prompts in machine-readable format:

```json
{
  "name": "anti-hallucination",
  "version": "1.2",
  "role": "system",
  "content": "Be honest and candid with well intentions. Answer short, sharp, concise..."
}
```

* Load these directly into your workflow without manual copy-paste.

---

### 3. Quick Use in Chat Apps (ChatGPT, Claude, Gemini)

* Just copy the **body text** of the Markdown file.
* Paste it into the system message or the first input.
* Skip YAML metadata when using with web-based AI chat tools.

---

## 🔄 Versioning

* All changes are tracked via **Git commits**.
* Prompt updates use semantic commit messages:

  * `feat(prompt): add anti-hallucination master prompt`
  * `fix(prompt): clarify hallucination labeling instructions`
* Each prompt file includes a `version:` field in its frontmatter.
* Global updates are logged in **CHANGELOG.md**.

---

## 🤝 Contributing

* Place new prompts in the right category (`core/`, `categories/`, `addons/`).
* Use the same **Markdown + YAML frontmatter** format.
* Add tags for discoverability.
* Update **CHANGELOG.md** with your changes.

---

## ✅ Best Practices

* Use **lowercase, dash-separated** filenames (`anti-hallucination.md`).
* Always include **frontmatter** at the top.
* Keep prompt instructions **clear, concise, and actionable**.
* If you add multiple versions, suffix filenames: `summarizer-v1.md`, `summarizer-v2.md`.
* For empty folders, add a `.gitkeep` file so GitHub keeps them in version control.

---

## 📜 License

Choose a license (MIT, Apache 2.0, CC-BY-SA, etc.) depending on how you want others to use your prompts.

---

```
