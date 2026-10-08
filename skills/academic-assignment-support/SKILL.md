---
name: academic-assignment-support
description: "Use when supporting coursework. Preserve learner authorship."
version: 1.0.0
author: Hermes Agent
license: MIT
metadata:
  hermes:
    tags: [academic, assessment, research, feedback]
    related_skills: [grounded-citations]
---

# Academic Assignment Support

## When to Use

Use for assessed reports, coursework, skills demonstrations, or similar learner submissions where assignment rules and learner authorship constrain assistance. First classify the target artifact, not its folder name: a college-themed repository of reusable agent skills is not an assignment. Do not apply assignment AI-use limits or create an assignment disclosure for that repository; apply those rules only when working on an actual assignment.

## Procedure

1. Discover assignment constraints before helping.
   - Read workspace instructions with `read_file("HERMES.md")` when present.
   - Read `references/standing-ai-use-rules.md` for the original learner's standing AI-use limits. The quoted policy comes from a Virtualisation Support brief; its use across that learner's assignments comes from their separate instruction. For another learner, treat this as course context, not their policy. Check their current brief and instructor directions before applying any rule.
   - Locate assessment materials with `search_files(target="files", pattern="*.pdf")`, then read the brief with `read_file`.
   - Render and inspect any embedded configuration screenshots or diagrams in the brief, zooming into small fields; text extraction often omits settings shown only as images. Compare sample values with surrounding placeholder instructions before recording requirements.
   - Identify deliverable format, evidence requirements, permitted AI uses, and submission constraints. When the learner reports an exception to the brief, label it as learner-reported, apply only its stated scope, and update every dependent checklist and scaffold; otherwise obsolete evidence gaps keep resurfacing. If asked to save that clarification in `MEMORY.md`, write and verify it in the active profile's `memories/MEMORY.md`; project instructions or a skill reference alone do not satisfy an explicit memory-file request.

2. Classify request against assessment rules.
   - Allow grammar/spelling review, reference-list help, constructive feedback, evidence checks, and source discovery when permitted.
   - Do not write learner-submittable report sections, reflective content, conclusions, or an essay from notes.
   - When research assistance is allowed, give research notes, questions, and sources. Keep these distinct from submission prose.
   - If learner gives a teacher clarification that expands permitted research use, preserve learner authorship: provide researched facts and links, not ready-to-submit paragraphs.

3. Review drafts without changing them unless learner explicitly requests edits.
   - Locate and read the current draft even when the learner renamed a scaffold into it; distinguish learner-written passages from inherited prompts before giving feedback. Treat a model as a comparison, not a rubric; distinguish its sample dates, recipient, and attachment claims from actual requirements.
   - Report issues by section/line where available: factual accuracy, unsupported claims, missing evidence, policy risk, grammar, and brief compliance. Distinguish a draft sent for feedback from a final submission: flag unfinished required sections without inventing them or claiming the draft was submitted. When the learner identifies a detail as a mock placeholder or explains that a body-only file intentionally omits fields shown in a screenshot, accept that scope and stop flagging the omission; repeating it obscures actionable feedback.
   - For screenshot-only reviews, re-inventory the evidence folder, reread the brief and prep instructions, then map every image to a required step. Inspect the host application's title and VM tab as well as guest output; a correct guest result can come from the wrong required hypervisor. Distinguish reachability tests such as `ping` from route traces that enumerate hops; the former cannot satisfy a hop-count requirement. If no report is supplied, do not certify screenshot order, headings, or displayed dimensions from loose image files.
   - State concrete correction needed and why. Do not silently rewrite the draft.
   - When checking live technical evidence, preserve hostnames, usernames, and placeholders exactly. Verify authentication before claiming remote access; an open SSH port proves only reachability. Distinguish kernel-module files, successful `modprobe` calls, and currently loaded modules; they establish different facts.

4. Research technical claims from authoritative sources.
   - Prefer standards bodies, government documentation, original vendor documentation, and primary project documentation.
   - Load `grounded-citations` for sourced research. Register each retrieved URL before drafting notes.
   - Separate stable foundational sources from current-industry sources. Use current sources for claims about trends.
   - Give 2–4 focused sources, a fact/topic list, and questions the learner can answer in their own words.

5. Create supporting artifacts only on request.
   - When asked to follow a previous assignment's drafting procedure, inspect that assignment's workspace instructions, scaffold, draft history, and AI-use rules first. Reuse the procedure, not its assessed prose or assignment-specific claims.
   - Match scaffold length to the brief and learner's requested depth. For a short practical demonstration, use brief-ordered evidence slots and concise learner-answer prompts, not long paragraphs, unnecessary sections, or a second outline duplicating an existing checklist.
   - Use a separate, clearly labelled non-submittable scaffold by default; leave the learner's draft unchanged. When the learner explicitly names an unsubmitted working revision for baselines, insert only brief-ordered headings and bracketed learner-answer prompts there. Preserve existing prose and figures, label prompts for replacement, and verify the submitted artifact remains unchanged; a scaffold is not permission to compose assessed paragraphs.
   - Place available screenshots at their relevant steps and flag missing evidence or configuration conflicts beside the prompt. Do not write captions or turn an unverified setting into a completed claim. Resolve every image link before handing off the scaffold; a plausible filename does not prove the starter works.
   - Include source links and a warning that learner must write final prose and acknowledge sources.

6. Keep an AI-use disclosure for every assignment workspace where AI assistance occurs.
   - Create or update `AI-DISCLAIMER.md` in the assignment folder; use `templates/AI-DISCLAIMER.md` as a guide, not as an unfilled deliverable. Record only assistance that actually happened, including direct edits and AI-created support files. Distinguish learner-supplied work from AI changes.
   - Before writing, read any existing disclosure and the assessment's AI-use rules. Preserve existing accurate entries, append or correct this session's use, and follow any required institution wording or disclosure format. Do not claim the learner reviewed, approved, submitted, or used a source unless confirmed.
   - Label the file as an AI-use record; do not insert it into assessed prose or assert that it must be submitted unless the brief requires it. Tell the learner to check whether the instructor requires a different form.

7. Update learner-owned documents only with explicit scope.
   - For permitted grammar, punctuation, formality, or humanizing edits, reread the latest learner draft, preserve its claims and placeholders, and make bounded wording changes rather than composing a new assessed piece. Show changed passages or a diff, then update any companion review notes that would otherwise contradict the edited draft.
   - When learner designates an original/work-in-progress copy and a separate draft for cleanup, preserve the original and edit only the designated draft. Remove AI scaffold instructions, unanswered bracket prompts, stale checkboxes, and false completion cues from the draft; leave missing assessed sections for the learner to write and report them as gaps.
   - Back up the original before changing embedded evidence.
   - Preserve the report's existing heading order and layout unless the learner explicitly authorizes restructuring.
   - Replace only screenshots or assets the learner explicitly identifies; do not silently rewrite their assessed narrative.
   - Inspect the exact deliverable, not only the evidence folder: enumerate headings, every embedded image (including extra images between numbered groups), displayed dimensions, targets, and packet-loss results against the brief. After cleanup, resolve every image link and reconcile image count with figure labels in order; a group-based renumber can skip an intervening image. Resize in-document images to the stated physical limits while retaining aspect ratio.
   - For VS Code Markdown PDF figure cleanup, use a nonbreaking `<figure>` block with its existing label and image; limit image height proportionally so the whole block fits a page. The extension strips inline `<style>` blocks in its default sanitization mode, so prefer safe inline attributes over hidden CSS. Render an export, confirm every image loads, and compare figure-label pages with image pages. Inspect adjacent page boundaries for split paragraphs or orphaned headings; place a deliberate page break before a section only when the rendered result improves. A separate Chromium layout check approximates the extension but is not proof of its exact export.
   - When a learner exports a new format, compare its text with their claimed latest corrections before editing; an export can preserve an older draft. Back up the exact exported file, keep learner-authored explanations unchanged, and flag stale claims for the learner.
   - Validate the saved document package and confirm each embedded replacement matches its source asset. A package check does not prove Word opens or renders correctly; request an actual open check when document compatibility matters.
   - For `.odt` reports, use a compatible office editor for in-document changes. If none is available, keep the ODT untouched and create a separate, clearly labelled scaffold or research-notes file. For learner-provided `.docx`, use python-docx to move existing sections or resize shapes, then run the docx package validator.

## Standing Rules

- Treat the assessment brief as default authority. When a learner reports an additional instructor permission, use the narrowest interpretation needed and preserve that permission's boundary.
- Do not mistake a report scaffold, source notes, or feedback for permission to generate the assessed narrative.
- Keep progress notes and learner-owned files unchanged unless the learner explicitly authorizes the exact edit.
- Review evidence claims against supplied screenshots and configuration notes. Flag discrepancies rather than invent explanations.
- Treat literal assessment values as requirements even when a different working configuration is technically valid; a functional result does not prove brief compliance. Compare exact configuration fields against the wording: total virtual CPUs can differ from requested cores, and a bridge label alone does not establish NAT.
- Flag claims that create legal, licensing, security, or academic-integrity risk; require instructor approval before retaining them in assessment material. Record a learner-confirmed assigned number for later assignments when asked, but never persist shared passwords or derived passwords in memory, notes, or report scaffolds.

## Pitfalls

- Verify stated minimum system requirements against an official source before accepting a comparison table; copied requirement tables often contain material errors.
- Distinguish configured virtual-disk capacity from host physical storage and preallocated disk use; these measurements answer different questions.
- Do not describe VM isolation as absolute; host compromise, shared integration features, networking, and hypervisor vulnerabilities can cross boundaries.
- Challenge universal performance and network-speed claims against workload and evidence before accepting them; nominal link rates alone do not establish remote-desktop usability or required LAN capacity.
- Do not recommend snapshot recovery as a completed safeguard unless evidence shows a snapshot exists; a restore point cannot recover work that was never captured.
- Treat a product feature page as evidence of a technical capability, not proof of universal industry adoption; phrase it as a source-backed trend example.
- Scope a classroom worksheet's simplified definition to its examples: centrally hosted VDI/RDS is not the only desktop virtualisation, and a local desktop VM does not prove VDI/RDS was configured. Verify product-specific models against vendor documentation; RDS users share a server instance but have separate sessions, not one shared desktop. Do not present a Linux desktop as Microsoft RDS.
- Keep research notes short and topic-led; long prose becomes a de facto assignment draft and weakens learner authorship.
- Reopen each screenshot linked from the current draft, even when its filename matches an earlier review; files can be replaced in place after a configuration change, making old checklist findings false. Read exact settings and distinguish a current hardware view from a creation summary; neither proves guest-side hostnames, ISO filenames, or an unshown disk size. Recheck addresses, gateways, ping targets, and packet-loss totals against final evidence.
- Keep failed and successful connectivity evidence separate and in brief order; an earlier partial-success capture cannot prove post-repair success, even if the destination replies.
- Do not treat a changed working configuration as evidence of the requested fault repair when the brief forbids changing that value; ask the learner to document actual checks and corrective steps.
