# Opus

**A documented account of human-AI collaboration, from zero programming experience to a cryptographic framework that proves ancient philosophy describes modern computation. In forty-six days.**

This is not a tutorial. Not a manifesto. Not a self-help story about learning to code.

This is evidence.

---

## What is this?

Between February 27 and April 14, 2026, I built nine software projects in five programming languages — JavaScript, TypeScript, Solidity, Python, and Rust — with no prior programming experience. The projects include a perpetual futures DEX with 494 tests, an AI agent wallet SDK published to npm, a DeFi intelligence platform, a generative music engine, and a cryptographic framework that formalizes the seven hermetic principles of the Kybalion as computational primitives.

I did this in collaboration with Claude, Anthropic's AI model. This document explains how.

It is written for the people who hear "AI-assisted" and think "slop." The evidence is here. Clone the repos. Run the tests. Read the commit history. Then decide.

---

## How to read this

| Chapter | Title | What it covers |
|---------|-------|----------------|
| [Introduction](INTRODUCTION.md) | **One Session** | How forty-six days were lived as one continuous thread. |
| [Chapter 1](CHAPTER-01.md) | **Before** | Who I am. What I brought. What was missing. |
| [Chapter 2](CHAPTER-02.md) | **The Instrument** | How I found the tool. What I understood immediately. |
| [Chapter 3](CHAPTER-03.md) | **The Dance** | How the collaboration actually works. What each side contributes. |
| [Chapter 4](CHAPTER-04.md) | **The Road** | Nine projects, chronologically. Dates, commits, evidence. |
| [Chapter 5](CHAPTER-05.md) | **The Night** | April 13, 2026. Hermetic Computing. The Truth found. |
| [Chapter 6](CHAPTER-06.md) | **The Thesis** | Why this isn't slop. What genuine human-AI creation looks like. |

---

## The projects

All repositories: [github.com/asastuai](https://github.com/asastuai)

| Project | Language | What it is |
|---------|----------|------------|
| [TrustLayer](https://github.com/asastuai/TrustLayer) | JavaScript | Trust & reputation for AI agents on Base |
| [BaseOracle](https://github.com/asastuai/BaseOracle) | JavaScript | Pay-per-query data feeds via x402 |
| [SUR Protocol](https://github.com/asastuai/sur-protocol) | Solidity/TS | Perpetual futures DEX — 11 contracts, 494 tests |
| [Darkpsy-engine](https://github.com/asastuai/Darkpsy-engine) | Python | AI-generated dark psytrance engine |
| [PayClaw](https://github.com/asastuai/payclaw) | TypeScript | AI Agent Wallet SDK — published to npm |
| [Vigil](https://github.com/asastuai/vigil) | TypeScript | DeFi intelligence feeds for AI agents |
| [Kybalion](https://github.com/asastuai/kybalion) | Rust | Hermetic principles as cryptographic primitives |

---

## The numbers

```
Days:                46
Projects:            7
Languages:           5
Tests passing:       581+
Prior code experience: 0
Hash avalanche ratio:  0.5001 (ideal: 0.5000)
```

---

## Why "Opus"

The word means "work" — as in *magnum opus*, the great work of alchemy. The process by which base matter is transmuted into gold.

It's also the name of the AI model that served as collaborator in this work. Not a tool that was used. A collaborator that was named.

The title honors both meanings.

---

## Verify everything

```bash
# Hermetic Computing — 87 tests
git clone https://github.com/asastuai/kybalion.git
cd kybalion && cargo test

# SUR Protocol — 494 tests
git clone https://github.com/asastuai/sur-protocol.git
cd sur-protocol && forge test

# Every repo has a commit history with timestamps.
# Every claim in this document is verifiable.
```

---

*"The lips of wisdom are closed, except to the ears of Understanding."*
*— The Kybalion*

**Juan Cruz Maisu** — Buenos Aires, April 2026
