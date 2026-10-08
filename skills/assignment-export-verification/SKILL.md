---
name: assignment-export-verification
description: "Use when verifying coursework PDF or DOCX exports."
version: 0.1.0
author: Hermes Agent
license: MIT
platforms: [linux, macos, windows]
metadata:
  hermes:
    tags: [coursework, export, pdf, docx]
    related_skills: [academic-assignment-support, assessment-evidence-audit]
---

# Assignment Export Verification

Check that a report export reflects the learner's current source and meets the current brief. This procedure verifies an existing artifact; it does not author assessed text or imply that Moodle received it. Use `academic-assignment-support` for permissions and `assessment-evidence-audit` for a full requirement-to-image mapping.

## When to Use

- Learner has a Markdown, DOCX, or other editable report and wants its PDF/DOCX export checked before submission.
- Learner reports a new export may contain old text, broken images, split figures, or wrong dimensions.
- Do not overwrite a submitted artifact or protected original. If the requested source or export is unclear, identify it before touching files.

## Procedure

1. **Identify authority and versions.** Read workspace instructions, brief, the learner's current editable source, and the *exact* export with `read_file` and the relevant `pdf`/`docx` skill. Record expected filename and format, required image order/limits, and the latest learner-confirmed corrections. Distinguish a learner-reported submission from an independently checked file; keep historical exports separate.
2. **Compare content.** Check key changed passages in source against export text; an export can preserve an older draft. Enumerate headings, figure labels, embedded images, and their order in the export. Resolve Markdown links and verify that images actually appear in the exported document. Count all images, including those between numbered groups; do not infer count from filenames or figure labels alone.
3. **Check rendered layout.** Inspect the exported pages for missing/blank images, broken links, split figures/captions, orphaned headings, clipped screenshots, and image size limits specified in the brief. Preserve aspect ratio when assessing or, only if explicitly authorized, changing dimensions. For DOCX inspect the saved package and embedded media, then request a real office-app open/render check when compatibility matters. A valid package alone does not prove Word renders it correctly.
4. **Handle failures within scope.** Report precise page/section and source/export discrepancy. Edit only a user-designated working copy when authorized; back up an original before any embedded-image change. Preserve learner-authored prose. For a VS Code Markdown PDF export, a separate Chromium render is only an approximation of the extension; do not certify its export from that proxy. Regenerate through the actual export path when available.
5. **Verify again.** Reread and inspect the newly generated *exact* export after any fix. Recheck corrected text, figure/image count and order, page boundaries, and required filename/format. If the exporter or viewer cannot run, say which checks remain unverified. Do not claim an upload, submission, or grade without independent evidence.

## Pitfalls

- Correct source text does not prove the exported PDF contains it.
- An image link that resolves locally can still fail in the export; image presence must be checked in the output.
- PDF page count, DOCX package validity, and source hashes answer different questions; none alone proves visual correctness.
- Editing a final submission to repair layout is not a default step. Ask before any change, and leave submitted artifacts intact.

## Verification

Record the exact source and export checked. List observed content/layout results and any remaining gaps; claim success only for the artifact and export path actually inspected.
