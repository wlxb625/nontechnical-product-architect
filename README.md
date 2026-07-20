# Nontechnical Product Architect

A plain-language AI skill that helps non-technical builders turn product ideas into clear, reviewable, and implementation-ready plans before coding begins.

**非技术产品开发架构师**：帮助没有计算机背景的用户，在正式写代码前完成产品澄清、MVP 收缩、用户流程、页面与数据设计、AI 行为设计、技术栈选择、风险分析和 Codex 开发交接，并用通俗语言解释专业概念。

## What it does

- Turns a rough website, app, or AI product idea into a structured product plan.
- Separates MVP essentials from unnecessary early complexity.
- Explains APIs, databases, authentication, RAG, deployment, and architecture in plain language.
- Records key decisions, alternatives, costs, risks, and future migration impact.
- Produces staged handoff documents that Codex or another coding agent can execute.
- Reviews existing PRDs and technical plans for gaps, conflicts, and overengineering.

## 适合谁

- 非计算机专业学生
- 希望通过 AI 开发网站或 App 的独立创作者
- 能使用 ChatGPT、Codex 等工具，但看不懂技术方案的用户
- 需要把产品构想整理成可执行开发资料的产品发起者

## Repository structure

```text
nontechnical-product-architect/
├── SKILL.md
├── README.md
├── LICENSE
├── agents/
│   └── openai.yaml
├── references/
│   ├── PLAIN_LANGUAGE_GUIDE.md
│   ├── QUALITY_GATES.md
│   ├── STAGE_TEMPLATES.md
│   └── TECH_DECISION_GUIDE.md
└── evals/
    └── prompts.csv
```

## Installation

### User-level installation

```bash
mkdir -p ~/.agents/skills
git clone https://github.com/wlxb625/nontechnical-product-architect.git \
  ~/.agents/skills/nontechnical-product-architect
```

### Project-level installation

Run inside your project directory:

```bash
mkdir -p .agents/skills
git clone https://github.com/wlxb625/nontechnical-product-architect.git \
  .agents/skills/nontechnical-product-architect
```

Restart Codex if the skill does not appear immediately.

## Usage

Call it explicitly:

```text
$nontechnical-product-architect
```

Example:

```text
使用 $nontechnical-product-architect。
我是非计算机专业，想开发一个长期陪伴用户成长的 AI 伙伴 App。
先不要写代码，请从产品想法澄清和 MVP 设计开始。
每次出现专业概念时，用通俗语言解释它是什么、为什么需要、
有哪些替代方案，以及这个决定会影响什么。
```

The skill can also be triggered through natural-language requests such as:

```text
先别写代码，帮我整理产品需求、收缩 MVP，并解释技术方案。
```

## Operating modes

- **Complete product mode** — from idea clarification through Codex handoff.
- **Rapid MVP mode** — a compact path for prototypes, hackathons, and weekend projects.
- **Technical translation mode** — explains an existing technical proposal in plain language.
- **Plan review mode** — finds missing requirements, contradictions, hidden costs, and overengineering.
- **Codex handoff mode** — converts an existing product plan into staged implementation tasks.

## Design principles

1. Requirements before technology.
2. Explain before advancing.
3. Prefer the simplest viable solution.
4. Separate confirmed facts, recommendations, assumptions, and pending decisions.
5. Expose costs, risks, platform dependencies, and migration consequences.
6. Do not hide product or privacy decisions inside technical defaults.
7. Do not start product coding before the relevant quality gates are met.

## License

MIT
