---
name: assessment-evidence-audit
description: "Use when auditing coursework evidence against a brief."
version: 0.1.0
author: Hermes Agent
license: MIT
platforms: [linux, macos, windows]
metadata:
  hermes:
    tags: [coursework, evidence, screenshots, review]
    related_skills: [academic-assignment-support]
---

# Assessment Evidence Audit

Check whether the *actual report* supports each evidence requirement in its current brief. This is a review procedure, not permission to change the report or write assessed explanations. Use `academic-assignment-support` for AI-use boundaries and learner authorship.

## When to Use

- Review screenshot or photograph evidence for an assessed practical, especially before export or submission.
- Do not use loose screenshots to certify a report's image order, headings, or displayed size. Ask for the report when those properties matter.

## Procedure

1. **Establish scope.** Read workspace instructions, current brief, any prep instructions, and learner-reported instructor exceptions with `read_file`; use `search_files` to locate the current draft, evidence folder, and final deliverable. Treat the brief as default authority. Label an exception as learner-reported unless verified in written instructions. Identify required steps, values, formats, order, headings, and image-size limits. Never copy assignment-specific values into this skill.
2. **Inventory actual evidence.** Enumerate every image in the current report, including images between numbered sections, plus source files in the evidence folder. For PDF/DOCX, load the `pdf`/`docx` skill to inspect the document and its rendered pages or package; for Markdown, resolve every image link relative to the document and inspect its eventual export when layout matters. Use `vision_analyze` on relevant images; zoom small fields. Reopen linked images even if filenames match a past review: they can be replaced in place. Keep loose images distinct from embedded images.
3. **Map requirements to observations.** Make one row per brief step: required proof; report heading/image and page or section; visible result; status (`shown`, `missing`, `conflicts`, or `not checkable`). Check host application/VM identity as well as guest output, exact displayed settings, targets, addresses, packet-loss results, sequence, captions, and physical image dimensions when required. Distinguish a creation summary from current settings, reachability from route hops, and configured values from successful execution. A technically working alternative does not prove compliance with a literal brief value.
4. **Report actionable gaps.** Cite the brief requirement and the observed report section/page or screenshot. Say what correction or new learner evidence would resolve each gap; do not manufacture screenshots, alter original evidence, or write submission-ready prose. Do not reopen issues the learner already accepted unless new evidence or instructions change the assessment.
5. **Verify scope of claims.** Recheck each cited image and count against the current report. State explicitly which requirements were checked, which could not be checked, and whether an export was inspected. Do not claim submission, a receipt, grading, or instructor approval from local files.

## Pitfalls

- Text extraction from a brief can omit values shown only in embedded diagrams; inspect those images before finalizing the checklist.
- A filename, an old checklist, or a screenshot folder does not prove what the current report embeds.
- A working ping can still show lost packets or a different destination. A ping is not a route trace.
- Screenshot dimensions in pixels do not establish centimetre limits in a report; inspect displayed dimensions in the final document.

## Verification

Every applicable brief evidence item has a report location and observed status. Every factual finding is traceable to current evidence; uninspected format or layout checks remain explicitly unverified.
