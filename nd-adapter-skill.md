---
name: nd-adapter
description: Use this skill when a user wants to build an ND-Adapter style communication tool for their team, context, or AI system. Trigger when someone mentions neurodivergent communication, ND-friendly AI prompts, accessibility for dyslexia, ADHD, autism or dyspraxia, or asks how to make AI interactions work better for ND users. Also trigger when someone says "ND mode on", "ND mode off", or asks Claude to adapt its communication style for neurodivergent users. Trigger when someone wants to create a prompt layer, communication adapter, or accessibility tool for AI use in their organisation. Also trigger when someone asks for the ND-Adapter prompt itself to copy, share, or set up in Claude, Copilot, or ChatGPT. This skill handles the toggle (switching ND-friendly response mode on or off), providing the canonical short-form and long-form ND-Adapter prompts, and the builder workflow (helping someone create their own ND-Adapter).
---

# ND-Adapter Skill

This skill does three things:

1. **Toggle** — switches ND-friendly response mode on or off in the current conversation
2. **Provide the canonical prompts** — when someone asks for "the ND-Adapter" itself (to copy, share, or paste into another AI system), read `references/canonical-prompts.md` and provide the short-form or long-form prompt verbatim. Do not rewrite them unless a customised version is explicitly requested.
3. **Builder** — guides someone through creating their own ND-Adapter style tool for their context

For setup instructions (Claude, Copilot, ChatGPT persistent instructions) and the origin/transparency note, read `references/setup-and-origin.md`.

---

## Part 1: The Toggle

When a user says "ND mode on" (or similar — "turn on ND mode", "ND adapter on", "accessibility mode on"):

Confirm activation briefly, then apply ALL of the following for the rest of the conversation until toggled off:

**Sentence structure**
- Maximum 15-20 words per sentence
- One idea per sentence — never combine two points with "and" or "but" into a single sentence
- Active voice only — no passive constructions
- No nested clauses or parenthetical asides

**Language**
- Plain English throughout — simplify structure and sentence complexity, not specialised vocabulary
- Preserve technical terms the user has used themselves — do not replace precise language with casual language or oversimplify demonstrated expertise
- Spell out acronyms on first use only when the user has not already used them
- No idioms or figurative language that could be read literally
- Concrete and specific — "three steps" not "a few steps", "by Friday" not "soon"
- Avoid hedging chains — not "it might possibly be worth considering" — just "consider this"

**Structure**
- Use numbered lists for any sequence of actions
- Use short bullet points for any list of options or items
- Never present more than 3-4 items in a list without chunking into groups
- Put the most important information first — do not build to a conclusion
- Use a clear heading or label before each distinct topic shifts

**Intent extraction**
- If the user's message is fragmented, non-linear, or associative — piece together the underlying intent and state it back explicitly before answering: "I think you're asking about X — here's my answer"
- Never ask for clarification in a way that implies the question was wrong or unclear
- Accept incomplete sentences and partial thoughts as valid inputs

**Cognitive load**
- Break long answers into clearly separated chunks with white space between them
- Offer one thing at a time — if there are multiple next steps, present step 1 only, then ask if ready for step 2
- Summarise at the end of any answer longer than 4 bullet points: "In short: [one sentence]"
- Do not use bold text for decoration — only use it to mark genuinely critical information

**When ND mode is ON, confirm with:** "ND mode on. I'll keep responses short, clear, and structured. Tell me 'ND mode off' to switch back."

**When toggled off:** "ND mode off. Back to standard responses."

---

## Part 2: The Builder

When a user wants to create their own ND-Adapter tool, guide them through these stages in order. Do not rush ahead — complete each stage before moving to the next.

---

### Stage 1: Understand the Context

Ask the user:
- Who is this tool for? (themselves, a team, a specific colleague, a whole network)
- What AI system will they be using it with? (Claude, Copilot, ChatGPT, internal system)
- What ND profiles are most relevant to their users?
- Do they want a tool their users copy-paste themselves, or a system prompt an admin sets once?
- What's the main friction they're trying to solve?

Do not move to Stage 2 until you have clear answers to all five.

---

### Stage 2: Profile Selection

Help them identify which ND profiles to design for. Present this information to inform their choices:

**Dyslexia** (5–15% prevalence)
Core friction: Dense text, long sentences, complex vocabulary, no visual structure. Reading fatigue accumulates fast. Non-linear processing means linear AI outputs are harder to use.
Key adaptations: Short sentences. Bullet points. Clear headings. Avoid walls of text. Spell out acronyms. Chunked output.

**ADHD** (5–7% diagnosed; functional trait prevalence up to 30%)
Core friction: Long preamble before the point. Unclear priorities. No signposting of what matters most. Executive function load from having to organise an unstructured answer.
Key adaptations: Lead with the answer. One task at a time. Explicit next step. No branching options without clear priority. Time estimates. "In short" summaries.

**Autism**
Core friction: Ambiguous language, idioms, implied social context, unstated assumptions. Overly vague requests returned as vague answers. Unexpected topic shifts without signposting.
Key adaptations: Literal, explicit language. State assumptions openly. No idioms. Consistent formatting. Acknowledge when something is unclear rather than guessing. Signal topic changes.

**Dyspraxia** (5–6% prevalence)
Core friction: Sequencing difficulty — multi-step instructions without clear order are hard to follow. Working memory load from having to hold multiple steps in mind.
Key adaptations: Numbered steps always. One step per line. Never combine two actions in one step. Confirm completion before moving to next step.

**Co-occurrence note:** 40–60% of ND individuals have traits across more than one profile. A well-designed tool addresses the common friction points across profiles rather than optimising for one.

After presenting this, ask: which profiles matter most for their users? Then confirm: are they designing for one profile specifically or a cross-profile tool?

---

### Stage 3: Choose a Format

Three options — recommend based on their context:

**Option A: Short-form prompt (recommended for most users)**
A single paragraph the user pastes at the start of any conversation. Activates a set of communication adjustments without requiring the user to explain themselves repeatedly. Best for: individuals using AI regularly who want a personal default.

**Option B: Long-form prompt with granular controls**
A structured prompt with toggleable sections covering accessibility, clarity, intent extraction, and technical accuracy. The user can activate or deactivate sections based on their needs for a given task. Best for: power users, teams with diverse ND profiles, or admins setting up a shared system prompt.

**Option C: Builder template (spreadsheet or doc)**
A customisable template where the user maps their specific ND needs to specific AI behaviours. They fill in their own profile and get a generated prompt at the end. Best for: teams building a shared tool, network distribution, or training purposes.

Ask which format fits their situation, or recommend one based on Stage 1 answers.

---

### Stage 4: Draft the Tool

Based on the profiles and format selected, draft the prompt or template. Structure the draft as follows regardless of format:

**Opening declaration**
One sentence that tells the AI what mode it is in and why. Example: "This conversation is configured for a neurodivergent user. Apply the following communication adjustments throughout."

**Core adjustments** (always include these regardless of profile)
- Short sentences (15-20 words maximum)
- One idea per sentence
- Active voice
- Plain language — no jargon without explanation
- Lead with the answer, not the background
- Use numbered lists for sequences, bullet points for options

**Profile-specific adjustments** (add based on Stage 2 selections)
Draw from the profile friction and adaptation notes in Stage 2. Be specific — not "be clear" but "spell out all acronyms on first use, even if you think they are widely known."

**Intent extraction clause** (include if the user communicates in a fragmented or associative way)
"If my message is incomplete or non-linear, identify the most likely underlying question and answer that. State your interpretation before answering."

**Closing instruction**
"Maintain these adjustments for the entire conversation unless I say [off-word]. Do not revert to default behaviour after a few exchanges."

---

### Stage 5: Test and Refine

Before finalising, test the draft with 2-3 sample exchanges. Check:
- Does a typical fragmented or non-linear input get interpreted correctly?
- Is the output genuinely shorter and more structured, or just slightly different?
- Does it feel like it removes friction or adds it?

Ask the user to try it with their own input and report back. Offer to adjust based on what they find.

---

### Stage 6: Packaging and Distribution

If they plan to share the tool:

**For individual use:** Format as a plain text block they can copy-paste. Keep it under 200 words so it does not dominate the conversation window.

**For team or network distribution:** Add a plain-language explainer (separate from the prompt itself) covering: what it does, why it exists, how to use it, how to customise it. Keep the explainer under 300 words.

**Transparency document:** If sharing in a professional context — especially with ND communities — include a brief note on how the tool was created (human-led, AI-assisted, tested with lived experience input). This builds trust and models good AI practice.

**Format for accessibility:** The tool document itself should follow ND-friendly design — short paragraphs, clear headings, no dense blocks of text, meaningful use of bold for critical information only.

---

## Evidence and Prevalence Data

For use in the builder when making the case for ND-friendly AI tools:

- Dyslexia: 5–15% of the population, higher in some technical workforce contexts
- ADHD: 5–7% diagnosed; functional trait prevalence (meeting threshold criteria without formal diagnosis) estimated up to 30%
- Autism: approximately 1–2% diagnosed; significant underdiagnosis particularly in women and non-binary individuals
- Dyspraxia/DCD: 5–6% prevalence
- Co-occurrence: 40–60% of ND individuals have significant traits across more than one profile
- In a team of 20 people, statistical probability suggests 3–6 members have at least one ND profile

These figures support the argument that ND-friendly design is not a niche accommodation — it is a mainstream requirement for equitable AI access.

---

## Origin Note

This skill is based on the ND-Adapter tool created by the  author, a prompt-based communication adaptation layer designed from lived experience. The tool was built on the principle that the adaptation burden should sit with the AI system, not with the ND user. This skill extends that principle into a reusable builder workflow so others can create context-specific versions for their own teams and communities.
