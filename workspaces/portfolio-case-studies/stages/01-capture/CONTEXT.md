# Stage 01: Capture

Draw out the raw material of a project into a structured dossier the later stages can shape into a case study.

## Inputs

| Source | File/Location | Section/Scope | Why |
|--------|--------------|---------------|-----|
| User | (conversation) | The project, plus any notes, links, or artifacts | The raw material to capture |
| Reference | `references/capture-prompts.md` | Full file | The questions that surface the facts that matter |
| Shared | `../../shared/impact-evidence.md` | "The Evidence Types" | The menu of impact signals to gather |
| Author vault | `../../author-vault/identity.md` | "Audience" and "Portfolio Mission" | Know what kind of detail this portfolio needs |

## Process

1. Ask the user which project this case study is about, which focus it leans toward (design, problem solving, or collaboration), and its intended use (portfolio site, a specific job application, an interview, or an internal showcase). Record these as per-run details.
2. Work through the capture prompts conversationally. Pull out: context and role, the real problem in one sentence, constraints, the 2-3 key decisions and why, the paths rejected and why, the outcome, and impact evidence from the toolkit.
3. Note where evidence is thin (a claimed result with no source, a decision with no reasoning, no rejected path). Flag these as gaps to fill rather than inventing detail.
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
| Problem captured | The underlying problem is stated in one sentence, not only the original brief |
| Decisions with reasoning | At least one key decision is recorded with the reasoning and tradeoffs behind it |
| Rejected path captured | At least one path the user considered and rejected is recorded, with why |
| Evidence noted | Claimed outcomes have a source, or the metric that would prove them is named |
| No invention | Nothing in the dossier was assumed or fabricated to fill a gap |

## Outputs

| Artifact | Location | Format |
|----------|----------|--------|
| Project dossier | `output/[project-slug]-dossier.md` | Structured raw facts: context, role, problem, constraints, key decisions, rejected paths, outcome, impact evidence, focus, intended use |

The dossier in `output/` is the human edit surface. Open it, correct facts, add detail. Stage 02 reads whatever is in that file.
