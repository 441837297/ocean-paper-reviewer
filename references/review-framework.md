# Review framework

## 1. Manuscript spine diagnosis

Reconstruct the paper in one compact chain:

`system/problem -> established knowledge -> exact gap -> this paper's move -> decisive evidence -> interpretation -> bounded implication -> limitation`

For each link, record `CLEAR`, `WEAK`, `MISSING`, or `CONFLICTING`.

A paper can be grammatically polished and still fail preflight if this chain is broken.

## 2. Introduction-Results-Discussion closure map

Use this table for a full manuscript:

| Introduction gap / question | Results evidence | Discussion answer | Status |
|---|---|---|---|
| exact gap statement | matching figure/result/analysis | explicit interpretation/answer | CLOSED / PARTIAL / OPEN / CONFLICTING |

Rules:

- `CLOSED`: the Introduction creates a question, Results provide evidence, and Discussion answers at the supported strength.
- `PARTIAL`: evidence or interpretation addresses only part of the stated gap.
- `OPEN`: the gap is raised but not resolved, or the Discussion makes a conclusion with no clear originating question.
- `CONFLICTING`: sections answer the same question differently.

Do not require every Introduction sentence to map one-to-one to a Discussion sentence. Map only consequential scientific gaps and claims.

## 3. Cross-manuscript consistency matrix

Apply the authoritative claim-evidence, promise-delivery and consistency rules in [cross-manuscript-checks.md](cross-manuscript-checks.md); this section defines only the compact reporting view.

Build only rows that matter:

| Item | Abstract | Main text | Figure/caption | Supplement / other | Status |
|---|---|---|---|---|---|
| central number / unit | | | | | CONSISTENT / CONFLICT |
| key term / variable | | | | | |
| spatial or temporal scope | | | | | |
| sign / direction | | | | | |
| sample / method definition | | | | | |
| limitation / evidence boundary | | | | | |

Do not waste space listing values that are already consistent unless they are central to the paper.

## 4. Whole-manuscript read order

For Full Preflight, use this order when possible:

1. Title + Abstract.
2. Figure titles/captions and Results headings.
3. Introduction.
4. Results with figures.
5. Discussion / Conclusion.
6. Methods.
7. References, acknowledgements, supplementary material, and submission components supplied by the user.
8. Re-read Title + Abstract after the body to detect drift.

This order exposes manuscript promises before reading details, then checks whether the body fulfills them.

## 5. Issue prioritization

Prioritize in this order:

1. central claim and evidence conflicts;
2. story/section closure failures;
3. inconsistent numbers, terms, methods, or scopes;
4. missing reproducibility-facing information;
5. figure/text organization;
6. redundancy and clarity;
7. soft editorial heuristics.

Do not lead with grammar when a scientific or structural blocker exists.

## 6. Recheck behavior

For Focused Recheck:

- first verify that each previously flagged issue was actually resolved;
- check whether the repair introduced a new contradiction elsewhere;
- expand globally only when a changed item is repeated elsewhere: central claim, number, unit, term, figure definition, method definition, section role, or scope;
- do not rerun a full stylistic audit unless the user requests it.

## 7. Manuscript-level closing summary

End with four short items:

- `Preflight state`: `CLEAR_WITHIN_SCOPE`, `REVISE`, or `INCOMPLETE_INPUTS`.
- `Highest-priority issue`: one sentence.
- `Recommended next owner`: one of the defined owners; give a separate route only when a workflow is appropriate.
- `Next action`: the smallest concrete repair or decision before the next preflight.

`CLEAR_WITHIN_SCOPE` means no material issue was found under this skill's checks. It does not certify scientific truth or predict publication outcome.
