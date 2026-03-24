# Test-driven development for skill creation
_Exported on 3/24/2026 at 17:39:58 GMT+6 from Cursor (2.6.20)_

---

**User**

/create-skill  Write failing tests first, then implement minimal code.

---

**Cursor**

I’ll create this as a reusable Cursor skill focused on strict TDD (`failing test -> minimal implementation`). First I need a couple of choices from you so I place and format it exactly right.

**TDD Skill Setup**

> **Where should I store this skill?**
> - Project skill (.cursor/skills/) for this repo ✔
> - Personal skill (~/.cursor/skills/) for all repos

> **What should the skill enforce by default?**
> - Strict TDD loop only (red -> green -> refactor, minimal code)
> - TDD loop + coverage checks + commit guidance ✔

> **Pick a skill name**
> - tdd-minimal-implementation ✔
> - red-green-refactor
> - I want a custom name

Thanks — I’ll add a project skill at `.cursor/skills/tdd-minimal-implementation/` with the stricter “TDD + coverage + commit guidance” workflow, using concise steps and trigger-based description for auto-discovery.

Created the project skill at:

- `.cursor/skills/tdd-minimal-implementation/SKILL.md`

What it includes:
- Strict **red -> green -> refactor** enforcement
- “Minimal code only” implementation rule
- A reusable **TDD progress checklist**
- **Coverage check** expectations
- **Commit guidance** section with intent-focused examples
- Structured reporting format (`Red`, `Green`, `Refactor`, `Validation`, `Coverage`)

If you want, I can also add a second supporting file with framework-specific commands (for your repo’s exact test and coverage commands) so the skill can run fully prescriptive steps.

