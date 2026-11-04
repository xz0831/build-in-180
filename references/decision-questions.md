# Questions tied to real decisions

Read only the situation relevant to the current work. Select one short question at a checkpoint, ask the user to explain or predict the behavior, and check it against code and observation. Keep the result in the existing build record. An untested claim or unanswered question remains open. These are design prompts, not ready-made answers about an implementation that has not been inspected.

## Inputs change while a computation is running

Ask: Which input state does this run see? If data changes before completion, can an old result appear current? Where is that prevented, and what check exercised it?

Choose consistency behavior appropriate to the product. For example, capture an immutable versioned snapshot and label its result with that version. Then choose whether a newer version cancels work, discards the old result, or retains it visibly as stale. Explain why that policy fits. A snapshot still needs a publication/freshness policy; cancellation alone does not establish that partially read inputs were consistent. A synchronous or transaction-based product may use a different justified mechanism.

Exercise the actual boundary with controlled ordering: capture/start -> change source data -> finish -> inspect output version and publication state. Prefer a barrier or controlled deferred operation to hoping a sleep triggers the race. Check that inputs are not mixed and that the chosen stale-result policy holds. Describe what was tested and what remains outside that case.

## A rewrite or language port must preserve behavior

Ask: What observable behavior must remain the same? Which shared inputs were run through both versions, what differed, and what is still untested?

Define the contract before comparing: values, ordering, errors, boundaries and, where relevant, randomness or tie handling. Keep the original implementation or its identified outputs available as a reference. Run differential checks on identical inputs, retaining representative and boundary fixtures and useful invariant checks. Declare any numeric tolerance or normalization before seeing the comparison; do not mask a discrepancy by adjusting it afterwards. Use property-based cases when existing tooling and the risk justify them.

Compare against independent expected behavior too: agreement between two implementations can preserve the same bug. State the tested input range and actual mismatches. Passing sampled checks is evidence within that coverage, not a proof of equivalence for all inputs. Do not start an unnecessary rewrite simply to demonstrate this method.

## An approach is called better, faster or optimal

Ask: Better by which metric, subject to which constraints, on what inputs and against what baseline? What result would make us choose differently?

Separate feasibility from solution quality and runtime. Use the same identified inputs, constraints, scoring rule, relevant settings and comparable compute limits for both approaches; record seeds and variability when relevant. Check outputs satisfy the requirements before comparing scores. Identify the actual library/solver version and configuration. An open-source reference is a baseline, not automatically ground truth; a heuristic returning a valid candidate does not establish global optimality.

Retain commands, observed values and input/output artifacts. Distinguish a measured improvement on these cases from a general guarantee. If no appropriate comparison fits the budget, describe the implemented heuristic and its limitations rather than inventing a ranking.

## Operational context changes the product

Ask: What could the supplied data not tell us? What did the domain contact add, how reliable is it, and exactly what changed in the product because of it?

Track the chain: question -> source response -> confirmed constraint or assumption -> affected decision/code -> observable acceptance check. Resolve a conflict with the stated requirements instead of silently replacing them. If no domain contact is available, label the assumption and choose a reversible bounded design where possible.

At a checkpoint, explain one such chain in the user's own words, including why an alternative was excluded. Technical correctness of the implementation does not by itself establish that it serves the right operational need.
