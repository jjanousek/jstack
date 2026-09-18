<p align="center">
  <img src="assets/slopify-logo.png" alt="Slopify logo: green audio waves melting into a puddle" width="420">
</p>

# Slopify

Slopify removes generic, inflated, repetitive, and unsupported AI-style writing without flattening the author's voice. It can audit existing material, rewrite it, restate it in plain jargon-free language, draft cleaner copy from scratch, or use a supplied writing sample as a voice reference.

It works as an [Agent Skill](https://agentskills.io/) in Claude Code, Codex, and other compatible tools.

## What it does

- **Audit**: point out likely slop and propose exact replacements without changing anything.
- **Rewrite**: clean up text while preserving facts, meaning, constraints, and useful voice.
- **Simplify**: restate any text, or the agent's previous reply, in plain human language: no jargon, shorter, like one human talking to another.
- **Voice match**: write from supplied facts using the observable traits of a writing sample.
- **Generate**: draft new material while avoiding common AI defaults from the start.

Slopify does not claim to detect whether AI wrote something. It judges the text, not its author.

## Install for Claude Code

Claude Code discovers personal skills under `~/.claude/skills/` and project skills under `.claude/skills/`.

### Personal installation

Use the skill across all your projects:

```bash
git clone https://github.com/jjanousek/slopify.git ~/.claude/skills/slopify
```

Invoke it directly with:

```text
/slopify
```

Claude can also load it automatically when your request matches the description in `SKILL.md`.

If `~/.claude/skills/` did not exist when the current Claude Code session started, restart Claude Code once after installation.

### Project installation

Keep the skill versioned with one project:

```bash
git submodule add https://github.com/jjanousek/slopify.git .claude/skills/slopify
```

Anyone cloning that project can fetch it with:

```bash
git submodule update --init --recursive
```

## Install for Codex

```bash
git clone https://github.com/jjanousek/slopify.git "${CODEX_HOME:-$HOME/.codex}/skills/slopify"
```

Invoke it with:

```text
$slopify
```

## Best way to use it

Give the skill five things when they matter:

1. **Mode**: audit, rewrite, simplify, voice match, or generate.
2. **Scope**: the pasted text, named file, slide range, page, or whole project.
3. **Invariants**: facts, quotations, terminology, formatting, or deliberate slop examples that must remain.
4. **Evidence**: the real figures, sources, events, or decisions the writing may use.
5. **Output**: clean text only, a proposal table, an edited file, or a before-and-after comparison.

Use this prompt shape:

```text
Use Slopify in [mode] mode on [scope].

Audience: [who will read it]
Purpose: [what the writing must accomplish]
Preserve: [facts, wording, formatting, or examples that must not change]
Evidence available: [facts and sources the rewrite may use]
Return: [desired output]
```

### Audit without editing

```text
/slopify Audit this deck for AI slop. Do not edit any files. Separate deliberate
slop examples from the teaching copy and propose exact replacements.
```

### Rewrite while preserving facts

```text
/slopify Rewrite this status update in plain language. Preserve every date,
number, owner, and caveat. Do not add facts or make it more enthusiastic.
Return the revised text first.
```

### Restate without jargon

```text
/slopify Say this more simply. No jargon, keep every fact and number, and make
it read like one person explaining it to another.
```

Works on pasted text or on the agent's own previous reply.

### Match a supplied voice

```text
/slopify Use the writing sample below as a voice reference. Draft a new customer
update using only the facts I provide. Match its directness, rhythm, formality,
and level of detail without copying phrases or inventing personal experiences.
```

A sample of roughly 150 words or more usually gives the skill enough evidence to identify stable voice traits. Include more than one sample when the writer changes style between formats.

### Generate cleaner copy

```text
/slopify Draft a 200-word product update for existing customers. Lead with what
changed and who is affected. Use the supplied release notes as the only factual
source. Avoid unsupported claims and generic launch language.
```

## Repository structure

```text
slopify/
├── SKILL.md                       # Instructions loaded by the agent
├── references/
│   ├── slop-patterns.md           # Diagnostic catalogue
│   └── voice-matching.md          # Sample-based voice workflow
├── agents/openai.yaml             # Codex interface metadata
├── assets/slopify-logo.png        # Repository and skill artwork
└── README.md                      # Installation and usage documentation
```

The README is for people. `SKILL.md` is the runtime entry point used by Claude Code and Codex.

Slopify is an independent parody project and is not affiliated with Spotify.
