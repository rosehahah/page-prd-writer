# Page PRD Writer

[中文](./README.zh-CN.md) | [English](./README.en.md)

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
1、Sorting Rules

Available sorting options: Comprehensive, Quality First, Latest. Default is Comprehensive.

Comprehensive: follows the ranking order returned by the search service.
Quality First: sort by recommendation level, recommendation time, and creation time in descending order.
Latest: sort by publish time in descending order; if tied, sort by recommendation level in descending order.
```

## Repository structure

```text
page-prd-writer/
├── SKILL.md
├── README.md
├── README.zh-CN.md
├── README.en.md
├── LICENSE
├── agents/
│   └── openai.yaml
└── references/
    └── output-pattern.md
```

## License

MIT
