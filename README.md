# Page PRD Writer

Write concise, execution-ready page PRDs from real product artifacts.

`page-prd-writer` is a practical skill for product teams. It turns a real page source — prototype, screenshot, local route, or code page — into a short requirement document that is clear enough for engineering and operations to align on quickly.

Instead of generating long, template-heavy PRDs, this skill focuses on one thing: **extracting the rules that actually matter for delivery**.

## Why this exists

In day-to-day product work, the slowest part is often not thinking through the solution, but translating an already-formed page plan into a document that other functions can execute against.

A common workflow looks like this:

1. The product manager has already explored the page through prototypes, drafts, or AI-generated mockups.
2. The overall structure and interaction direction are already fairly clear.
3. What still takes time is rewriting all of that into a PRD that engineering and operations can read, review, and act on.

That translation step is repetitive and expensive.

`page-prd-writer` is built for exactly that gap.

It helps convert an existing page artifact into a requirement note that is:

- short enough to read quickly,
- specific enough to execute,
- structured enough for cross-functional alignment.

## What problem it solves

Most AI writing tools either:

- produce generic PM templates,
- describe every visible UI block one by one,
- or expand into long documents that look complete but are hard to use.

This skill takes a different approach.

It defaults to **feature-based, rule-focused PRD output**, and keeps only the logic that affects implementation, such as:

- search behavior
- tabs and filters
- sorting rules
- list/card actions
- submit logic
- empty states
- URL state sync
- output/data mapping

In short: it tries to produce the version of a page PRD that teams actually use.

## Best use cases

Use this skill when you already have a concrete page artifact and want to turn it into a usable requirement note fast.

Typical scenarios:

- turning a prototype page into a page PRD
- summarizing a shipped or in-progress frontend page into product language
- converting screenshots or page captures into requirement notes
- creating a concise alignment doc before syncing with engineering or operations
- standardizing page-level requirement writing across a product team

## Core principles

### 1. Real artifact first
The skill reads the actual source artifact before writing.

Depending on input, that may be:
- a local route or page path
- frontend code and related constants
- a prototype
- a screenshot

If both code and UI exist, code is treated as the source of truth for page rules.

### 2. Group by function, not by layout
The output is organized by functional blocks, not by every visual area on the screen.

That means the result is closer to how delivery teams discuss work:
- list sorting
- filter logic
- publishing rules
- card actions
- result states

not:
- top area
- middle area
- bottom area
- button area

### 3. Default to short, not exhaustive
The default output is intentionally concise.

The target is not "document everything visible".
The target is **"enough to execute"**.

For a normal page, the result is usually 3–8 numbered feature blocks.

### 4. Expand only when needed
Detailed mode is used only when the user explicitly asks for:
- a full PRD
- field-by-field detail
- a detailed version
- or when the page is a complex publish/edit form

Even in detailed mode, the writing should stay operational and avoid decorative noise.

## Example output style

```md
1、列表排序

排序选项包括：综合排序、质量优先、最近发布。默认选中综合排序。

综合排序：沿用搜索中台返回顺序。
质量优先：按推荐等级、推荐时间、创建时间倒序。
最近发布：按发布时间倒序，相同发布时间再按推荐等级倒序。
```

This is the intended density: one functional topic, then only the rules that matter.

## What it keeps

- sorting rules
- filter options and combined logic
- tab switching logic
- search behavior
- URL parameter sync
- submit/delete/copy/download consequences
- empty states
- data mapping that affects output

## What it cuts

- decorative layout descriptions
- repeated UI inventory
- static copy that does not affect logic
- long explanations of obvious page structure
- fake completeness for the sake of documentation format

## Team value

This skill is especially useful in product-engineering-operations collaboration.

It helps teams move faster in the middle layer between "we already know roughly what this page should do" and "we now need a doc that others can execute against".

Its value is not replacing product judgment.
Its value is **compressing the translation cost** between page intent and delivery-ready documentation.

## Repository structure

```text
page-prd-writer/
├── SKILL.md
├── README.md
├── LICENSE
├── agents/
│   └── openai.yaml
└── references/
    └── output-pattern.md
```

## Files

### `SKILL.md`
Defines the skill behavior, use cases, and writing rules.

### `references/output-pattern.md`
Provides the short-form output skeleton, detailed fallback, and keep/cut rules.

### `agents/openai.yaml`
Defines the interface metadata for agent runtime integration.

## Who this is for

- product managers
- AI product managers
- product operations teams
- frontend teams who need page logic summarized quickly
- teams trying to standardize concise PRD writing

## Open source intent

This repository is an attempt to turn a real, repeated product workflow into a reusable skill.

The underlying belief is simple:

> A lot of PM work is not about generating ideas from zero. It is about turning an already-formed solution into a clear artifact that others can execute.

This project packages that step into a reusable format.

## License

MIT
