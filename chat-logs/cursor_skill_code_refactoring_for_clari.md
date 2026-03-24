# Skill code refactoring for clarity
_Exported on 3/24/2026 at 17:39:38 GMT+6 from Cursor (2.6.20)_

---

**User**

/create-skill  Help me create this skill for Cursor: Refactor this code for clarity and modularity.

---

**Cursor**

I can set this up, and first I need a few specifics so the skill is useful and auto-triggers correctly. Please answer these quick choices.

**Configure the new Cursor skill**

> **Where should I store this skill?**
> - Project skill (.cursor/skills/) for this repo ✔
> - Personal skill (~/.cursor/skills/) for all repos

> **What kind of refactoring should this skill focus on by default?**
> - General readability + modularity refactors
> - Frontend (React components/hooks)
> - Backend (Express/routes/services)
> - Full-stack patterns across frontend/backend ✔

> **How strict should the workflow be?**
> - Strict TDD (failing test -> minimal fix -> refactor) ✔
> - Lightweight refactor checklist (no mandatory tests first)

> **Preferred output style from the skill?**
> - Apply edits directly with brief rationale
> - Show short plan, then apply edits ✔
> - Review + suggestions only (no edits)

> **Which trigger phrases should activate this skill automatically?**
> - "refactor" ✔
> - "clarity/readability"
> - "modularity"
> - "clean up code"
> - "extract function/component/module"

Thanks — I’ll create a project skill focused on full-stack clarity/modularity refactors, with strict TDD and a “plan then patch” flow, triggered by `refactor`. I’m checking existing project skill structure first, then I’ll add the new skill file.

I’m now writing the `SKILL.md` with concise trigger logic, a strict TDD refactor workflow, and the plan-then-patch output format you selected.

Created the skill as a **project skill** at:

- `.cursor/skills/refactor-clarity-modularity/SKILL.md`

It now includes the preferences you selected:

- Full-stack refactoring scope
- Strict TDD workflow (`red -> green -> refactor`)
- `plan then patch` execution style
- Auto-trigger guidance for `refactor`

If you want, I can also add a small `examples.md` beside it with 2–3 concrete refactor scenarios (React component, Express route/service extraction, shared utility cleanup) so the skill is even more consistent in practice.

