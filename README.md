# Ocean Paper Reviewer

Ocean Paper Reviewer checks a coherent, complete ocean-science manuscript before advisor circulation, submission, or after a major revision.

## Scope

It performs whole-manuscript preflight: section responsibilities, claim-evidence alignment, cross-manuscript consistency, Introduction-Results-Discussion closure, and manuscript-wide diagnostic review. It reports issues and recommended routes without making revisions.

It does not construct a scientific story from scratch, draft final prose, verify ordinary local revisions, or manage reviewer/editor responses.

## Rule sources

The preflight guidance was distilled from two Chinese Academy of Sciences Changchun Institute of Optics lectures on scientific writing (`中科院长光所写作1_原文.docx` and `中科院长光所写作2_原文.docx`) and the former Ocean Paper Writer tutor-review checklist. The lectures' manuscript-relevant advice informs the section and whole-paper checks; numerical writing preferences remain heuristics. Novelty ranking, reviewer selection and rejection appeals are outside this Skill's preflight remit. See [source basis](references/source-basis.md) for provenance and scope.

## Ecosystem

- [Ocean Paper Writer](https://github.com/441837297/ocean-paper-writer) controls manuscript development, Strategy, Prose, local Verify, and external feedback. Reviewer does not replace OPW Verify.
- [Nature Story](https://github.com/haohuresearch/nature-story) develops scientific questions, novelty, mechanisms, evidence and Figure/Results architecture. It does not replace the Reviewer preflight.

```text
research idea / unstable scientific story
  -> user confirms route -> Nature Story -> Story Handoff Packet
  -> user confirms scientific decisions -> Ocean Paper Writer
  -> Build / Strategy -> Prose -> Verify -> complete manuscript
  -> user confirms route -> Ocean Paper Reviewer -> issue list
  -> user selects issue -> Ocean Paper Writer: Strategy -> Prose -> Verify
```

Cross-skill routing is advisory and requires explicit user confirmation.

## Installation

This repository root is the `ocean-paper-reviewer` Skill root. Install it as `<skills-directory>/ocean-paper-reviewer`, or link that path to this repository root. Keep Ocean Paper Writer and Nature Story independently installed.
