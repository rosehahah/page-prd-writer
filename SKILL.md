---
name: page-prd-writer
description: Write concise product requirement notes for a specific page by inspecting the real page artifact and mirroring the user's existing style. Default to short, feature-based output instead of exhaustive field-by-field inventory. Use when the user asks for a PRD, 需求文档, 需求细则, 页面需求, or wants page logic summarized from code, a local route, or a prototype, especially when they want the result to be 简洁明了, 不要废话, or close to an existing sample style.
---

# Page PRD Writer

Write page requirement docs that are short by default. The goal is "enough to execute", not "everything visible on the screen".

## Workflow

1. Read the source artifact first.
   - If the user gives a route or page path, locate the page component and related constants.
   - If the user gives a prototype or screenshot, inspect that artifact before writing.
   - If both UI and code exist, treat code as the rule source.

2. Extract only product-relevant logic.
   - Focus on search, tabs, filters, sorting, list rules, card actions, submit logic, empty states, URL sync, and data mapping.
   - Keep exact copy only when the wording changes behavior or decision.
   - Ignore decorative layout details unless the user explicitly asks for them.

3. Group by function, not by every visible block.
   - Prefer `1、功能点` style output.
   - Merge related logic into the same item.
   - Do not force `入口` / `权限` / `模块展示` sections on every page.

4. Switch to detailed mode only when needed.
   - Use detailed output only if the user explicitly asks for `详细版` / `完整PRD` / `逐字段` / `全量需求`, or the page is a complex publish form.
   - In detailed mode, still stay compact and skip decorative content.

5. Cut before returning.
   - Remove repeated explanations.
   - Remove lines that only say something exists but do not explain rules.
   - Omit assumptions unless the user explicitly asks to补齐.

## Default Output Rules

- Prefer Chinese unless the user asks otherwise.
- Default to 3-8 numbered items for one page.
- Each item should contain the rule itself, not a long preface.
- Mention limits, options, sorting, filtering, URL handling, result states, and action consequences when they matter.
- Do not automatically include `入口` / `权限` unless the user asks for them or the page truly depends on access differences.
- Do not restate obvious UI chrome like "展示标题" or "展示按钮" unless there is logic tied to it.
- Do not explain product value, design rationale, implementation effort, or future-state ideas unless asked.

## Detailed Mode Rules

- If the user explicitly asks for a detailed PRD, follow their structure first.
- Keep exact strings for placeholders, button copy, and error copy when those strings matter.
- Cover required state, options, limits, success/failure, preview, and delete logic only when the page defines them.

## Resources

- Use [references/output-pattern.md](references/output-pattern.md) for the short-form skeleton, detailed-form fallback, and cut list.
