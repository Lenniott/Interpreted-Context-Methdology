# Onboarding Questionnaire: Portfolio Case Studies

Read this file when the user types "setup". Ask ALL questions below in a single conversational pass. The user should be able to answer everything in one message. These configure the production system, not a specific case study. The individual project is provided at the start of each pipeline run by the capture stage.

---

### Q1: What is your name (or the name on the portfolio)?
- Placeholder: `{{AUTHOR_NAME}}`
- Files: `author-vault/identity.md`, `author-vault/voice-rules.md`
- Type: free text

### Q2: What is your discipline or role?
- Placeholder: `{{DISCIPLINE}}`
- Files: `author-vault/identity.md`
- Type: free text
- Example: "product designer", "design lead", "UX researcher", "design engineer"

### Q3: What should your portfolio signal about you? What makes your work different?
- Placeholder: `{{POSITIONING}}`
- Files: `author-vault/identity.md`
- Type: free text
- Example: "a systems thinker who ships -- I connect messy business problems to clean, shipped design"

### Q4: Who reads your portfolio, what do they care about, and what do they look for in a case study?
- Placeholders: `{{PORTFOLIO_AUDIENCE}}`, `{{AUDIENCE_CARES_ABOUT}}`, `{{AUDIENCE_LOOKS_FOR}}`
- Files: `author-vault/identity.md`, `author-vault/voice-rules.md`
- Type: free text
- Example: "Hiring managers and design directors. They care about judgment and impact. They look for clear thinking under constraint, not just pretty screens."

### Q5: In one sentence, what should every case study you publish accomplish?
- Placeholder: `{{PORTFOLIO_MISSION}}`
- Files: `author-vault/identity.md`
- Type: free text
- Example: "show how I turn an ambiguous problem into a decision someone can trust"
- Note: If skipped, derive a default from Q3 (positioning) and Q4 (audience).

### Q6: Give me 2-3 sentences that sound exactly like how you write about your work.
- Placeholders: `{{VOICE_RIGHT_EXAMPLE_1}}`, `{{VOICE_RIGHT_EXAMPLE_2}}`
- Files: `author-vault/voice-rules.md`
- Type: free text
- Example: "We cut the onboarding from nine steps to four and watched activation jump." / "The real problem wasn't the form. It was that no one trusted the data behind it."
- Note: These become the positive examples in the Sentence Rules table.

### Q7: Give me 2-3 sentences you would never write in a case study.
- Placeholders: `{{VOICE_WRONG_EXAMPLE_1}}`, `{{VOICE_WRONG_EXAMPLE_2}}`
- Files: `author-vault/voice-rules.md`
- Type: free text
- Example: "I leveraged cross-functional synergies to deliver a best-in-class experience." / "This project was a transformative journey of growth."
- Note: These become the negative examples in the Sentence Rules table.

### Q8: List things that are always errors in your writing. Patterns, phrases, or habits to avoid.
- Placeholders: `{{VOICE_HARD_CONSTRAINT_1}}`, `{{VOICE_HARD_CONSTRAINT_2}}`, `{{VOICE_HARD_CONSTRAINT_3}}`
- Files: `author-vault/voice-rules.md`
- Type: free text
- Example: "Resume verbs like 'spearheaded'." / "Claiming a result without a number or source." / "Burying the decision under process description."
- Note: These become the numbered error list in Hard Constraints. If fewer than 3 are given, derive the rest from the Q6/Q7 examples. Also derive `{{VOICE_PACING_DESCRIPTION}}`, `{{VOICE_ANTI_PATTERN}}`, and `{{VOICE_ANTI_PATTERN_DESCRIPTION}}` from Q6-Q8.

### Q9: Which kinds of value do your case studies most need to deliver? (pick at least 2)
- Placeholders: `{{VALUE_CRAFT_DESCRIPTION}}`, `{{VALUE_IMPACT_DESCRIPTION}}`, `{{VALUE_THINKING_DESCRIPTION}}`, `{{VALUE_COLLABORATION_DESCRIPTION}}`, `{{VALUE_CREDIBILITY_DESCRIPTION}}`
- Files: `shared/value-framework.md`
- Type: free text
- Options to reference: DEMONSTRATES-CRAFT, SHOWS-IMPACT, REVEALS-THINKING, PROVES-COLLABORATION, BUILDS-CREDIBILITY
- Example: "Mostly REVEALS-THINKING and SHOWS-IMPACT. My work is judged on decisions and results."
- Note: The agent fills a concrete description for all five value types, marking which ones you lean toward. Any type you do not mention still gets a short generic description so the framework stays complete.

### Q10: How long should a typical case study be?
- Placeholder: `{{TARGET_LENGTH}}`
- Files: `shared/case-study-anatomy.md`
- Type: free text
- Default: "800-1200 words, a 4-6 minute read"

### Q11: Do you want a publishing stage that formats case studies for a specific platform?
- Placeholder: `{{PUBLISH_PLATFORM}}`
- Files: `stages/05-publish/CONTEXT.md`, `stages/05-publish/references/format-guide.md`
- Type: yes/no, then free text
- If YES: Keep `stages/05-publish/` and the `{{?PUBLISH_STAGE}}` section in `CONTEXT.md`. Fill `{{PUBLISH_PLATFORM}}` with the named platform (for example "portfolio site", "Notion", "PDF") and trim the unused platform sections in `format-guide.md`.
- If NO: Remove `stages/05-publish/` entirely. Remove the `{{?PUBLISH_STAGE}}...{{/PUBLISH_STAGE}}` block from `CONTEXT.md`.

---

## After Onboarding (Two-Pass Process)

**Pass 1:** Collect all answers above and replace the direct placeholders.

**Pass 2 (Voice Review):** After replacing placeholders, present the generated voice rules to the user:

"Here are the voice rules I derived from your examples. Review these and edit anything that does not match how you actually write:"

Show the populated Hard Constraints, Sentence Rules table, and Pacing section. The user edits before the rules are finalized. This catches misinterpretations and produces better rules than one-shot derivation.

**After both passes:** Derive and fill remaining fields:
1. Pacing description and anti-patterns (from Q6-Q8)
2. Portfolio mission, if skipped (from Q3 and Q4)
3. Value framework descriptions for all five types (from Q9)

Then scan every `.md` file for remaining `{{` patterns. If any remain, resolve them. Tell the user:

"You are set up. Your case study system is configured with your voice, audience, and value framework. To write a case study, just tell me which project it is about."
