# ancestors-skill

Two Claude skills that answer decisions and problems with what people historically did about them, then test the best option with a small trial.

## Index

- [What it does](#what-it-does)
- [The skills](#the-skills)
- [How an answer is built](#how-an-answer-is-built)
- [Install](#install)
- [Usage](#usage)

## What it does

Most advice is either modern fashion or one person's opinion. These skills look at what civilizations actually practised for the same kind of problem, tell you which tradition knows it best, check whether separate cultures arrived at the same answer, and say what modern research adds or contradicts. Then they set up a trial, one change at a time, with a measure decided before you start.

Each answer is written as a historian of ideas working from written records and long-running practice. Historical claims that are wrong get corrected plainly.

## The skills

| Skill | Command | Purpose |
|---|---|---|
| `ancestors/` | `/ancestors <question>` | Advice from history, framed as "what did our ancestors do about X". |
| `oracle/` | `/oracle <question>` | The same method, framed as guidance from humanity's accumulated experience. |

Each skill folder holds one `SKILL.md`, which contains the instructions Claude follows.

## How an answer is built

1. **Route** to the one or two traditions with the deepest expertise in the area.
2. **State** the concrete practice and what it responded to, with primary sources named where possible.
3. **Convergence test** labels each practice *convergent*, *single-tradition*, or *symbolic/sacred*.
4. **Modern evidence** separates the practice (which may work) from the explanation (which may not).
5. **Recommendation and trial:** one change, 2–4 weeks, one baseline measure and a success threshold set in advance.
6. **Learnings log:** the user's own tested result outranks any tradition's claim.

## Install

Clone the repo into your Claude skills folder, or add it as a plugin that reads `.claude-plugin/manifest.json`:

```powershell
git clone https://github.com/saiganeshreddym611-ai/ancestors-skill.git
```

## Usage

```text
/ancestors how should I structure a study day
/oracle my cofounder keeps changing his mind
```
