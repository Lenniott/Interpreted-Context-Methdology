# Portfolio Case Studies

This workspace guides you from a project you worked on through capture, angle, draft, and polish -- one stage at a time -- to produce a portfolio case study about design, problem solving, or collaboration.

## Folder Map

```
portfolio-case-studies/
├── CLAUDE.md              (you are here)
├── CONTEXT.md             (start here for task routing)
├── setup/
│   └── questionnaire.md   (onboarding -- run with "setup")
├── author-vault/
│   ├── CONTEXT.md         (routes to voice and identity files)
│   ├── voice-rules.md     (how you write -- tone and constraints)
│   └── identity.md        (who you are, who the portfolio is for)
├── stages/
│   ├── 01-capture/        (a project -> raw project dossier)
│   │   ├── CONTEXT.md
│   │   ├── output/
│   │   └── references/    (capture prompts)
│   ├── 02-angle/          (dossier -> narrative brief and outline)
│   │   ├── CONTEXT.md
│   │   ├── output/
│   │   └── references/    (angle patterns)
│   ├── 03-draft/          (brief -> full draft case study)
│   │   ├── CONTEXT.md
│   │   ├── output/
│   │   └── references/    (draft guide)
│   ├── 04-polish/         (draft -> polished case study)
│   │   ├── CONTEXT.md
│   │   ├── output/
│   │   └── references/    (polish checklist)
│   └── 05-publish/        (polished -> publish-ready format) [optional]
│       ├── CONTEXT.md
│       ├── output/
│       └── references/    (format guide)
└── shared/
    ├── case-study-anatomy.md  (the outcome-first structure of a case study)
    ├── impact-evidence.md     (how to prove impact, with or without metrics)
    └── value-framework.md     (what makes a case study worth reading)
```

## Triggers

| Keyword | Action |
|---------|--------|
| `setup` | Run onboarding questionnaire -- configures your identity, voice, audience, and case study structure |
| `status` | Show pipeline completion for all stages |

### How `status` works

Scan `stages/*/output/` folders. For each stage, if the output folder contains files (other than .gitkeep), the stage is COMPLETE. Otherwise it is PENDING. Render:

```
Pipeline Status: portfolio-case-studies

  [01-capture]  -->  [02-angle]  -->  [03-draft]  -->  [04-polish]  -->  [05-publish]
     STATUS            STATUS           STATUS           STATUS            STATUS
```

## Routing

| Task | Go To |
|------|-------|
| Capture a project's raw material | `stages/01-capture/CONTEXT.md` |
| Choose the angle and outline | `stages/02-angle/CONTEXT.md` |
| Write the case study draft | `stages/03-draft/CONTEXT.md` |
| Polish and edit the draft | `stages/04-polish/CONTEXT.md` |
| Format for publishing | `stages/05-publish/CONTEXT.md` |
| Configure this workspace | `setup/questionnaire.md` |

## What to Load

| Task | Load These | Do NOT Load |
|------|-----------|-------------|
| Capture a project | `stages/01-capture/references/capture-prompts.md`, `shared/impact-evidence.md`, `author-vault/identity.md` | `author-vault/voice-rules.md`, all later stage references |
| Choose the angle | `stages/01-capture/output/`, `stages/02-angle/references/angle-patterns.md`, `shared/value-framework.md`, `shared/impact-evidence.md`, `shared/case-study-anatomy.md`, `author-vault/identity.md` | `author-vault/voice-rules.md`, `stages/03-draft/`, `stages/04-polish/` |
| Write the draft | `stages/02-angle/output/`, `stages/03-draft/references/draft-guide.md`, `shared/case-study-anatomy.md`, `shared/impact-evidence.md`, `author-vault/voice-rules.md`, `author-vault/identity.md` | `stages/01-capture/`, `stages/04-polish/`, `stages/05-publish/` |
| Polish the draft | `stages/03-draft/output/`, `stages/04-polish/references/polish-checklist.md`, `author-vault/voice-rules.md`, `shared/impact-evidence.md`, `shared/value-framework.md` | `stages/01-capture/`, `stages/02-angle/`, `stages/03-draft/references/` |
| Format for publishing | `stages/04-polish/output/`, `stages/05-publish/references/format-guide.md` | everything else |

## Stage Handoffs

Each stage writes its output to its own `output/` folder. The next stage reads from there. If you edit an output file between stages, the next stage picks up your edits. This is the primary way to steer the pipeline.
