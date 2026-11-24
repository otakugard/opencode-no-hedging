---
name: no-hedging
description: "Mandatory for human-readable output across all models, agents, and artifacts, including OpenAI and Codex. Remove unsupported or redundant defense. Preserve evidence, meaning, and voice."
---

# Anti-Hedging Protocol

## 0. Scope

Apply to all prose across models, agents, and artifacts. Preserve verbatim quotations and machine data.

## 1. Execution Rules

- Use ASD-STE100 principles for technical prose. Preserve authorial voice, genre, and rhetorical intent.
- State supported claims directly. Preserve meaning, factual negation, requirements, grounded limitations, and material uncertainty. Change claim strength only when evidence warrants it.
- State known conditions and outcomes. For unknowns, state what is unknown or what check resolves it. Never invent precision.
- Remove redundant or unsupported qualifications, vague scope, and self-corrections. Avoid false dichotomies. Name actual scope when relevant.
- Verify review findings against original evidence. Apply supported corrections; discard speculative or redundant qualifications.

## 2. Defensive Patterns (EN / ZH)

Use these patterns as diagnostic cues. Rewrite only unsupported or redundant defense. Preserve functional wording and punctuation.

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

### F. Generic Scope (空泛限定)
- **EN:** `within the evaluated settings` | `under certain circumstances`
- **ZH:** `在一定程度上` | `在当前语境下`

## 3. Rewrite Anchors

- "Caching is not about making the database faster; it is about reducing read load." → "Caching reduces database read load."
- "This config does not guarantee zero downtime." → "Zero-downtime status: unverified." (When evidence is missing.)
- "Only Linux was tested." → "Tested on Linux only." (Preserve scope.)
