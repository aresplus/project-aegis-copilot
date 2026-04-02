# 🛡️ Project Aegis

[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![Claude Skill](https://img.shields.io/badge/Claude_Skill-Available-black.svg)](#-quick-start)
[![Architecture](https://img.shields.io/badge/Architecture-Multi--Agent-purple.svg)](#-the-5-aegis-core-directives)
[![Theory](https://img.shields.io/badge/Theory-Closed--Loop_Control-success.svg)](#-the-aegis-whitepapers)
[![Stage](https://img.shields.io/badge/Stage-Production_Architecture-red.svg)](#-what-problem-aegis-solves)

**Build production-grade AI agent systems with closed-loop architecture, deterministic workflows, and Claude Skill enforcement.**

Project Aegis is a **Claude Skill + architecture framework** for building reliable, scalable, and production-safe AI Agent systems.

It helps developers and teams move beyond fragile prompt scripts by enforcing **closed-loop control**, **structured state management**, **deterministic execution boundaries**, and **safe multi-step orchestration**.

If you are designing real-world agents for internal tools, ops automation, copilots, or multi-agent workflows, Aegis gives you a more production-ready foundation.

---

## Why Project Aegis Exists

Most open-source agent frameworks look powerful in demos, but become brittle in production.

They often rely on open-loop prompt chaining, hidden mutable state, recursive tool calls, and loosely controlled side effects. Under real traffic, this leads to familiar disasters:

- Context overflow
- Hallucination cascades
- State drift across long-running tasks
- Recursive instability
- Unsafe execution of tools and APIs
- Zombie processes and incomplete cleanup

**Project Aegis** redefines the AI Agent as a **Closed-Loop Control System**, conceptually closer to a **Kubernetes Controller** than a chatbot script.

The core idea is simple:

> Use deterministic architecture to surround non-deterministic AI.

---

## What Problem Aegis Solves

Aegis is designed for builders who want to answer questions like:

- How do I stop an LLM agent from becoming an untraceable mess in production?
- How should agent state be stored outside the model context?
- How do I make multi-step actions recoverable and auditable?
- How do I prevent recursive tool chaos and hidden side effects?
- How do I turn “prompt-based automation” into a real system architecture?

Aegis provides a practical answer through:

- A reusable **Claude Skill**
- A production-oriented **agent architecture model**
- A set of **core directives** for system design
- Technical whitepapers for deeper architectural reasoning

---

## 🚀 Quick Start

We have packaged the Aegis architecture specification into an installable **Claude Skill**.

Once installed, Claude will stop drifting toward ad-hoc agent code and begin guiding you toward **production-safe architecture decisions**.

### Install for Claude.ai

1. Download or clone this repository.
2. Compress the `aegis-architect` folder into a `.zip` file.
3. Go to [Claude.ai](https://claude.ai) → **Settings** → **Skills**.
4. Click **Upload skill** and select the zipped folder.
5. Enable the skill.
6. Start a new chat and try a prompt like:

```text
Help me design a production-grade agent for Kubernetes log analysis.

Install for Claude Code
Copy the aegis-architect/ folder into your Claude Code .claude/skills/ directory.
The skill will be loaded automatically when you discuss agent architecture, orchestration, or refactoring.
What You Get After Installation

After enabling the skill, Claude will help you:

Design agents with explicit state boundaries
Avoid unsafe API execution patterns
Replace recursive loops with actor-style workflows
Introduce rollback paths for multi-step actions
Think in terms of controllers, intents, queues, and lifecycle management
Refactor fragile agent prototypes into production-oriented systems

In short, Aegis turns Claude from a code generator into an agent architecture copilot.

Typical Use Cases

Project Aegis is especially useful for:

Incident response agents
Kubernetes / SRE automation assistants
Internal enterprise copilots
Workflow orchestration agents
Knowledge-to-action systems
Multi-agent task pipelines
Tool-using agents that require safety and auditability

If your agent is expected to survive real users, real data, and real failure modes, Aegis is built for that battlefield.

🏛️ The 5 Aegis Core Directives

These directives are designed to prevent the most common production failures in LLM agents: context overload, hidden state drift, recursive instability, and unsafe side effects.

When the skill is active, Claude will enforce the following architectural principles:

1. State Decoupling

The LLM context is only an L1 register, not your source of truth.

Persistent state should live in deterministic storage layers such as:

L2 GraphDB
L3 Event Log
Durable workflow state stores
2. Zero-Trust Actuation

LLMs should not call external APIs directly.

Instead, they should emit strongly typed IntentDescriptors, which are executed by a deterministic gateway layer with validation, policy checks, and observability.

3. Actor Model over Recursion

Avoid recursive prompt loops.

Agents should be modeled as asynchronous actors driven by queues, messages, and explicit transitions, rather than self-calling prompt chains.

4. SAGA Compensating Transactions

Every multi-step LLM-driven action must have a predefined rollback or compensation path.

If an operation fails halfway, the system should be able to recover instead of leaving hidden wreckage behind.

5. Lifecycle Cleanup

Every agent run should end with explicit cleanup.

Resources, locks, memory handles, and temporary artifacts must be released to prevent zombie processes and state pollution.

📚 The Aegis Whitepapers

For deeper architectural reasoning, trade-off analysis, and blueprint design patterns, read the Aegis whitepapers:

📄 Project Aegis Technical Guide (English) – PDF

Technical deep dive for architects, staff engineers, and advanced builders.
📄 Project Aegis 技术指导手册（中文版）– PDF

中文架构导读与核心思想说明，适合中文开发者与技术负责人阅读。

Recommended for: Staff Engineers, Tech Leads, System Architects, AI Infra Builders, and serious Agent developers.

Repository Structure
.
├── aegis-architect/    # Installable Claude Skill package
├── docs/               # Whitepapers and supporting technical documents
├── README.md
├── LICENSE
Who This Project Is For

Project Aegis is built for people who are no longer satisfied with “it works in the demo.”

This repository is for:

AI engineers building serious agent systems
Product-minded technical founders
Staff engineers and architects
Teams designing internal AI platforms
Developers exploring production-safe multi-agent design

If you are still in the “prompt toy” phase, this repo may feel strict.

If you are already asking, “How do I make this safe, durable, and scalable?” then you are in the right place.

Roadmap

Planned directions for Project Aegis include:

More reference agent templates
Additional Claude Skill patterns
Expanded architecture examples
Evaluation and observability guidance
Safer execution gateway patterns
Multi-agent orchestration blueprints
🤝 Contributing

We welcome contributions in areas such as:

Agent runtime design
Workflow orchestration
Memory architecture
Intent schema design
Evaluation pipelines
Claude Skill prompt refinement
Production architecture examples

PRs, issues, and discussions are welcome.

If you want to contribute, improve the skill, or expand the architecture patterns, jump in.

Discussions

If you are experimenting with:

distributed agent systems
long-running workflows
execution sandboxing
memory paging
safe tool invocation
production agent architecture

please open an Issue or start a Discussion.

This project is intended to grow through real-world architecture conversations, not just static documentation.

Contact

For architecture collaboration, consulting, enterprise adoption, or custom AI Agent system design:

Contact: your-email@example.com

You can also use this repository as the starting point for deeper technical discussion.

License

This project is licensed under the Apache 2.0 License
.