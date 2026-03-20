---
name: refactor-clarity-modularity
description: Refactors full-stack code for clarity and modularity while preserving behavior. Use when the user asks to refactor code, improve readability, simplify structure, or make logic more modular, especially with phrases like "refactor".
---

# Refactor for Clarity and Modularity

## When to apply

Apply this skill when the user asks for:
- "refactor"
- improved clarity or readability
- more modular code
- extracting functions/components/services without changing behavior

## Core goals

1. Preserve behavior while improving structure.
2. Prefer small, reversible changes over large rewrites.
3. Separate concerns into focused modules with clear boundaries.
4. Keep naming explicit and intent-revealing.
5. Follow strict TDD for behavior-affecting changes.

## Workflow

Copy this checklist and keep it updated during implementation:

```markdown
Refactor Progress
- [ ] Identify the target code smell and scope
- [ ] Write a short plan before edits
- [ ] Add or update a test that fails first (if behavior could change)
- [ ] Run tests and confirm red
- [ ] Apply the smallest refactor/implementation step
- [ ] Run tests and confirm green
- [ ] Continue in small cycles until objective is met
- [ ] Final pass for naming, duplication, and module boundaries
- [ ] Run relevant test suite
```

### 1) Identify and constrain scope

- Define one concrete objective (e.g., "extract pricing rules from route handler").
- List files likely affected and avoid touching unrelated areas.

### 2) Plan first, then patch

Before editing, provide a short plan:
- current problem
- proposed module/function boundaries
- smallest first step

Then apply code changes immediately after plan approval (or directly if user asked to proceed).

### 3) TDD cycle (strict)

For each behavior-affecting step:
1. Add/update one focused test.
2. Confirm the test fails for the intended reason.
3. Make the minimal production change.
4. Re-run tests until green.
5. Refactor safely while tests remain green.

For pure mechanical refactors (rename/move with no behavior change), still run tests after each meaningful step.

### 4) Modularity heuristics

- Extract when a block has mixed responsibilities.
- Keep functions/components small and single-purpose.
- Move domain logic out of controllers/routes/UI components.
- Prefer composition over deep conditionals.
- Keep public interfaces minimal and explicit.

### 5) Clarity heuristics

- Replace ambiguous names with intent-based names.
- Remove dead code, duplicate branches, and needless indirection.
- Add short comments only for non-obvious decisions.
- Keep error handling close to failure points.

## Output format

When responding during work, use this order:

1. **Plan**: concise 2-4 step refactor plan
2. **Red**: test added/updated and failing signal
3. **Green**: minimal change to pass tests
4. **Refactor**: structure/naming improvements made
5. **Validation**: tests run and result

## Guardrails

- Do not change user-visible behavior unless requested.
- Do not combine unrelated refactors in one pass.
- Do not skip tests for behavior-sensitive changes.
- Do not introduce new dependencies unless the user agrees.
