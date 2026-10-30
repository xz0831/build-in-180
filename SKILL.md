---
name: build-in-180
description: Build a working product under a short deadline, usually 180 minutes. Use for hackathon or timed prototype work that needs scope control, small verified integrations, practical tool selection, and an explainable result.
---

# Build in 180

Deliver the required user journey within the actual remaining time. Keep the participant able to explain the implemented behavior and its evidence. Adapt the budget to the task, rather than treating this schedule as permission to reset its clock.

## Establish the target

Read the task, supplied files, actual environment and restrictions. Identify the user, triggering situation, input, useful output and observable success. Separate mandatory requirements, one possible differentiator and deferred ideas. Do not convert every suggestion into current scope.

Use the platform clock or an observed start/deadline. If the start is unknown, ask once. Setup, research, integration and verification all consume this budget. Preserve active work and timers.

Before committing to a design, spend at most a few minutes identifying the professional check that matters most, the original evidence needed, a concrete method, and an outcome that could disprove the approach. Choose only checks that improve this submission. Leave genuine product choices with the participant.

## Find tools for a capability

Inspect supplied dependencies, examples and APIs first. Search for a specific missing capability, not a fashionable stack. Prefer official SDKs and established libraries over importing an entire application.

Timebox a tool search to roughly five minutes. Compare at most three plausible candidates on capability fit, runtime requirements, license, installation cost, maintenance and an actual minimal example. Read primary documentation for the version in use. Existing documentation tools can help; do not build a new toolchain just to do the search. Use public capability terms instead of transmitting private task data.

Install or clone only when permitted. Run one representative input through the uncertain capability before broad implementation. Record the source and observed result. If the experiment fails, choose a requirement-preserving alternative or remove optional scope. Do not hide a mandatory dependency behind a mock. Revisit the search when new evidence changes the decision.

## Use an observable budget

For a fresh 180-minute attempt, start with this allocation and adjust to its risks:

| Elapsed minutes | Required checkpoint |
| --- | --- |
| 0-15 | Necessary setup, task understanding, core journey and highest-risk dependency |
| 15-40 | One real input completes the core journey with real required processing |
| 40-105 | Mandatory behavior implemented and integrated in small units |
| 105-135 | Important failures, persistence, return paths and realistic inputs exercised |
| 135-160 | Main interaction refined; one useful distinction only if required checks pass |
| 160-180 | Feature expansion stopped; restart, final demonstration, deliverables and explanation checked |

A missed checkpoint calls for resolving the blocking dependency or reducing optional scope. Mandatory behavior still has to work. Recalculate from the actual time left instead of restarting this plan. Reserve a separate explanation period only if the task provides one; never borrow from a fixed cutoff.

## Build, verify and integrate one small unit

Choose units that end in a useful user action, not just a file, screen or technical layer. Aim for a short cycle, often five to fifteen minutes, including verification and integration. Large mandatory units may need smaller experiments or a different decomposition.

For each unit:

1. Name the observable behavior, acceptance check and relevant failure condition.
2. Implement the smallest complete change for that behavior. Keep data ownership and important interfaces explicit.
3. Run the check on the matching artifact with representative input. Test the risky boundary; do not substitute a green build or a stub for a real required path.
4. Integrate with the current working product and repeat the core journey. Keep the last working state recoverable.
5. Carry forward a compact note of what works, the decision/evidence that changed, and remaining gaps. Use the existing work record, not another reporting system.

Do not start broad fan-out on top of a broken shared base. Parallelize independent work only when its contracts and integration can fit before the next demonstration. Agent count, commits and token consumption are not completion checks.

Treat new optional ideas as deferred until they replace an existing optional item or required behavior is secure. Keep critical interaction quality from the first working version. Reopen design alternatives only for a concrete unresolved decision.

## Keep understanding and evidence current

At meaningful checkpoints, make the input, processing/state, output and important failure path clear. Connect the chosen design to an actual requirement or observation. Distinguish verified behavior from untested cases and accepted shortcuts, including what would trigger revisiting them.

In an interactive learning session, invite a brief explanation in the participant's own words after the first working journey, after a major design change and before final delivery. Acknowledge uncertainty and resolve it with a code trace, a small experiment or a reproduction. Do not answer for the participant or claim understanding merely because they accepted an explanation. Routine implementation should not wait on repeated approval rituals.

## Finish the actual artifact

Freeze optional work near the end. Restart from the documented entry point and complete the required journey again. Check saved results and important failures, retain actual commands/results, and state material limits. If the task has an AI-free question period, the participant answers from the work they actually did; stop coaching answers during that period.

Use only available and permitted models, tools, network paths and credentials. Follow the task's publication and data-transfer rules. This skill does not authorize extra providers, personal host access or publication. It works without pstack; use relevant installed skills when they help, leaving upstream unchanged.
