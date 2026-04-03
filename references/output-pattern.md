# Output Pattern

Use this reference when writing page requirement docs in a shorter, more operational style.

## Default Short Form

Use this structure unless the user explicitly asks for a detailed PRD:

```md
1、<功能点>

<规则 1>
<规则 2>
<规则 3>

2、<功能点>

<规则 1>
<规则 2>
```

Write each rule as a short sentence. One page usually needs 3-8 items.

## Good Short Example

```md
1、列表排序

排序选项包括：综合排序、质量优先、最近发布。默认选中综合排序。

综合排序：沿用搜索中台返回顺序。
质量优先：按推荐等级、推荐时间、创建时间倒序。
最近发布：按发布时间倒序，相同发布时间再按推荐等级倒序。
```

This is the target density: one function block, then only the rules that matter.

## When to Include Entry or Permission

Include `入口` or `权限` only when one of these is true:

- The user explicitly asks for a full PRD structure
- The page has real access differences
- The route or source path itself is important to the requirement

Otherwise, skip them.

## Detailed Form Fallback

Use the longer form only when the user explicitly asks for detail or the page is a complex publish/edit form:

```md
用户直接进行 <动作>。

入口：...
权限：...

<模块名>：
规则...
规则...
```

## What to Keep

- Sorting rules
- Filter options and combined-effect logic
- Tab switching logic
- Search behavior
- URL state / parameter sync
- Submit / delete / copy / download consequences
- Empty states
- Data source mapping when it affects output

## What to Cut

- Decorative layout and visual style
- Repeated statements like "展示标题" or "展示按钮"
- Purely static copy that does not affect behavior
- Long explanations of obvious page structure
- Repeating the same filter logic in multiple places

## Do

- Group by feature, not by every visible block.
- Prefer concise numbered items.
- Preserve the user's terminology and sentence rhythm.
- Use exact strings only when the copy itself is part of the rule.

## Don't

- Do not default to exhaustive field inventory.
- Do not force every answer into `入口 / 权限 / 模块展示`.
- Do not invent backend logic, validation, or future plans.
- Do not turn a simple page into a long-form PRD unless the user explicitly wants that.
