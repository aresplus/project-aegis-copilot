# 🛡️ Project Aegis 

[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![Skill](https://img.shields.io/badge/Claude_Skill-Available-black.svg)](#-quick-start-install-the-aegis-skill)
[![Whitepaper](https://img.shields.io/badge/Theory-Closed--Loop%20Control-success.svg)](#-the-aegis-whitepapers)

**Designing Production-Grade Agent Systems with Closed-Loop Control Theory.**

Through extensive architectural research and real-world SRE deployments, we discovered a harsh reality: **Most open-source Agent frameworks are fragile, open-loop scripts.** When deployed in production, they suffer from context overflow, hallucination cascades, and catastrophic long-tail operations.

**Project Aegis** redefines the AI Agent as a "Closed-Loop Control System" (analogous to a Kubernetes Controller). We use Deterministic Architecture to surround Non-Deterministic AI.

---

## 🚀 Quick Start: Install the Aegis Skill

We have packaged the entire Aegis Architecture Specification into an official **Claude Skill**. By installing this skill, your Claude (via Claude.ai or Claude Code) will actively enforce production-grade architecture during your development.

### How to Install

**Method 1: For Claude.ai Users**
1. Download or clone this repository.
2. Zip the `aegis-architect` folder.
3. Go to [Claude.ai](https://claude.ai) -> **Settings** -> **Skills**.
4. Click **Upload skill** and select your zipped folder.
5. Enable the skill.
6. In a new chat, say: *"Help me design a new Agent for Kubernetes log analysis."*

**Method 2: For Claude Code (CLI) Users**
1. Copy the `aegis-architect/` folder into your Claude Code `.claude/skills/` directory.
2. The skill will automatically load when you discuss agent architecture or refactoring.

---

## 🏛️ The 5 Aegis Core Directives

When the skill is active, Claude will enforce the following directives on your codebase:

1. **State Decoupling:** The LLM context is just an L1 Register. True state must live in an L2 GraphDB or L3 Event Log.
2. **Zero-Trust Actuation:** LLMs do not call APIs. They emit strongly-typed `IntentDescriptors`. A deterministic gateway handles execution.
3. **Actor Model over Recursion:** Abandon recursive loops. Agents are asynchronous Actors driven by message queues.
4. **SAGA Compensating Transactions:** Every multi-step LLM action must have a predefined rollback chain to self-heal.
5. **Lifecycle Cleanup:** Enforce a strict cleanup chain on Agent exit to prevent zombie processes.

---

## 📚 The Aegis Whitepapers

The deep-dive theoretical foundation, trade-off analysis, and blueprint designs are available in our whitepapers:

- 📄 [Project Aegis Technical Guide (English) - PDF](./docs/Aegis_Whitepaper_EN.pdf)
- 📄 [Project Aegis 技术指导手册 (中文版) - PDF](./docs/Aegis_Whitepaper_ZH.pdf)

*(Recommended reading for Staff Engineers, Tech Leads, and System Architects)*

---

## 🤝 Contributing
We welcome discussions on distributed agent architectures, memory paging algorithms, and execution sandboxing. PRs to improve the Skill prompts or reference templates are always welcome.

*Maintained by Ares Sheng & Mzday Technology.*