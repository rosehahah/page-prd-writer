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
