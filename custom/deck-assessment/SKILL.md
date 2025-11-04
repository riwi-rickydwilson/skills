---
name: deck-assessment
description: Analyze PowerPoint presentations for narrative clarity, design quality, and executive readiness. Use when user requests deck scoring, feedback, or assessment of presentation quality. Supports both pitch decks (investor/stakeholder presentations) and update/brief decks (internal status reports, progress reviews). Auto-detects deck type and applies appropriate evaluation rubric.
---

# Deck Assessment

Evaluate PowerPoint decks using standardized storytelling and slidewriting rubrics. Deliver structured scores with specific, actionable feedback.

## Workflow

### 1. Detect Deck Type

Analyze the deck to determine whether it is a **Pitch Deck** or **Update/Brief Deck** based on these indicators:

**Pitch Deck signals:**
- Problem-solution structure
- Market opportunity framing
- Investment ask or funding context
- Competitive positioning
- Team credentials or founder story
- Future vision or growth roadmap

**Update/Brief Deck signals:**
- Progress reporting or status updates
- RAG (Red/Amber/Green) status indicators
- Decision documentation
- Risk or issue tracking
- Operational or quarterly metrics
- Internal stakeholder focus

**If deck type is ambiguous:** This is itself meaningful feedback. Note in the Executive Summary that the deck's purpose is unclear, which indicates a fundamental narrative problem.

### 2. Load Appropriate Rubric

Based on deck type detection:
- **Pitch Deck:** Read `references/pitch_deck_rubric.md`
- **Update/Brief Deck:** Read `references/update_brief_rubric.md`

### 3. Score Each Category

Apply the rubric criteria (scored 1-10) for each category. Use the detailed scoring bands in the rubric to guide assessment.

Calculate Overall Score: Multiply each category score by its weight, then sum to 100.

### 4. Generate Feedback

Produce structured output following the format below.

## Output Format

Deliver assessment as a structured report:

### Overall Score
- Numeric score (0-100)
- One-sentence summary of overall quality

### Executive Summary
3-5 bullet points capturing:
- Primary strengths
- Critical weaknesses
- Deck type classification (and if unclear, state that explicitly)

### Category Breakdown
For each rubric category:
- **Category Name (Weight%):** Score/10
- 2-3 sentences explaining the score with specific observations

### Top 3 Improvements
Ranked list of highest-impact changes:
1. **[Improvement]:** Brief explanation of why and how
2. **[Improvement]:** Brief explanation of why and how
3. **[Improvement]:** Brief explanation of why and how

### Storyline Map
High-level outline of the deck's narrative flow. Identify:
- Opening/framing
- Key progression of ideas
- Closing/resolution
- Gaps or logical breaks in the story

### Slide Feedback Summary
Thematic issues across the deck (NOT per-slide commentary):
- Common design problems
- Recurring message clarity issues
- Data presentation patterns
- Consistency gaps

### Action Title Rewriter
Select 3-5 slides with weak headlines. Rewrite them as strong action titles:
- **Original:** [Generic or weak title]
- **Revised:** [Clear, declarative, action-oriented title]

## Response Tone

Executive. Specific. Constructive.

Write like a senior communications coach advising a CEO:
- Be direct but not harsh
- Focus on impact, not aesthetics
- Prioritize clarity over cleverness
- Give concrete examples when critiquing
- Avoid subjective design opinions

## Guidelines

**Focus on:**
- Clarity: Can the message be understood quickly?
- Structure: Does the narrative flow logically?
- Logic: Do claims follow from evidence?
- Professionalism: Is it ready for the stated audience?

**Avoid:**
- Personal or stylistic critiques unrelated to effectiveness
- Aesthetic opinions ("I don't like this color")
- Speculation about intent without evidence in the deck
- Overwhelming detail (keep feedback actionable and prioritized)
