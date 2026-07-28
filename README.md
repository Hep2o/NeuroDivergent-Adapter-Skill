ND-Adapter

A prompt-based communication adapter that makes AI interactions work better for neurodivergent users.

What it does

The ND-Adapter is a communication layer you add to any AI system — Claude, Copilot, ChatGPT, or others. It adjusts how the AI responds so that output is shorter, clearer, better structured, and easier to process.

It covers four ND profiles: dyslexia, ADHD, autism, and dyspraxia. It works across all four simultaneously because most ND people have traits across more than one.

Core principle: the adaptation burden sits with the AI, not the person. The tool changes the interface, not the user.

Before / After

Q1 — Summarise a project update:

Without ND-Adapter	With ND-Adapter
The supplier may deliver the parts on Thursday, but the date is uncertain due to a backlog. If the delivery is delayed, the testing schedule will need to be adjusted. The documentation folder may also be missing the latest version and needs to be reviewed.	Here are the main points:
• parts might arrive Thursday, but not confirmed
• if they don't arrive, testing will need to move
• the documentation folder may be missing the latest version

Q2 — Simplify a technical explanation:

Without ND-Adapter	With ND-Adapter
The system works only when run in a specific sequence. If the sequence isn't followed, it triggers a false error caused by a leftover flag from the previous run. Resetting the workflow may resolve the issue.	Here is a simpler version:
• the system works, but only in a set order
• running it out of order shows a false error
• the error is a leftover flag from the last run
• resetting the workflow might fix it

Q3 — Pull key points from a messy email:

Without ND-Adapter	With ND-Adapter
The sender needs to reschedule the meeting because they are double booked. They are available later today or tomorrow morning and are open to whichever time works best.	Key points:
• they need to move the meeting
• they're double booked with a call they can't move
• they're free later today or tomorrow morning

Q4 — Handle fragmented, non-linear input:

Input	Without ND-Adapter	With ND-Adapter
"hmm it needs the accual example like um! lets do it, summarise the conversation in A/B test form"	You asked for an example that demonstrates the difference between a normal summary and an ND-Adapter summary. Throughout the conversation, we developed the ND-Adapter prompt, created divergent prompts, and built A/B examples. You then requested a full summary using your exact wording without corrections.	Here is the summary:
• you asked for an A/B example
• we built the ND-Adapter rules
• we added the quick-use version
• we created Q1–Q4 tests
• you asked for the conversation to be summarised using your exact wording

Q1–Q3 show clearer output. Q4 shows what makes the ND-Adapter different — it extracts intent from fragmented, non-linear input instead of asking you to rephrase.

What's in this repo
File	What it is
nd-adapter-skill.md	The full skill — toggle, builder workflow, and evidence data
canonical-prompts.md	The short-form and long-form ND-Adapter prompts, ready to copy and paste
setup-and-origin.md	Setup instructions for Claude, Copilot, and ChatGPT, plus the transparency note
Quick start
Open canonical-prompts.md
Copy the short-form prompt (or long-form if you want granular control)
Paste it into your AI system's custom instructions or at the start of a conversation
That's it — the AI will adapt its responses from that point on
Where to paste it
Claude: Settings → Profile → Personal preferences
Copilot: Settings → Custom instructions / Personalisation
ChatGPT: Settings → Personalisation → Custom instructions
What the adapter adjusts
Sentence structure — short sentences, one idea each, active voice, no nested clauses
Language — plain English structure, but preserves technical vocabulary when you demonstrate expertise
Formatting — numbered lists for sequences, bullets for options, chunked output, clear headings
Intent extraction — pieces together fragmented or non-linear input and states interpretation before answering
Cognitive load — one thing at a time, summaries for long answers, no decorative bold
The builder workflow

The skill also includes a guided builder for creating your own ND-Adapter for a team, network, or organisation. It walks through six stages: understanding context, selecting ND profiles, choosing a format, drafting the tool, testing, and packaging for distribution.

Who made this

Created through a human-led, AI-supported process. The concept, structure, categories, and reasoning came from lived experience of ND communication needs. AI was used as an editing tool to tighten language and formatting — not to generate the ideas or design.

Full transparency note in setup-and-origin.md.

Licence

MIT — use it, adapt it, share it. Attribution appreciated.
