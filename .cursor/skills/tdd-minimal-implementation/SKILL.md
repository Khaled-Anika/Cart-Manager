---
name: tdd-minimal-implementation
description: Enforces strict test-driven development by writing a failing test first, implementing the smallest code change to pass, then refactoring safely. Use when implementing features, fixing bugs, or changing behavior where correctness matters and the user wants a red-green-refactor workflow with coverage and commit guidance.
---

# TDD Minimal Implementation

## When to apply

Apply this skill when the user asks for:
- "write tests first"
- "TDD"
- "red-green-refactor"
- bug fixes or feature work that should be driven by tests

## Core rules

1. Never implement behavior before a failing test exists for that behavior.
2. Keep each cycle small: one behavior, one failing test, one minimal fix.
3. Implement only enough code to make the current failing test pass.
4. Refactor only while tests are green.
5. Do not broaden scope unless the user asks.

## Workflow

Copy this checklist and keep it updated during implementation:

```markdown
TDD Progress
- [ ] Define one small behavior
- [ ] Add/adjust one test that fails for the right reason
- [ ] Run tests and confirm red
- [ ] Implement minimal code to pass
- [ ] Run tests and confirm green
- [ ] Refactor safely (optional)
- [ ] Re-run relevant tests
- [ ] Check coverage expectations
- [ ] Prepare commit guidance
```

### 1) Define behavior

Describe the exact behavior in one sentence before touching code.

### 2) Create failing test (Red)

- Add or update the smallest relevant test.
- Confirm failure is caused by missing/incorrect behavior (not test setup issues).
- If the test fails for the wrong reason, fix the test first.

### 3) Minimal implementation (Green)

- Change as little production code as possible.
- Prefer simple logic over abstractions in the first passing version.
- Re-run targeted tests, then broader suite as appropriate.

### 4) Refactor

- Refactor only after green.
- Keep refactors behavior-preserving.
- Re-run tests immediately after each meaningful refactor step.

### 5) Coverage checks

- Verify changed paths are covered by tests.
- If project has coverage tooling, run it and report results.
- If coverage drops unexpectedly, add focused tests or explain tradeoff.

### 6) Commit guidance

Before proposing a commit:
- Ensure tests pass.
- Summarize behavior change and why it matters.
- Recommend commit message focused on intent, e.g.:

```text
test(cart): add failing test for quantity floor validation

fix(cart): enforce minimum quantity of one to satisfy cart constraints
```

## Output format

When reporting progress, use:

1. **Red**: which test was added and how it failed
2. **Green**: minimal code change that made it pass
3. **Refactor**: what was cleaned up (or "none")
4. **Validation**: tests run and outcome
5. **Coverage**: result or note if unavailable

## Guardrails

- Do not skip directly to implementation.
- Do not batch multiple behaviors into one test cycle unless explicitly requested.
- Do not claim TDD completion without showing both failing and passing test evidence.
