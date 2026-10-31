# Build in 180

A personal agent skill for turning a short product-building window into a working, verified result its builder can explain.

[Read the skill](SKILL.md)

The default schedule is a planning heuristic, not a delivery guarantee. It covers setup, focused open-source selection, a real core flow, small verified integrations, ongoing understanding, and final restart/demonstration. Use the actual project and remaining clock.

## Use in Codex

Read `SKILL.md` directly in the supplied environment. For project-local skill discovery, place this folder under `.agents/skills/build-in-180` when the environment permits local skills:

```bash
git clone https://github.com/xz0831/build-in-180.git .agents/skills/build-in-180
```

Then invoke it with the actual task, deadline, available inputs and restrictions:

```text
$build-in-180
Help me deliver this task within the remaining time. Establish the mandatory user journey, choose a minimal implementation, verify and integrate small units, and keep me able to explain the result. Use only the environment and tools this task permits.
```

The skill does not require a particular framework, external model, paid service or personal setup. Existing tool availability and project rules determine what can run. Installation consumes the same work budget.

The skill includes a small pstack routing table and Codex adaptation guidance. It also tracks technical, intent and cognitive (understanding) debt throughout the build, using one existing work record and brief user walkthroughs. See [Storey's Triple Debt Model](https://arxiv.org/abs/2603.22106).

## Design influences

The workflow draws on pstack's [Experience First](https://github.com/cursor/plugins/blob/main/pstack/skills/principle-experience-first/SKILL.md), [Sequence Verifiable Units](https://github.com/cursor/plugins/blob/main/pstack/skills/principle-sequence-verifiable-units/SKILL.md), [Prototype](https://github.com/cursor/plugins/blob/main/pstack/skills/poteto-mode/playbooks/prototype.md) and [Sharpen](https://github.com/cursor/plugins/blob/main/pstack/skills/sharpen/SKILL.md). This repository is a separate personal workflow. It does not modify or bundle pstack.

It has structural validation and scenario review, not a demonstrated claim of better delivery outcomes. Improve it from actual use instead of adding rules for hypothetical failures.
