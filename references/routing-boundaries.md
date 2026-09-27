# Routing boundaries

Ocean Paper Reviewer diagnoses. It does not silently take over adjacent workflows.

`Owner` names who must resolve an issue: `USER_OR_JOURNAL`, `OPW`, `NATURE_STORY`, or `REVIEWER_SELF`. `Recommended route` names an optional next workflow: `OPW_STRATEGY`, `OPW_PROSE_VERIFY`, `NATURE_STORY`, or `NONE`. These fields are separate. Author verification of missing parameters, evidence or policy is `Owner: USER_OR_JOURNAL; Recommended route: NONE`. Mechanical reviewer checks can be `Owner: REVIEWER_SELF; Recommended route: NONE`.

## Route to Nature Story when

The issue asks whether the paper's **scientific story itself** is the right one, for example:

- the central question is weak or fragmented;
- several incompatible storylines compete for the manuscript;
- the claimed novelty is unclear or threatened by prior work;
- the result hierarchy is wrong;
- the figure sequence needs redesign around a different scientific tension;
- mechanism-first, consequence-first, or alternative narratives need comparison;
- a major analysis should be added or removed to establish the story.

Return a short reason and the manuscript evidence that triggered the routing recommendation.

## Route to OPW Strategy when

The scientific story is broadly retained but a manuscript unit needs a substantive decision, for example:

- a claim is too strong for the evidence;
- the Introduction gap and Results do not align;
- a result belongs in another section;
- the Discussion needs a different interpretation order;
- a limitation changes the scope of the conclusion;
- a figure or paragraph has the wrong manuscript function;
- new verified evidence must be integrated.

OPW Strategy should create or update a Revision Brief before prose changes.

## Route to OPW Prose/Verify when

Scientific meaning is already fixed and the remaining problem is expression:

- sentence clarity;
- concision;
- redundancy;
- terminology normalization;
- transitions;
- grammar or tense consistency;
- local paragraph flow.

Do not use Prose to fix an unresolved scientific decision.

## Keep with Reviewer Self when

The correction is mechanical and does not require a scientific judgement:

- duplicate figure citation;
- inconsistent figure numbering;
- an obvious unit formatting mismatch where the intended value is unambiguous;
- repeated abbreviation definition;
- reference style mismatch against supplied journal instructions;
- capitalization or label consistency.

## Assign to User or Journal when

The issue depends on information the reviewer cannot infer:

- target-journal-specific policy;
- author/contributor decision;
- missing dataset, code, analysis, or provenance;
- unresolved conflicting manuscript versions;
- ethics, disclosure, or submission declarations requiring authoritative policy.

## Confirmation rule under OPW control

When OPW is the main controller:

1. Ocean Paper Reviewer returns the grouped issue report, owners and recommended routes.
2. OPW summarizes the proposed route in plain language.
3. OPW asks the user to confirm before invoking Nature Story or entering a new OPW revision workflow.
4. After the routed work returns and OPW Verify passes, rerun only the necessary preflight checks unless the changes altered the central story.

Do not create hidden automatic chains across skills.
