---
name: slopify
description: Remove AI slop from prose, presentations, websites, interfaces, emails, memos, reports, documentation, and other written material; audit suspected slop without editing; rewrite while preserving meaning and facts; restate text or a previous reply in plain jargon-free language; or generate new text in the observable voice of a user-supplied sample. Use for requests such as de-slop, desloppify, unslop, remove AI wording, make this sound natural, clean up AI copy, identify AI-writing tells, avoid generic AI style, say it simply, no jargon, bro, or match this sample's voice.
---

# Slopify

Make the writing clear, precise, and concise. Diagnose patterns in the text, preserve what is true and intentional, and remove language that is generic, inflated, repetitive, or unsupported. Prefer the plain words one person would say to another.

## Choose the mode

- **Audit**: Identify problems and propose replacements. Do not edit files or silently rewrite the text.
- **Rewrite**: Return or apply a cleaner version while preserving meaning, facts, constraints, and useful voice.
- **Simplify**: Restate a text, or your own previous reply, in plain human language: no jargon, shorter, and coherent, like one human talking to another.
- **Voice match**: Rewrite or generate text using the observable traits of a supplied writing sample.
- **Generate**: Draft new text that avoids the common defaults from the start.

Honor scope literally. If the user says “proposal only,” “do not edit,” or marks passages as deliberate examples of slop, leave them untouched.

## Load the references

Read [references/slop-patterns.md](references/slop-patterns.md) for every task. Use it as a diagnostic catalogue, not a word blacklist.

For voice matching, also read [references/voice-matching.md](references/voice-matching.md).

## Follow the workflow

### 1. Establish the job

Identify:

- the audience, purpose, and medium;
- whether the user wants an audit, rewrite, file edit, or new draft;
- the requested level of intervention;
- any text that must remain verbatim, including quotations, examples, legal language, terminology, and intentional slop specimens;
- the facts and claims that must survive.

Inspect the actual artifact when a file, deck, page, or repository is in scope. For visual work, distinguish visible copy from code and layout. Do not refactor implementation code unless the user asks.

### 2. Protect substance

Create an internal preservation list before rewriting:

- verified facts, figures, dates, names, and citations;
- decisions, instructions, caveats, and calls to action;
- domain terms that are precise even if they sound formal;
- the author's real opinions, humour, and deliberate rhetorical choices;
- formatting required by the medium.

Never invent a number, source, anecdote, opinion, failure, personal experience, or named person to make writing seem human. If the draft needs evidence the user has not supplied, flag the gap, ask for the fact when necessary, or use an explicit placeholder.

### 3. Diagnose before rewriting

Review the material at five levels:

1. **Substance**: What does it actually claim? Is it specific and checkable?
2. **Language**: Which words or phrases add ceremony but no meaning?
3. **Structure**: Are lists, contrasts, summaries, or dramatic fragments being used automatically?
4. **Tone**: Does every sentence sound equally polished, positive, formal, or enthusiastic?
5. **Presentation**: Does formatting or visual styling create importance that the content has not earned?

Treat patterns as evidence only when they cluster. An em dash, a formal word, a list, or a clean sentence is not a verdict. Do not claim to determine authorship from style.

### 4. Rewrite in passes

Use the smallest set of passes that solves the problem:

1. **Cut** throat-clearing, repeated conclusions, decorative modifiers, fake transitions, and empty closing lines.
2. **Clarify** inflated verbs, abstract nouns, jargon, and indirect constructions with plain, accurate language.
3. **Ground** general claims in supplied, verified facts. If no facts are available, expose the gap rather than filling it with fiction.
4. **Reshape** automatic threes, false contrasts, uniform paragraph rhythms, and excessive bullets only where they weaken the text.
5. **Restore voice** by keeping purposeful quirks, varied sentence lengths, real opinions, and medium-appropriate tone.
6. **Read cold** and remove any new slogan, metaphor, summary, or flourish introduced during the rewrite.

Prefer deletion over replacement. Do not turn every sentence into a short sentence. Do not replace one set of stock phrases with another.

### 5. Verify

Compare the result with the preservation list and confirm:

- no fact, qualification, instruction, or source changed;
- no evidence or personal detail was invented;
- the main point appears sooner;
- each remaining sentence adds information, necessary tone, or useful rhythm;
- formatting supports the content instead of disguising its absence;
- the result still fits the author, audience, and medium;
- deliberate examples and quoted material remain intact.

## Simplify on request

When the user asks for a plain restatement — "say it simply", "no jargon", "what does this actually mean", or a quick "bro" — skip the full workflow and restate the text, or your own previous reply, directly:

- Lead with the point in the first sentence.
- Swap jargon, acronyms, and abstract nouns for the words you would say aloud to a colleague. Keep a technical term only when no plain word means the same thing, and gloss it on first use.
- Keep every fact, number, caveat, and instruction. Simplify the language, never the claims.
- Cut hedging, framing, and repeated context until only information remains.
- Read the result as speech. Rewrite any sentence you would not say to a person.

Return the restatement alone, with no preamble and no notes.

## Return the right output

For a short rewrite, return the revised text first. Add notes only when they help.

For an audit, use a compact table with:

| Location or excerpt | Problem | Proposed change |
|---|---|---|

Separate high-impact problems from optional polish. Include exact replacement wording where practical.

For a file edit, report the files changed, the main simplifications, the checks performed, and any remaining content gaps. Do not describe authorship as proven.

For a voice-matched draft, provide the draft. Include the voice brief only when the user requests it or when the sample is too short or inconsistent for a reliable match.

## Keep these boundaries

- Judge text; do not accuse or diagnose its author.
- Treat specificity as useful only when it is true or clearly marked as a placeholder.
- Preserve intentional style. A rhetorical device is not slop merely because models overuse it.
- Do not add fake typos, slang, vulnerability, personal stories, or random sentence fragments as “human” signals.
- Do not flatten strong writing into bland minimalism. The goal is precise, recognisable writing, not sterile writing.
