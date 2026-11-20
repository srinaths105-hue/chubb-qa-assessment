# Chubb QA Assessment — AI Working Journal

## AI assistance used
AI assistance was used for troubleshooting commands, interpreting test output, organizing findings, and drafting assessment documentation. All execution claims below are based on terminal output supplied during the assessment; AI did not run commands on the local Windows machine.

## Decision log
| Situation | AI suggestion | Human verification / decision |
|---|---|---|
| Docker and frontend setup | Generate missing OpenAPI TypeScript client with `npm run generate:api` and rebuild UI. | Accepted after observing missing generated-module error; generation completed and dashboard loaded. |
| Java compilation | Build services while skipping tests to unblock local application startup. | Accepted as a temporary setup workaround only. Explicitly documented that backend tests did not pass. |
| Frontend test execution | Install local npm dependencies, then run `npm test`. | Accepted; Vitest executed 266 tests, with 243 passes and 23 failures. |
| Failure analysis | Investigate `localStorage` environment warnings as a possible shared cause for 17 failures. | Treated as a hypothesis, not a confirmed root cause or application bug. |
| Claim wizard failures | Investigate six validation/accessibility assertions. | Left unresolved rather than altering tests solely to obtain green results. |
| Source control | Exclude dependencies/build outputs and review credentials before pushing. | Added `.gitignore` and reviewed configuration; private repository created. |

## Accepted, challenged, and overridden AI output
- **Accepted:** commands that were confirmed by local terminal results; documentation structure and evidence-based risk prioritization.
- **Challenged:** any inference that container health, Maven packaging with skipped tests, or 243 passing frontend tests implied the entire system passed.
- **Overridden / deferred:** broad recommendations to fix all 23 frontend failures before submission. Time was instead prioritized for transparent reporting of unresolved failures.

## Limitations and integrity
- AI-generated text is a draft and must be reviewed for accuracy against the local project and assignment instructions.
- No claim is made that AI independently executed, fixed, or verified the unresolved tests.
- Any additional tests, bug fixes, or reruns must be recorded with actual output before the report is updated.
