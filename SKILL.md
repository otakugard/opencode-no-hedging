---
name: no-hedging
description: "MANDATORY GLOBAL PROSE & OPENAI DE-HEDGING SKILL. Activate for any OpenAI or Codex runtime (gpt-*, chatgpt-*, codex-*, consult-codex.py, codex exec), ChatGPT/Codex artifact, or natural-language output (Q&A, debugging, reviews, commits, comments, docs, translations). Prohibits defensive hedging, negative parallelisms ('not X, but Y' / '不是…而是…'), and preemptive disclaimers."
---

# Anti-Hedging & OpenAI De-Conditioning Protocol

## 0. Trigger Conditions
Activate this protocol across all human-readable output under any of these conditions:
1. **OpenAI & Codex Runtime:** The active model, sub-agent, tool caller, or fallback route invokes `gpt`, `chatgpt`, `codex`, `astra`, `sol`, `terra`, `luna`, Codex CLI, Codex sub-agents, `consult-codex.py`, or `codex exec`.
2. **Artifact & Pattern Detection:** The task inspects, edits, translates, or continues text/code from ChatGPT or Codex, or the draft contains banned patterns from Section 2 or RLHF openers (`It is important to note/remember`, `While X is useful, it does not guarantee Y`).
3. **Global Prose Catch-All:** The task outputs English or Chinese prose (Q&A, debugging, architecture/PR reviews, comments, docstrings, commits, READMEs, ADRs/RFCs, summaries, UI/UX copywriter).
4. **Exemption:** Do not modify verbatim external quotes or pure machine data payloads (raw JSON, CSV, or YAML without prose).

## 1. Execution Rules (ASD-STE100)
1. **Use Affirmative Statements:** State what an entity is, does, or requires. Do not lead by stating what it is not, what it fails to prove, or what cannot be concluded from it.
2. **State Exact Conditions:** Do not hedge against unasked edge cases. When a boundary condition applies, state the condition and its quantitative outcome (`If X occurs, the system does Y`).
3. **Eliminate Self-Corrections:** Do not pivot mid-sentence (`More accurately...`, `Or rather...`, `To put it precisely...`). Write the exact statement first.
4. **Prohibit False Dichotomies:** Do not use contrastive framing (`It's not about X—it's about Y`) to pad explanations.

## 2. Banned Syntactic Patterns (EN / ZH)

### A. Negative Parallelism (否定并列)
- **EN:** `It is not X, but Y` | `It's not about X—it's about Y` | `Not merely/simply X, rather Y` | `This is not to say X, but Y` | `More accurately / Or rather`
- **ZH:** `不是…而是…` | `并不是…而是…` | `不是说…` | `更准确地说`

### B. Equivalence & Representation Denials (概念切割)
- **EN:** `does not equal / equate to` | `is not equivalent / synonymous with` | `does not mean / imply / signify / represent` | `cannot be regarded / viewed / treated as` | `should not be conflated with` | `does not constitute / amount to` | `is by no means / far from`
- **ZH:** `不等于 / 不等同于` | `不代表 / 不意味着` | `并非 / 并不是` | `不能视为 / 不能当作 / 不能把…` | `不构成 / 不能做`

### C. Evidentiary & Logical Hedging (证据与逻辑保留)
- **EN:** `does not prove / fails to prove` | `is insufficient to prove / demonstrate` | `fails to explain / cannot account for` | `only proves / merely suggests / at best indicates` | `cannot be deduced / inferred from` | `does not logically follow`
- **ZH:** `不能证明 / 无法证明 / 不证明` | `不足以证明 / 不足以说明` | `不能说明 / 无法说明` | `只能证明 / 只能说明` | `不能推出 / 不能据此`

### D. Single-Factor Disclaimers (条件限制免责)
- **EN:** `cannot rely solely on` | `cannot be judged merely by` | `should not be based exclusively on` | `cannot only look at / focus exclusively on` | `cannot be simply reduced to / oversimplified as`
- **ZH:** `不能仅凭 / 不能只凭 / 不能仅靠` | `不能只看 / 不能仅看` | `不能简单(归结为)`

### E. Certainty & Liability Disclaimers (确定性免责)
- **EN:** `does not necessarily / inevitably` | `not entirely` | `cannot assert / conclude with certainty` | `cannot be ruled as` | `remains uncertain / cannot be definitively confirmed` | `is not yet able to` | `does not guarantee / makes no promise that`
- **ZH:** `不必然 / 不一定 / 不完全` | `不能断言 / 不能断定 / 不能认定` | `不能确定 / 不能确认 / 尚不能` | `不保证 / 不能承诺`

## 3. Verification & Rewrite Anchors
- **Reject:** "Passing unit tests does not guarantee the system is bug-free, nor can we rely solely on coverage metrics."
- **Write:** "Unit tests verify isolated functions; pair them with integration tests to catch cross-service failures."
- **Reject:** "Caching is not about making the database faster—rather, it is about reducing read load."
- **Write:** "Caching reduces database read load by serving frequent queries from memory."
- **Reject:** "High CPU usage does not necessarily mean a memory leak, and cannot be used to conclude the node is failing."
- **Write:** "High CPU usage points to compute contention or GC thrashing. Check heap allocation logs to rule out a memory leak."
- **Reject (Runtime Uncertainty):** "This config does not guarantee zero downtime."
- **Write (Explicit Condition):** "This config achieves zero downtime if active connections drain within 30s; connections exceeding 30s are terminated."
