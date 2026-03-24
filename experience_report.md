# Experience Report - AI Cart Manager

Date: 2026-03-24

## 1. Project Context

AI Cart Manager is developed as a modular full-stack project with:

- `AI-Cart-Frontend` (React + Vite)
- `AI-Cart-Backend` (Express + Jest)
- workflow/rules guidance under `context/`

The team followed a structure-first approach: separating API integration, UI components, and validation logic to keep each module focused.

## 2. Work Completed

Key outcomes completed during recent development:

- Added/improved backend test coverage for cart add/remove behavior.
- Improved frontend UI structure and readability.
- Integrated and fixed inline form validation behavior.
- Refactored frontend to separate:
  - API methods from component logic
  - form component from form validation logic
- Added a root-level project `README.md` with setup, run, test, and troubleshooting instructions.

## 3. Engineering Practices Applied

- **Modular architecture:** Business logic, UI components, and API helpers were separated into dedicated files.
- **TDD alignment:** Backend improvements were done with tests as the primary safety net.
- **Small iterative changes:** Large refactors were broken into minimal, verifiable steps.
- **Verification discipline:** Build/test checks were run after substantial changes.

## 4. Challenges Encountered

- **Validation not triggering as expected:** Browser-native form validation prevented submit handlers from running, so custom validation state did not update.
- **Code drift during refactor flow:** Previously expected validation code was not present in one refactor step, requiring confirmation and explicit user direction.
- **Cross-file consistency:** Moving logic across files required careful imports and behavior checks to avoid regressions.

## 5. Lessons Learned

- Keep validation strategy consistent: either native HTML validation or custom React validation, not both competing.
- Splitting UI and logic early reduces complexity and makes bug fixing faster.
- Short verification loops (`build`/`test` after each change) significantly reduce integration risk.
- Explicit workflow rules (`context/workflows/`*) help maintain consistent implementation quality.

## 6. Current State

- Frontend and backend structures are modular and easier to maintain.
- Core cart flows (add/remove/view/update) are covered by API routes and test scaffolding.
- Root setup documentation is now present and suitable for onboarding.

## 7. Recommended Next Steps

1. Add a dedicated frontend unit-test layer (component/validation tests) to complement Playwright E2E coverage.
2. Add API contract examples (sample request/response payloads) to docs.
3. Standardize report templates under `chat-logs/` for recurring retrospectives.

