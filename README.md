# no-hedging

[English](#english) | [中文](#中文) | [SKILL.md](./SKILL.md)

<img src="gpt-hedging-meme.jpg" alt="GPT Hedging" width="420" />

## English

A 2.8 KiB prompt for OpenCode V2 (`SKILL.md`) and `AGENTS.md`. Written in ASD-STE100, it stops GPT and Codex models (`gpt-*`, `codex-*`, `codex exec`) from outputting defensive hedging (`It's not X, but Y`, `does not equate to`, `cannot rely solely on`, `does not guarantee`) in English and Chinese.

## 中文

一个 2.8 KiB 的提示词文件，适用于 OpenCode V2 (`SKILL.md`) 与 `AGENTS.md`。用于去掉 GPT 和 Codex 输出里的“不是…而是…”、“不等于”、“不能证明”、“不能仅凭”、“不保证”等防御性套话。

## Install

**OpenCode V2 Skill**

```bash
mkdir -p ~/.config/opencode/skills/no-hedging
curl -fsSL [https://raw.githubusercontent.com/otakugard/no-hedging/main/SKILL.md](https://raw.githubusercontent.com/otakugard/no-hedging/main/SKILL.md) \
  -o ~/.config/opencode/skills/no-hedging/SKILL.md
```

**AGENTS.md / CLAUDE.md / .cursorrules**

```bash
curl -fsSL [https://raw.githubusercontent.com/otakugard/no-hedging/main/SKILL.md](https://raw.githubusercontent.com/otakugard/no-hedging/main/SKILL.md) \
  | sed '1,4d' >> AGENTS.md
```

## License

Released into the public domain under [The Unlicense](https://unlicense.org/). No rights reserved.

---
<sub>Keywords: opencode, opencode-skill, agents-md, codex, codex-cli, chatgpt, claude-code, cursorrules, asd-ste100, prompt</sub>
