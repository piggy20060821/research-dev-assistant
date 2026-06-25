# research-dev-assistant

An [Agent Skill](https://github.com/anthropics/skills) that makes an AI assistant
**do its homework before it acts**: search the papers, study them, explain the idea
in the simplest first-principles / explain-like-I'm-5 terms (what it is, why it works,
pros & cons), let *you* decide, and make sure **every line of code has a reason — not
guesswork** (不拍脑袋).

> 一个 Agent Skill：让 AI 在动手前先查论文、读论文，然后用「小孩都能听懂的第一性原理」
> 讲清楚——这是什么、为什么有效、优缺点——再让你拍板；而且每一行代码都有出处、有逻辑，
> 绝不拍脑袋。

## What it does / 它做什么
Whenever a research or development task starts (picking a method, a library, a
parameter, or writing non-trivial code), the skill enforces this workflow:

1. 🔍 **Search papers first** — find how the problem is really solved.
2. 📖 **Study & extract** — mechanism, assumptions, results, failure cases.
3. 🧒 **Explain ELI5 + first principles** — what it is / why it works / pros & cons.
4. 🤔 **Let the user decide** — options + tradeoffs + a recommendation, then stop.
5. 🧩 **Same rigor for your inputs** — search industry-common usage before asking you.
6. ✅ **Justify every line of code** — no magic numbers, no arbitrary choices.

## Structure / 结构
```
research-dev-assistant/
├── SKILL.md                                  # metadata + the core instructions
└── references/
    ├── workflow.md                           # the full step-by-step
    ├── search-playbook.md                    # where to search + how to judge quality
    ├── eli5-guide.md                         # how to write child-friendly explanations
    └── code-justification-checklist.md       # the "every line has a reason" checklist
```

## How to use / 如何使用

### Claude.ai
Upload the `research-dev-assistant/` folder (or a zip of it) as a custom skill, then
just start a research/dev task — it triggers automatically.
将 `research-dev-assistant/` 文件夹（或其 zip）作为自定义 skill 上传即可。

### Claude API
Use the [Skills API](https://docs.claude.com/en/api/skills-guide) to upload the folder.

### Claude Code
Place the `research-dev-assistant/` folder under `.claude/skills/` in your project (or
`~/.claude/skills/` for global use).

## Format / 格式
Built to the official [Agent Skills](https://github.com/anthropics/skills) standard: a
folder with a `SKILL.md` containing YAML frontmatter (`name`, `description`) plus
instructions, with extra detail in `references/` loaded on demand (progressive
disclosure).

## License
[Apache-2.0](./LICENSE)
