# [gwas-chat](https://github.com/gwas-ai/gwas-chat)

ChatGPT, Grok, and Atlas side-panel chats ngram'd and available at via subdomain on gwas.* websites.


## gwas-chat

> **Mission:** Unify, archive, and analyze conversational intelligence across the GWAS ecosystem.

## Overview

**`gwas-chat`** is the central coordination repo for all chat-related workflows across the **GWAS** network.  

It provides a **local-first, cross-platform conversation archive** that synchronizes threads from:

- **chatgpt.com** (Conversation search and named chats)
- **ChatGPT Atlas** (side-panel and full-page chats)
- **Grok (xAI)** summaries and threads on **x.com**
- **gwas.chat** — the public-facing chat webapp and gateway

## Draft Repository Layout

```txt
/gwas-chat/
├── conversations/
│   ├── chatgpt-atlas/
│   │   ├── 2025-10-22T05-30_gwas-handshake-init.md
│   │   ├── 2025-10-22T07-12_makefile-architecture.md
│   │   └── ...
│   ├── x-website-grok/
│   │   ├── 2025-10-21T11-15_xdotcom-summary.md
│   │   └── ...
├── scripts/
│   ├── capture_conversation.ts
│   ├── sync_conversations.ts
│   └── summarize_conversation.ts
├── Makefile
└── README.md
```

---

## Conversation Format

Every chat log follows this schema:

```markdown
---
title: "Grok Summary — BYU Sports Thread"
source: "x.com"
model: "grok"
date: 2025-10-22T05:30:00-05:00
repo: gwas-ai/gwas-chat
tags: [grok, xai, summary, sports]
context_url: "https://x.com/chandlerhaueter/status/..."
---

# Conversation Log

**User:** What happened with BYU’s game last night?

**Grok:** BYU dominated Kansas City 34–21. Slovis threw for 312 yards and 3 TDs.
```

## Goals

1. **Unify** all LLM conversations (ChatGPT, Grok, Atlas, etc.) into a single structured archive.
2. **Version** them under Git for reproducibility, analysis, and reference.
3. **Summarize and tag** using modular utilities (`@gwas-chat/chat-index`, `@gwas-chat/chat-summary`).
4. **Link back** to related repos (`gwas-handshake`, `gwas-feedback`, etc.).
5. **Visualize** chat relationships via a graph (LLM ↔ repo ↔ topic).

## Automation Plan

| Layer     | Function                            | Example Tool                        |
| --------- | ----------------------------------- | ----------------------------------- |
| Summary   | Generate concise abstracts          | `scripts/summarize_conversation.ts` |

## Related Projects

| Repo                           | Purpose            |
| ------------------------------ | ------------------ |
| [gwas.chat](https://gwas.chat) | Public chat webapp |
| [ubi.chat](https://ubi.chat)   | Public chat webapp |
| [wld.chat](https://ubi.chat)   | Public chat webapp |

## Future Directions

## License

MIT — © 2025 **gwas.ai**

## GWAS Footer (v1 — Ecosystem Unified)

### **PRODUCTS**

* [GWAS Chat](https://gwas.chat) — LLM conversation archive
* [GWAS Docs](https://docs.gwas.ai) — Documentation hub
* [GWAS Sheet](https://sheet.gwas.chat) — Structured data tables
* [GWAS App](https://gwas.app) — Local-first desktop + mobile
* [GWAS Feedback](https://gwas.feedback) — Surveys + evaluation
* [GWAS Network](https://gwas.network) — Node graph + identity
* [GWAS Market](https://gwas.market) — Auctions & prediction tools
* [GWAS Registry](https://mcp.gwas.ai) — MCP + API registry

---

### **SUPPORT**

* [Help Center](https://help.gwas.ai)
* [Knowledge Base](https://docs.gwas.ai/support)
* [Feedback Portal](https://feedback.gwas.ai)
* [Status Page](https://status.gwas.ai)
* [Contact](mailto:support@gwas.ai)

---

### **TOOLS**

* [Conversation Search](https://search.gwas.chat)
* [Prompt Index](https://index.gwas.chat)
* [Model Playground](https://labs.gwas.ai)
* [Spec Viewer](https://spec.gwas.ai)
* [API Access](https://api.gwas.ai)

---

### **OUR COMPANY**

* [About GWAS.ai](https://gwas.ai/about)
* [Blog](https://blog.gwas.ai)
* [Careers](https://jobs.gwas.ai)
* [Branding Guidelines](https://brand.gwas.ai)
* [Privacy & Terms](https://legal.gwas.ai)

---

### **ACCOUNT**

* [My Profile](https://id.gwas.ai)
* [Billing & API Keys](https://billing.gwas.ai)
* [Settings](https://settings.gwas.ai)
* [Logout](https://id.gwas.ai/logout)

---

### **FOLLOW**

[GitHub](https://github.com/gwas-ai) · [X (Twitter)](https://x.com/chandlerhaueter) · [YouTube](https://www.youtube.com/@chandler-haueter) · [LinkedIn](https://linkedin.com/in/chandlerhaueter)

---

**© 2025 gwas.ai — MIT Licensed**
See also: [sheet.gwas.chat](https://sheet.gwas.chat) · [docs.gwas.ai](https://docs.gwas.ai) · [feedback.gwas.ai](https://feedback.gwas.ai)

---

### DESIGN NOTE

For a UI layout:

* Use **four columns** with headings identical to the sections above.
* Each link in **red hover** (#ff4d4d) on dark background (#111).
* Social/payment icons in a **bottom bar**, e.g.:

`GitHub · X · YouTube · Apple Pay · Google Pay · Bitcoin · Stripe`

---

Would you like me to output this as an **HTML + Tailwind footer component** (ready for GitHub Pages or Deno Fresh)?

**See also:** [https://gwas.chat](https://gwas.chat) · [https://sheet.gwas.chat](https://sheet.gwas.chat) · [https://docs.gwas.ai](https://docs.gwas.chat)
