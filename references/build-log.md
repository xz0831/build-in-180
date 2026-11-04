# One readable build record

Reuse the project's existing record. Otherwise create `BUILD_LOG.md` in the working project, using the shape below. The agent maintains it; the user should be able to scan it during the build. Keep decisions short, link evidence and append corrections without erasing the original failure. Record actual observations, never fabricated times, approvals or understanding.

```markdown
# Build log

Goal / core user journey:
Required outcomes and acceptance checks:
Constraints / must not change / out of scope:
Actual start / deadline / timezone:
Current stage / next checkpoint / latest useful return time:

## Important decisions

### D1 | observed time, elapsed/remaining | stage | user choice or agent assumption
- Purpose and choice: requirement served; what was chosen; new domain context/source and confirmed or assumed status when relevant.
- Alternative and technical reason: what else was plausible; why this tradeoff fits now.
- Mechanism and evidence: code location; artifact revision; command/input; actual result or not yet checked.
- Debt and follow-up: shortcut, cost and revisit trigger; user explanation/prediction or understanding pending; any correction.

## Current checkpoint

Observed time / working behavior / evidence / next action:
One short question and the user's actual response, or pending:
Open understanding gaps and accepted limitations:
Applicable decision question: input-change consistency, rewrite equivalence, comparison evidence or domain-context impact; link the actual check.

## Domain sweep

Area | question asked | answer, "asked, nothing" or open | constraint, where the product applies it, and its validator check
Meaning and units / unmarked exceptions / legal and policy limits / current conditions / priorities

## Explanation card

One line per follow-up question: the short answer, file:line or function, test or command, observed numbers, what was not tested and the next check.
Input change during computation / overlapping requests and open pages / behavior kept across a rewrite / evidence and data / domain answer -> code / algorithm vs baseline / first failure at 10x or bad input / one operator change end to end

## Final verified state

Artifact revision / run command / input / configuration names / observed result:
Core flow: input -> processing/state -> output; important failure path:
Choices and alternatives: link the relevant decision entries.
Open gaps, shortcuts and what a later change would invalidate:
```

Explain one consequential choice and ask one brief question at a unit boundary. Rotate purpose, mechanism, tradeoff and failure behavior. The user's own explanation is evidence of understanding only to the extent checked against the actual artifact. Silence, agreement or the agent's generated answer is not that evidence. Continue independent work and carry a pending question forward without repeatedly interrupting.

Technical debt: preserve a runnable core and record accepted costs. Intent debt: preserve the actual goal, alternatives and reasoning at decision time. Cognitive debt: find and resolve the person's specific understanding gaps. A completed record does not by itself establish any of these outcomes.
