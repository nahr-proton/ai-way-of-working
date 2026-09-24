# Instruction file snippet

**What it is:** one paragraph that points every coding assistant at `patterns.md` and the release checklist.
**Who fills it in:** the tool owner, once per repo. The two blanks take a minute.
**When:** the same day `patterns.md` lands at the root of the repo. Check it again whenever the checklist moves.

## Where it goes

Paste the paragraph below into the instruction file your coding assistants read at the root of the repo. As of September 2026, two examples are `AGENTS.md` and `CLAUDE.md`. If you have more than one, paste it into each.

Prototyping tools and hosted app builders work outside the repo and cannot read it. Paste the whole of `patterns.md` into the tool's project instructions instead, and paste it again when `patterns.md` changes.

## The paragraph

```markdown
## Screens, components and text a customer sees

Before you generate or change any screen, component or text a customer sees, read `patterns.md` at the root of this repo and follow it. If a request conflicts with it, follow `patterns.md` and say so. Use the components it lists; do not add a new component, color, font size or spacing value without asking {{experience quality owner}}. Never write a price, a policy, a legal term or a promise: write {{PLACEHOLDER}} and flag it. If the change touches anything in section 8 of `patterns.md`, stop and say that it belongs in the high lane before you go on. Every screen you touch handles the empty, loading, error, success and too much states, and the accessibility rules in section 7. Before the change goes to review, fill in the release checklist evidence in {{path to PULL_REQUEST_TEMPLATE.md}}: the lane, the kind of change, and one screenshot per state the change touches where you can capture it. Say plainly which states you could not capture or check, so the author does it. The person who opens the pull request is its author and owns it; you do not approve it.
```

## Check that it works

Ask the assistant to add a small list screen. It should mention `patterns.md`, use a listed component, and include an empty state. If it does none of that, the assistant is not reading the file. Fix the location before anything else.
