# Stage 01: Capture

Draw out the raw material of a project into a structured dossier the later stages can shape into a case study.

## Inputs

| Source | File/Location | Section/Scope | Why |
|--------|--------------|---------------|-----|
| User | (conversation) | The project, plus any notes, links, or artifacts | The raw material to capture |
| Reference | `references/capture-prompts.md` | Full file | The questions that surface the facts that matter |
| Author vault | `../../author-vault/identity.md` | "Audience" and "Portfolio Mission" | Know what kind of detail this portfolio needs |

## Process

1. Ask the user which project this case study is about, and which focus it leans toward: design, problem solving, or collaboration. Record this as the per-run focus.
2. Work through the capture prompts conversationally. Pull out: context and role, the real problem, constraints, the key decisions and why, what was done, the outcome and evidence, and any tradeoffs or dead ends.
3. Note where evidence is thin (a claimed result with no number, a decision with no reasoning). Flag these as gaps to fill rather than inventing detail.
4. **[Checkpoint]** -- Present the assembled dossier and the list of gaps. Let the user fill gaps or confirm the record is complete.
5. Run the audit checks below. If any fail, gather more before saving.
6. Save the dossier to output/.

## Checkpoints

| After Step | Agent Presents | Human Decides |
|------------|---------------|---------------|
| 3 | The structured dossier so far, plus a list of thin or missing facts | What to add, correct, or leave out |

## Audit

| Check | Pass Condition |
|-------|---------------|
| Role clarity | The user's specific role and contribution is recorded, not just the team's |
| Problem captured | The underlying problem is stated, not only the original brief |
| Decisions with reasoning | At least one key decision is recorded with the reasoning and tradeoffs behind it |
| Evidence noted | Claimed outcomes have a source or are flagged as needing one |
| No invention | Nothing in the dossier was assumed or fabricated to fill a gap |

## Outputs

| Artifact | Location | Format |
|----------|----------|--------|
| Project dossier | `output/[project-slug]-dossier.md` | Structured raw facts: context, role, problem, constraints, decisions, actions, outcome, evidence, tradeoffs, focus |

The dossier in `output/` is the human edit surface. Open it, correct facts, add detail. Stage 02 reads whatever is in that file.
