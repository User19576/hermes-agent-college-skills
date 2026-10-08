---
name: completed-assignment-cleanup
description: "Use when archiving submitted coursework. Preserve evidence."
version: 1.0.0
author: Hermes Agent
license: MIT
platforms: [linux, macos, windows]
metadata:
  hermes:
    tags: [coursework, archive, cleanup, provenance]
    related_skills: [academic-assignment-support]
---

# Completed Assignment Cleanup

Organize a learner-confirmed completed assignment without deleting work or changing the submission. This procedure complements `academic-assignment-support`.

## When to Use

- Learner confirms assignment was submitted and asks to clean up its project folder.
- Do not use while assignment is still in progress or when the submitted artifact cannot be identified; clarify rather than guessing.

## Procedure

1. **Discover current state.** Use `search_files(target="files")` for root, `Resources/`, and existing `Archive/`. Read project instructions, brief, index, AI-use record, and any source notes with `read_file`. Identify the learner-reported submitted artifact, final editable source, assessment project file, screenshots, protected backups, and historical drafts. Do not infer a Moodle receipt from a filename.
2. **Classify, then preserve.** Keep the submitted PDF, final editable source, assessment project, original evidence, brief, workspace instructions, and AI-use record at root. Put only superseded drafts, intermediate copies, scaffolds, and research notes in `Archive/`. Honor any explicit protected-backup rule, even when the backup looks old. Do not delete files or rewrite the submitted artifact.
3. **Move without altering contents.** Check for target-name collisions before each move. Use `terminal` to record hashes of files being moved, create `Archive/` if absent, move each file, and compare source hashes to archived hashes. If a move or comparison fails, stop; do not claim cleanup complete. Preserve original filenames.
4. **Write index and status.** Create or update `README.md` with learner-reported completion, explicit lack of independently checked receipt, exact root essentials, archived contents, and a warning that archived relative image links may still point to root `Resources/`. Update `AGENTS.md`/`HERMES.md`, context notes, and AI-use disclosure to identify the final artifact and mark old prompts as historical. Preserve learner-authored prose in drafts and notes. Do not reopen accepted review issues as pending work.
5. **Verify.** Re-list root and archive with `search_files`; confirm every intended target exists, moved source paths are absent, hashes match, and final PDF/source still open or validate using appropriate read/validation tools. Report only checks actually performed; distinguish learner-reported submission from verified file integrity.

## Pitfalls

- A final file can have a draft-like filename; identify it from learner confirmation and actual contents, not the name.
- Cloud sync or Word may move or replace files mid-task. Re-discover paths before moving and avoid overwriting a newer version.
- `Archive/` is provenance, not trash. Leave prior versions and AI research intact, with clear non-submission labels.
- An unreadable PDF or unavailable submission receipt does not justify claiming verification; record the exact gap.
- Do not add submission-ready writing or rewrite the assessed report as part of cleanup.
