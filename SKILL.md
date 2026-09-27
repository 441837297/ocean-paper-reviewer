---
name: ocean-paper-reviewer
description: Review a coherent ocean-science manuscript after a first draft exists, before advisor circulation or submission, or after a major revision. Perform whole-manuscript preflight checks for scientific argument closure, section function, claim-evidence alignment, cross-section consistency, figure/text coordination, reproducibility-facing Methods completeness, clarity, concision, and common editorial failure modes. Use for DOCX, PDF, or manuscript text when the user wants an internal manuscript audit rather than story generation, prose drafting, peer-review simulation, or response-letter work.
---

# Ocean Paper Reviewer

## Purpose

Perform an internal **whole-manuscript preflight review** after a paper has become a coherent draft. Treat the manuscript as an integrated scientific object: title, abstract, introduction, results, discussion, methods, figures, captions, references, supplementary material, and any other supplied submission components must agree with one another.

This skill is not a substitute for domain analysis, statistical validation, journal acceptance judgement, or peer review. Its job is to find manuscript-level faults early and convert them into actionable repair tasks.

## Operating boundary

Keep these responsibilities separate:

- **Ocean Paper Reviewer**: audit the complete or nearly complete manuscript; diagnose structural, consistency, clarity, and manuscript-integrity problems.
- **Nature Story**: reconsider the scientific story, novelty, competing storylines, mechanism, result hierarchy, or figure-led research architecture.
- **Ocean Paper Writer (OPW)**: execute manuscript revisions through Strategy -> Revision Brief -> Prose -> Verify, and process advisor/editor/reviewer feedback.

Do not silently absorb Nature Story or OPW responsibilities. Do not rewrite the full manuscript by default.
Ordinary single-paragraph or local revision acceptance belongs to OPW Verify, not this reviewer.

When this skill is called from OPW, return a **recommended route** for each issue but never switch to another skill automatically. OPW must ask the user for confirmation before routing work to Nature Story, OPW Strategy, OPW Prose/Verify, or another workflow.

## Inputs

Use the smallest set of materials needed for the requested audit:

- current authoritative manuscript version;
- figures and captions when available;
- supplementary material when cross-document consistency matters;
- target journal only when the user has supplied one;
- previous preflight report when performing a recheck.

For DOCX/PDF material, inspect rendered pages or embedded figures when the available tools support it. Do not rely only on extracted text for layout-sensitive figures, captions, equations, tables, or slide-derived source material. If a relevant visual cannot be inspected, state that limitation instead of guessing.
Mark inaccessible figures, captions, supplements and reference lists `NOT_ASSESSABLE`. Do not infer that the submission lacks them unless the user has identified the supplied package as complete and a required component is absent.

Do not invent journal formatting requirements. If no target journal is supplied, use general scientific-writing and manuscript-integrity checks only.

## Review modes

Choose one mode and state it briefly.

### Full Preflight

Default for a complete first draft, pre-advisor draft, pre-submission draft, or major-revision draft. Review the manuscript globally before reporting local issues.

### Focused Recheck

Use to revisit a small set of explicitly identified whole-manuscript issues from a previous report. Recheck the affected units and only the global invariants they can affect. Do not expand to Full Preflight by default.

### Section Audit

Use when only one section or a partial manuscript is supplied. Audit that unit rigorously, but mark any whole-manuscript checks as `NOT_ASSESSABLE` rather than inferring the missing context.

## Core workflow

### 1. Establish the review frame

Identify:

- manuscript version and supplied components;
- selected review mode;
- target journal if explicitly provided;
- material that is missing but relevant;
- what can and cannot be assessed from the supplied evidence.

Do not delay a useful bounded audit merely because optional material is missing.

### 2. Reverse-outline the manuscript before judging sentences

Extract the manuscript's intended chain:

**system/problem -> established knowledge -> exact gap -> this paper's move -> decisive results -> interpretation -> bounded implication -> limitation**

Then identify the role of every major section and main figure. If the chain cannot be reconstructed cleanly, report the break before commenting on line-level style.

Read [references/review-framework.md](references/review-framework.md).

### 3. Run the whole-manuscript integrity checks

Check at minimum:

- one dominant scientific main line, with a small number of clearly subordinate highlights;
- Title / Abstract / Introduction / Results / Discussion alignment;
- Introduction gap -> Results evidence -> Discussion answer closure;
- claim strength no stronger than the evidence;
- observed result, association, mechanism, causal inference, projection, and speculation clearly separated;
- repeated numbers, units, signs, time periods, regions, variables, terminology, and sample definitions consistent across all supplied components;
- every main figure has a clear scientific function and is discussed in one coherent location;
- figure order and Results order support the same argument;
- Methods contain the details needed to understand and reproduce the reported analysis at the level supported by the supplied manuscript;
- references and acknowledgements follow the supplied journal requirements when those requirements are available.

Use [references/section-rules.md](references/section-rules.md) and [references/cross-manuscript-checks.md](references/cross-manuscript-checks.md).

### 4. Separate hard problems from editorial heuristics

Do not turn lecture-style rules of thumb into universal pass/fail rules. Evaluate soft preferences in context, including title length, paragraph length, number of main figures, tense simplification, abstract abbreviation avoidance, and similar conventions.

Read [references/editorial-heuristics.md](references/editorial-heuristics.md).

### 5. Classify every issue by severity, owner and route

Use only these severities:

- `BLOCKER`: a central contradiction, unsupported central claim, missing required scientific connection, or manuscript-level fault that prevents a trustworthy internal handoff under this review scope.
- `MAJOR`: materially weakens the argument, evidence boundary, section function, reproducibility, or reader interpretation.
- `MINOR`: localized clarity, redundancy, wording, organization, or formatting issue with limited scientific effect.
- `HEURISTIC`: a non-binding editorial preference worth considering, not a failure.
- `PASS`: explicitly checked and no material issue found.
- `NOT_ASSESSABLE`: missing material prevents the check.

Assign an `Owner` to identify who must resolve the issue: `USER_OR_JOURNAL`, `OPW`, `NATURE_STORY`, or `REVIEWER_SELF`. Separately assign a `Recommended route`: `OPW_STRATEGY`, `OPW_PROSE_VERIFY`, `NATURE_STORY`, or `NONE`. Facts requiring author verification have `Owner: USER_OR_JOURNAL` and `Recommended route: NONE` until verified. A route is advice, not permission to invoke another workflow.

Read [references/routing-boundaries.md](references/routing-boundaries.md).

### 6. Report issues as repairable units

Do not return vague criticism such as "the logic is weak" or "the English needs improvement." Each issue must contain:

- exact location;
- severity;
- issue type;
- what is wrong;
- why it matters;
- minimum repair action;
- owner and recommended route;
- evidence or manuscript comparison that triggered the issue.

Prefer the smallest repair that restores manuscript integrity. Do not rewrite an entire paragraph when one claim boundary, transition, figure placement, or repeated number is the actual problem.

### 7. Finish with a manuscript-level decision summary

Return:

1. review scope and limitations;
2. manuscript spine diagnosis;
3. top blockers/major issues first;
4. cross-section closure map when a full manuscript is available;
5. consistency findings;
6. section-by-section issue register;
7. heuristic notes separated from true defects;
8. grouped routing recommendations;
9. the smallest next action that should occur before another full preflight.

Do **not** assign a single numeric manuscript score. Do **not** predict acceptance, rejection, impact factor, or journal outcome.

## Default output contract

Use this compact issue format:

```text
[ID] OPR-<section>-<number>
Location: <section / paragraph / figure / sentence>
Severity: BLOCKER | MAJOR | MINOR | HEURISTIC
Type: <closure / evidence / consistency / section function / clarity / figure / methods / format ...>
Issue: <specific diagnosis>
Why it matters: <scientific or editorial consequence>
Minimum repair: <smallest corrective action>
Owner: USER_OR_JOURNAL | OPW | NATURE_STORY | REVIEWER_SELF
Recommended route: OPW_STRATEGY | OPW_PROSE_VERIFY | NATURE_STORY | NONE
Trigger evidence: <what in the manuscript caused the flag>
```

For a full manuscript, also include the closure and consistency tables defined in [references/review-framework.md](references/review-framework.md).

## Source discipline

The bundled rules were distilled from the user's two Chinese Academy of Sciences Changchun Institute of Optics writing-lecture documents and from the prior OPW tutor-review checklist. The lecture transcripts contain speech-recognition errors, so slide content was treated as higher-confidence than conflicting transcript text. Read [references/source-basis.md](references/source-basis.md) only when provenance or rule interpretation matters.

Keep the distinction between:

- source-derived manuscript guidance;
- general review architecture added to make the skill reusable;
- target-journal requirements supplied later by the user.

Do not silently turn a source-specific recommendation into a universal scientific norm.
