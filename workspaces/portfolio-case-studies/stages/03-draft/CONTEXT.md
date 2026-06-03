# Stage 03: Draft

Turn the narrative brief into a full case study draft written in the author's voice.

## Inputs

| Source | File/Location | Section/Scope | Why |
|--------|--------------|---------------|-----|
| Previous stage | `../02-angle/output/[project-slug]-brief.md` | Full file | The thesis, value types, and outline to write from |
| Reference | `references/draft-guide.md` | Full file | How to write each section well |
| Shared | `../../shared/case-study-anatomy.md` | "The Sections" through "Length and Scannability" | The outcome-first structure and target length |
| Shared | `../../shared/impact-evidence.md` | Full file | How to write the evidence and impact section |
| Author vault | `../../author-vault/voice-rules.md` | "Hard Constraints" through "What the Voice Is NOT" | Voice to write in |
| Author vault | `../../author-vault/identity.md` | "Audience" | Who you are writing for |

## Process

1. Read the brief: thesis, lead outcome, locked value types, and outline.
2. Draft a working title that states the point and an opening that leads with the outcome, not the process.
3. Write each section in outcome-first order following the outline and the draft guide. Give every section a headline that tells the story on its own. Show decisions and reasoning, including at least one rejected path.
4. Mark where visual evidence belongs with a bracketed note, for example `[before/after: the checkout flow]`, with a "why" caption. Do not invent visuals.
5. **[Checkpoint]** -- Present the full draft. The human redirects structure, emphasis, or any section before polish.
6. Run the audit checks below. If any fail, revise before saving.
7. Save the draft to output/.

## Checkpoints

| After Step | Agent Presents | Human Decides |
|------------|---------------|---------------|
| 4 | The complete draft with section headings and visual-evidence notes | Whether the structure, emphasis, and story are right before polish |

## Audit

| Check | Pass Condition |
|-------|---------------|
| Outcome first | The draft opens with the strongest outcome, before the process |
| Headline test | Reading only the section headlines conveys the whole story |
| Thesis delivered | The draft proves the brief's thesis from start to finish |
| Value delivery | The draft delivers on every value type locked in the brief |
| Decisions and rejected path | Key decisions appear with reasoning and tradeoffs, and at least one rejected path is shown |
| Evidence present | The outcome is backed by at least two evidence types, or what would be measured is named |
| Voice constraints | Zero violations of the hard constraints in voice-rules.md |
| Role visible | The reader can tell exactly what the author did |

## Outputs

| Artifact | Location | Format |
|----------|----------|--------|
| Draft case study | `output/[project-slug]-draft.md` | Markdown: title, sections per the anatomy, with bracketed visual-evidence notes |

The draft in `output/` is the human edit surface. Rewrite lines, cut sections, change the title. Stage 04 reads whatever is in that file.
