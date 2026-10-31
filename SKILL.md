---
name: build-in-180
description: Build a working product under a short deadline, usually 180 minutes. Use for focused product or prototype work that needs scope control, small verified integrations, practical tool selection, and an explainable result.
---

# Build in 180

Deliver the required user journey within the actual remaining time. Keep the person building the product able to explain its implemented behavior and evidence. Adapt the budget to the project, rather than treating this schedule as permission to reset its clock.

## Establish the target

Read the task, supplied files, actual environment and restrictions. Identify the user, triggering situation, input, useful output and observable success. Separate mandatory requirements, one possible differentiator and deferred ideas. Do not convert every suggestion into current scope.

Use an observed start/deadline. If the start is unknown, ask once. Setup, research, integration and verification all consume this budget. Preserve active work and timers.

Before committing to a design, spend at most a few minutes identifying the professional check that matters most, the original evidence needed, a concrete method, and an outcome that could disprove the approach. Choose only checks that improve this product. Leave genuine product choices with the user.

In the first minutes, put the target in the existing repository instructions or work record without replacing existing rules: goal, mandatory behaviors and their acceptance checks, constraints, must-not-change boundaries and excluded scope. Reuse that record for decisions, accepted shortcuts and unresolved understanding gaps. A useful decision line is: "Choose X because Y; defer Z because W; user choice or agent assumption." Surface consequential assumptions at the next checkpoint; do not stall routine implementation for approval.

Frame each work unit with its goal, scope, must-not-change boundary and verification. This is the agent's job too: do not require the user to repeat a long prompt for every follow-up.

## Find tools for a capability

Inspect supplied dependencies, examples and APIs first. Search for a specific missing capability, not a fashionable stack. Prefer official SDKs and established libraries over importing an entire application.

Timebox a tool search to roughly five minutes. Compare at most three plausible candidates on capability fit, runtime requirements, license, installation cost, maintenance and an actual minimal example. Read primary documentation for the version in use. Existing documentation tools can help; do not build a new toolchain just to do the search. Use public capability terms instead of transmitting private task data.

Install or clone only when permitted. Run one representative input through the uncertain capability before broad implementation. Record the source and observed result. If the experiment fails, choose a requirement-preserving alternative or remove optional scope. Do not hide a mandatory dependency behind a mock. Revisit the search when new evidence changes the decision.

## Use an observable budget

For a fresh 180-minute build window, start with this allocation and adjust to its risks:

| Elapsed minutes | Required checkpoint |
| --- | --- |
| 0-15 | Necessary setup, task understanding, core journey and highest-risk dependency |
| 15-40 | One real input completes the core journey with real required processing |
| 40-105 | Mandatory behavior implemented and integrated in small units |
| 105-135 | Important failures, persistence, return paths and realistic inputs exercised |
| 135-160 | Main interaction refined; one useful distinction only if required checks pass |
| 160-180 | Feature expansion stopped; restart, final demonstration, deliverables and explanation checked |

A missed checkpoint calls for resolving the blocking dependency or reducing optional scope. Mandatory behavior still has to work. Recalculate from the actual time left instead of restarting this plan. Include explanation and handoff within the available budget.

Observe the clock at the start and after each unit; report elapsed and remaining time from actual readings. Keep a single coordinating session. If a unit consumes its budget without demonstrable progress, stop expanding it and split the work or test the blocking premise.

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

## Pay down three debts during the build

[Storey's three debts](https://arxiv.org/abs/2603.22106) are technical debt in code and structure, intent debt in missing or stale goals and rationale, and cognitive debt in people's incomplete understanding. Here, "understanding debt" means cognitive debt. A working demonstration alone does not establish the user's understanding.

At meaningful checkpoints, make the input, processing/state, output and important failure path clear. Connect the chosen design to an actual requirement or observation. Distinguish verified behavior from untested cases and accepted shortcuts, including what would trigger revisiting them.

Review each agent diff against intent before integration. At the first working journey, after a major design change and before delivery, invite the user to explain the input, state, output and one failure path in their own words. Before a consequential experiment, ask for a brief prediction when they are available; compare it with the observed result. Resolve mismatches with a code trace or a small experiment, recording remaining gaps honestly. Do not answer for the user or claim understanding merely because they accepted an explanation. Continue independent work while awaiting an explanation; do not invent their response or create repeated approval rituals.

Record shortcuts with their cost and revisit trigger in the same work record. Keep a reproducible run command and focused checks for the core path. Exclude secrets from the repository. Check handoff claims against the actual code and results.

## Use pstack selectively in Codex

This workflow owns the clock and scope; use pstack for the current problem, not as a second competing controller. Read the selected skill and necessary references only. If absent, follow the method here without delaying delivery to install a suite.

| Situation | Useful pstack method |
| --- | --- |
| Product tradeoff | `principle-experience-first`: protect the user's core outcome |
| Uncertain dependency or interaction | Prototype playbook: test one real input before broad implementation |
| Work too large to integrate | `principle-sequence-verifiable-units`: split by observable behavior |
| Ready to claim success | `principle-prove-it-works`: run the matching real artifact |
| Tempted by extra layers | `principle-laziness-protocol`: choose the smallest complete change |
| Two fixes fail under the same premise | `principle-attack-the-premise`: test that premise directly |

Use a focused `how` or `why` walkthrough to close an actual understanding gap. Broad arenas, swarms and multi-review loops are not default setup steps; use them only when a specific unresolved risk and the remaining budget justify them.

Inspect the installed Codex capabilities and the user's allowed models. Do not pass Cursor `Task` arguments or other-provider model slugs to Codex. Apply constraints through instructions Codex actually reads; installing pstack or writing a Cursor `.mdc` file does not prove that. When GPT-6.1 Sol is selected and effort is configurable, medium is a starting heuristic; raise it for a bounded difficult decision if needed. This is not a measured performance guarantee. Use native supported tools, or work sequentially when delegation is unavailable.

## Finish the actual artifact

Freeze optional work near the end. Restart from the documented entry point and complete the required journey again. Check saved results and important failures, retain actual commands/results, and state material limits. Ensure the handoff explains the product's purpose, operation and known limitations from the work actually completed.

Use only available and permitted models, tools, network paths and credentials. Follow the task's publication and data-transfer rules. This skill does not authorize extra providers, personal host access or publication. It works without pstack; use relevant installed skills when they help, leaving upstream unchanged.
