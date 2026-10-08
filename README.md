# Hermes Agent College Skills

Four agent-created skills for Hermes that grew out of my Cork College of FET assignments. Classmates might find them useful, but they reflect my briefs and how I work. This repository is not assessed work; assignment AI-use rules apply when using the skills on coursework, not when developing the repository. Check your own brief and instructor directions.

## Included skills

- [`academic-assignment-support`](skills/academic-assignment-support/SKILL.md) helps review briefs and drafts while keeping assessed writing with the learner. It includes a course-specific rules reference and an AI-use disclosure template.
- [`completed-assignment-cleanup`](skills/completed-assignment-cleanup/SKILL.md) helps archive old drafts without changing the submitted file or original evidence.
- [`assessment-evidence-audit`](skills/assessment-evidence-audit/SKILL.md) maps brief requirements to visible evidence in the current report and flags gaps without inventing proof.
- [`assignment-export-verification`](skills/assignment-export-verification/SKILL.md) compares an editable report with its PDF/DOCX export and checks images and page layout.

These are copies of skills from my own Hermes setup, not official Hermes skills. [Design principles](DESIGN_PRINCIPLES.md) explains the choices behind them.

## Installation

### Install manually

1. Get the files from GitHub. Use **Code → Download ZIP** and extract it, or run `git clone https://github.com/User19576/hermes-agent-college-skills.git`.
2. Read the four skills linked above. [`standing-ai-use-rules.md`](skills/academic-assignment-support/references/standing-ai-use-rules.md) quotes a brief from my course and includes a clarification reported by one learner. Even if you're in the same course, check your own current brief and instructor directions.
3. Open your Hermes skills folder: `%LOCALAPPDATA%\hermes\skills` on Windows or `~/.hermes/skills` on macOS/Linux. If you use a named profile, find its own `profiles/<name>/skills` folder under your Hermes home. If `HERMES_HOME` is set to the active profile, use its `skills` folder. Create the folder if it doesn't exist.
4. Copy `academic-assignment-support/`, `completed-assignment-cleanup/`, `assessment-evidence-audit/`, and `assignment-export-verification/` from this repository's `skills/` into your Hermes `skills/`. Keep `SKILL.md` and any `references/` or `templates/` folders in place. If any skill already exists, back it up and compare the copies before replacing it.
5. Start a new chat in that profile and type `/skills`. You should see all four names. You can also run `hermes skills list --enabled-only` (or `hermes -p NAME skills list --enabled-only` for a named profile). If a skill is missing, check that `SKILL.md` sits directly inside its folder.

This installs only the four skills. It does not change `SOUL.md`, `memories/USER.md`, or `memories/MEMORY.md`. See the [Hermes skills guide](https://hermes-agent.nousresearch.com/docs/guides/work-with-skills) for more on loading skills.

### Install via Hermes prompt

Paste this into Hermes. It will follow the [installation guide](installation/FOR_HERMES.md), show any proposed changes to the skills and your `SOUL.md`, `USER.md`, and `MEMORY.md`, and wait for typed approval before making them.

```text
Install academic-assignment-support, completed-assignment-cleanup, assessment-evidence-audit, and assignment-export-verification directly from https://github.com/User19576/hermes-agent-college-skills into my Hermes profile, without cloning it. Read installation/FOR_HERMES.md in that repository and follow its review and approval steps. Show me the exact plan and wait for the specified typed approval before changing anything.
```

## Related skills

Hermes normally bundles these five skills, so you usually don't need to install them. A profile can disable or omit them; check `hermes skills list --source builtin --enabled-only` if one is missing. `humanizer` started as a third-party skill and was ported into Hermes.

- Nous Research: [`pdf`](https://github.com/NousResearch/hermes-agent/tree/main/skills/productivity/pdf) for briefs and exports; [`docx`](https://github.com/NousResearch/hermes-agent/tree/main/skills/productivity/docx) for Word reports.
- Co-authored: [`obsidian`](https://github.com/NousResearch/hermes-agent/tree/main/skills/note-taking/obsidian) for the assignment tracker (Teknium and Hermes Agent); [`grounded-citations`](https://github.com/NousResearch/hermes-agent/tree/main/skills/research/grounded-citations) for source-backed research (Hermes Agent and Teknium).
- Third-party origin: [`humanizer`](https://github.com/blader/humanizer) for wording edits. It is [listed on skills.sh](https://www.skills.sh/blader/humanizer/humanizer) and linked here, not copied into this repository.

This list shows related tools, not a count of past skill uses. The four skills in this repository use the [MIT License](LICENSE). The related skills above keep their own licenses.
