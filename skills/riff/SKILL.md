---
name: riff
description: Explore distinct UI or UX design options with rendered mocks, checked interaction analogs, explicit tradeoffs, and a recommendation. Use for a riff, design exploration, alternative UI paradigms, or another round of an existing design decision. Supports implementing a chosen take when requested; does not turn a narrow fix into a redesign.
---

# Riff

Answer one design question with distinct, visible alternatives. Ground them in the current product, borrow interaction patterns deliberately, and help the user pick or combine them.

A **riff** is the whole exploration. A **take** is one design, named after its interaction pattern. A **round** is one set of takes and the response to them. A **proof** is a short, evidence-linked argument for a take, not a claim of mathematical certainty or measured usability.

## Pin the question

State the question in one sentence and identify its level:

- **Flow:** steps, actors, and handoffs.
- **Paradigm:** how selection, comparison, navigation, or another main interaction works.
- **Screen:** layout, controls, and copy within a settled paradigm.

Match the user's requested level. If it is unclear, start higher and narrow in later rounds. Preserve the requested scope: a riff on a control should not silently redesign the page.

Read the existing decision log before proposing takes. Keep a short log in the repository's designated local scratch location, or beside the local deliverable if there is no repository. Record the question, level, constraints, picks, and rejections. Follow local instructions about what belongs in version control.

## Ground the work

Read the current screen or flow's code and applicable repository instructions. Inspect the running UI when available. Cite the files or supplied reference material that establish the baseline.

Read the product's component inventory, design tokens, and design guidance. Reuse those components and tokens in the mocks. If the task is a new product or code is unavailable, use the supplied brief or screenshots and explicitly state the missing baseline. Do not invent existing product behavior or pretend a proposed component already exists.

List two to five jobs the person using this view needs to do. Every element in a take should serve one of them. Use realistic synthetic content, clearly identified outside the mock; never copy private customer, employee, or production records into deliverables.

## Find useful analogs

Read [references/analogs.md](references/analogs.md) and use the correspondence check in [references/proof.md](references/proof.md). Include products the user names and look beyond the product's category.

Verify current behavior through accessible product UI or primary documentation. Link the source for each checked claim. Label unchecked ideas as hypotheses, not observations. If browsing is unavailable, disclose that limitation and avoid treating remembered behavior as evidence.

Prefer analogs matching at least five of the seven correspondence dimensions. The count is a heuristic: a critical mismatch can outweigh the total. If none qualify, say so; use the grounded jobs and constraints without forcing an analogy.

Choose analogs and continue into the mocks without a separate approval stop, unless the user requested one. Show the relevant matches and limits alongside the designs, without dividing the presentation into mandatory category labels.

## Make distinct takes

Use the requested count; otherwise start with three to five. Each take must answer the question differently. Cosmetic variations of the same interaction do not count as distinct takes.

Include a simplest-path take: the fewest steps, roles, and controls that still satisfy the jobs. Explain what each other take adds and why.

For every take, deliver:

- A rendered mock using the product's real components and tokens, or clearly identified proposed components for a new product.
- The borrowed pattern, its source, and where the analogy stops working, when an analog is used.
- What it removes or simplifies relative to the baseline.
- A concrete tradeoff and who the take suits.
- A three-to-six-row proof following [references/proof.md](references/proof.md).

Show the actual content and interaction under discussion, not only a state diagram. Keep rationale and internal take identifiers outside the product UI. For a flow question, include a diagram comparing current and proposed steps; mark the current flow unknown when it is unknown.

Recommend one take or an explicit combination. Connect the recommendation to the jobs and evidence, and identify assumptions that still need user testing.

## Cut what does not earn its place

Remove unexplained labels, decorative sections, nonexistent product concepts, and controls with unclear outcomes. Button labels should distinguish creating new items from loading existing ones. Avoid exposing internal IDs as user-facing names.

Follow the target product's visual and accessibility conventions. Quiet borders, restrained color, thumbnail navigation for visual items, and moving secondary actions into menus can be useful starting points; use them only when they fit the jobs. Do not override the product's design system with an unrelated personal style.

Write plainly. Explain tradeoffs without promotional copy or filler.

## Deliver the round

Default to a local HTML comparison page with one self-contained mock per take. Use the project's existing preview tooling when that better represents its components. A design canvas or hosted artifact is optional when the tool is available and the destination is authorized. No particular hosting service, private skill, or MCP integration is required.

Keep the rationale beside the mocks. Include baseline, question, takes, recommendation, and one decision question. Do not upload private source material or publish the deliverable without authorization.

Render and inspect the result at desktop and phone widths when relevant to the target product. Check that every take has a visible mock and a supported proof, the comparisons answer the requested level, and the simplest-path take is present. Report any rendering limitation honestly; do not call unrendered HTML visually verified.

Return the local artifact or authorized preview link, one line per take, the recommendation, and one decision question. A completed round includes mocks, not just prose. If a required input or tool prevents completion, identify the blocker and provide the usable work without claiming the round is complete.

## Continue from the decision

When the user reacts, record the pick, its reasoning, and what caused each rejection. Carry those decisions into the next round; reopen a rejected idea only when new requirements or evidence justify it.

Check new requests against the original question. If the exploration drifts, state the change and resolve consequential ambiguity. If the user says it is overbuilt, move up a level, identify the largest sources of complexity, and revisit the simplest path.

When implementation is requested, build the chosen scope in the real code under the repository's instructions. Run the relevant checks and inspect the UI. Update the log with what shipped and any remaining gaps. Commit, push, open a PR, or deploy only within the user's authorization.
