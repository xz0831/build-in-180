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

In the first minutes, put the target in the existing repository instructions or work record without replacing existing rules: goal, mandatory behaviors and their acceptance checks, constraints, must-not-change boundaries and excluded scope. Reuse one readable work record for important decisions, accepted shortcuts and unresolved understanding gaps; use [this compact format](references/build-log.md) if none exists. Write decisions when made, then append their observed results. Label later reconstructions as retrospective; never invent an earlier rationale or time.

Frame each work unit with its goal, scope, must-not-change boundary and verification. This is the agent's job too: do not require the user to repeat a long prompt for every follow-up.

When data cannot reveal an operational constraint, ask the available domain contact a focused question. Record what was learned, its source, whether confirmed or assumed, and which requirement or design decision changed. Do not invent hidden context or treat a plausible explanation as an established fact.

Practitioners usually answer only what is asked, so a broad "what rules are missing?" question finds only the rules you already guessed. Before the first design, sweep these areas with one short question each, naming the actual columns, entities and numbers from the data:
1. Meaning and units: for each column that drives a constraint (capacity, hours, size, flags), is the listed value the usable value, and what does the flag oblige?
2. Unmarked exceptions: specific people, places, vehicles or items with a restriction the data does not record.
3. Legal, safety, contract or policy limits: rest, duration, time, load or exposure limits.
4. Current conditions: anything broken, closed, changed or temporary in this period.
5. Priorities: what matters most when not everything fits, and what the users must see.
If the user relays the domain contact, give them these questions ready to ask, one at a time. Record each answer, or "asked, nothing", per area. An area stays open until its own question is answered: if the reply addresses a different question, ask the original again, and list every open area in each check-in until it is closed. A confirmed constraint gets a check in the validator below; return to the contact when new data or a new rule appears.

A confirmed fact that corrects or adds to the supplied data (a stale flag, a person's restriction, a capacity that is not the usable one) belongs to the product: put it in code or in a versioned configuration file the product applies by default, with its source. Never only as an extra file inside the input data folder, because the next export of the data will not contain it. Prove it on an untouched copy of the supplied data folder.

## Find tools for a capability

Inspect supplied dependencies, examples and APIs first. Search for a specific missing capability, not a fashionable stack. Prefer official SDKs and established libraries over importing an entire application.

Timebox a tool search to roughly five minutes. Compare at most three plausible candidates on capability fit, runtime requirements, license, installation cost, maintenance and an actual minimal example. Read primary documentation for the version in use. Existing documentation tools can help; do not build a new toolchain just to do the search. Use public capability terms instead of transmitting private task data.

Every documented command must work from a fresh clone with no separate manual setup step: the entry script installs or locates what it needs on first use (for example a pinned interpreter through an available package runner), or degrades with a clear message for an optional part. Install or clone only when permitted. Run one representative input through the uncertain capability before broad implementation. Record the source and observed result. If the experiment fails, choose a requirement-preserving alternative or remove optional scope. Do not hide a mandatory dependency behind a mock. Revisit the search when new evidence changes the decision.

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

Before a long experiment or delegation, set its latest useful return time, leaving room for integration and verification. Recheck the clock after long operations and returned work. If that time passes, change the plan rather than silently waiting or accepting an unverified late change. Keep the actual deadline, next checkpoint and useful return time in the existing record; no new timer system is needed.

## Build, verify and integrate one small unit

Choose units that end in a useful user action, not just a file, screen or technical layer. Aim for a short cycle, often five to fifteen minutes, including verification and integration. Large mandatory units may need smaller experiments or a different decomposition.

For each unit:

1. Name the observable behavior, acceptance check and relevant failure condition.
2. Implement the smallest complete change for that behavior. Keep data ownership and important interfaces explicit.
3. Run the check on the matching artifact with representative input. Test the risky boundary; do not substitute a green build or a stub for a real required path. For planning or optimisation output, keep a validator separate from the algorithm that re-checks every stated and confirmed constraint, and run it on the supplied data, on at least one altered input (another period, generated data, an operator change) and at exact limit values (equal to the limit, one over, rounding). Every limit or weight the operator can change is a variant to validate: run the validator on the output produced under each operator setting the product offers, not only the defaults, and check limits that a later step applies (a cap, a trim, a ratio, an override after the solver) on the final output, not only inside the model.
4. Integrate with the current working product and repeat the core journey. Keep the last working state recoverable.
5. Update the work record and give a short progress explanation: elapsed/remaining time, current stage, what works, why a consequential choice was made, the observed check and the next action. Include one brief understanding question when appropriate; do not turn each unit into a full lesson.

Do not start broad fan-out on top of a broken shared base. Parallelize independent work only when its contracts and integration can fit before the next demonstration. Agent count, commits and token consumption are not completion checks.

Before delegated writing, name one owner, writable paths, shared interfaces, evidence required and latest useful return time. One integration owner coordinates shared contracts, dependency files and the work record. Workers return the exact change, commands, observed results and unresolved issues; the coordinator reads the actual diff and replays the relevant check before integration.

Treat new optional ideas as deferred until they replace an existing optional item or required behavior is secure. Keep critical interaction quality from the first working version. Reopen design alternatives only for a concrete unresolved decision.

## Pay down three debts during the build

[Storey's three debts](https://arxiv.org/abs/2603.22106) are technical debt in code and structure, intent debt in missing or stale goals and rationale, and cognitive debt in people's incomplete understanding. Here, "understanding debt" means cognitive debt. A working demonstration alone does not establish the user's understanding.

At meaningful checkpoints, make the input, processing/state, output and important failure path clear. Connect the chosen design to an actual requirement or observation. Distinguish verified behavior from untested cases and accepted shortcuts, including what would trigger revisiting them.

For a consequential choice, record the requirement or purpose, chosen approach, plausible alternative and why it lost, technical mechanism and code location, current process stage, and actual verification result tied to a revision. Identify user decisions separately from agent assumptions. For uncertain experiments, state the observation that would change the choice before running them. Link evidence instead of duplicating logs; skip routine edits that change no meaningful decision.

Review each agent diff against intent before integration. At each short unit boundary, normally every 10–15 active minutes, communicate the change and rotate one small question: why this approach, how input becomes output, what a failure does, or what a proposed change should affect. Keep it brief in the user's language. Also invite a full input/state/output/failure walkthrough after the first working journey, a major design change and before delivery. Show the actual code or behavior needed to explain the answer; distinguish observed mechanism from inferred historical intent.

Compare the user's prediction or explanation with the code and observed result. Resolve a mismatch with a focused trace or experiment and update the record. A log entry or agent explanation alone cannot repay cognitive debt. If the user has not responded, mark understanding pending, keep the question visible at the next checkpoint and continue independent work. Never invent their response, claim they understand, or require approval for every diff. At handoff, retain unresolved gaps and shortcuts rather than replacing them with confident prose.

Record shortcuts with their cost and revisit trigger in the same work record. Keep a reproducible run command and focused checks for the core path. Exclude secrets from the repository. Check handoff claims against the actual code and results.

In each check-in, name where the behavior lives (file and function), the check that proved it and its observed numbers, not only the story. Say what happens on a bad input and when inputs are read, once those exist.

Read the relevant part of [the decision question bank](references/decision-questions.md) when inputs can change during work, a rewrite must preserve behavior, an algorithm is compared, or domain context changes a requirement. Connect the chosen question to actual code and a small discriminating check, then revisit it after verification. Use it while making the decision, not only at handoff. Skip inapplicable cases; the bank does not require a rewrite, an optimizer or a concurrency framework.

## Use pstack selectively in Codex

This workflow owns the clock and scope; use pstack for the current problem, not as a second competing controller. Read the selected skill and necessary references only. If absent, follow the method here without delaying delivery to install a suite.

Carry the current goal, scope, writable paths, allowed models/tools, deadline, useful return time and required evidence into every skill invocation and worker brief, including nested calls and fallbacks. A model failure never authorizes a provider or model outside the allowed set. Apply a supported equivalent method or proceed sequentially when the original tool is unavailable; do not claim the original workflow ran unchanged.

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

Finishing the required journey early does not end the build. Use the remaining time, in this order: domain areas not yet asked; a clean start from a fresh clone in a new shell with the default interpreter and tools (no reused virtual environment, ignored files or warm caches); altered inputs and limit values through the validator; then the explanation rehearsal below. Do not declare the work complete or stop for approval while useful time remains. If the list is done before the last ten minutes, spend the idle time on the explanation rehearsal (another round of questions, a weak answer redone against the code, a gap's next check actually run) instead of waiting. In every late check-in state the remaining minutes, the open items and what the next one buys; recommend handing in during the last ten minutes, and leave that decision to the user.

Before the freeze, and whenever the work is done early, rehearse the follow-up questions with the user, one at a time, in their language: what happens if input data changes during a computation; how behavior was kept the same across a rewrite or refactor; what evidence shows the output is correct and on which data; which domain answer changed which code; why this algorithm and how it measured against the baseline (metric, data, numbers, seconds); what fails first at ten times the data or with a bad input; trace one operator change from the screen to the stored result. For a service, also ask: what happens with two overlapping requests, when an input file changes on disk while the service runs, and what an already open end-user page shows after the plan changes. Let the user answer first, then show the file:line, test name and observed numbers that settle it, and correct the gap. End every answer, in the rehearsal and on the card, with one line naming its weakness (what the mechanism does not cover), its risk (what goes wrong in use if that weakness is hit) and the next check that would test it; ask the user to say that line too, and correct it like the rest. A named gap with a concrete next check is worth more than a confident answer that misses one. Keep the settled answers as the explanation card in the work record ([format](references/build-log.md)).

Freeze optional work near the end. Restart from the documented entry point and complete the required journey again. Tie the check to an identifiable artifact revision (commit or content digest), run command, representative input, configuration names and observed output; never record credential values. After any later change, repeat affected checks before carrying the verdict forward. If packaging or deployment is part of the authorized work, inspect that actual output too. Check saved results and important failures, and state material limits. Use the work record to explain the product's purpose, choices and alternatives, input/state/output/failure path, and known limitations from the work actually completed.

Use only available and permitted models, tools, network paths and credentials. Follow the task's publication and data-transfer rules. This skill does not authorize extra providers, personal host access or publication. It works without pstack; use relevant installed skills when they help, leaving upstream unchanged.
