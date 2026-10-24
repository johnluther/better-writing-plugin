# better-prose-writer (Better Prose Writer): Issues Log

If following this skill produces friction, ambiguity, a wrong output, or a gap in its
instructions, append an entry here. A workaround of your own does not remove the need
for an entry. This log is the raw input for the next revision of `SKILL.md`. If the
friction is not written down here, it disappears the moment you solve it and the next
person hits it fresh.

Newest entries at the top. Do not edit or delete past entries. If one turns out to be
wrong or already fixed, add a note under it instead of removing it.

## Entry format

```
### YYYY-MM-DD: [short description]
**Step:** Intake / Samples / Shape / Pass / Hand over / Rewrite
**What happened:** [the situation, in enough detail that a reader who was not there understands it]
**Gap in the skill:** [what SKILL.md did not cover, or covered ambiguously]
**What you did about it:** [your workaround or decision]
**Suggested fix:** [optional: a concrete change to SKILL.md]
```

---

### 2026-10-24: Documentation is not narrative prose
**Step:** Rewrite / Shape
**What happened:** Ran the skill over this repo's README. The README is a functional document: install commands, a file tree, a subtree command, a license line. The skill's shape rules (no headers under 800 words, every paragraph carries a checkable particular, the ending is the last point) are written for narrative prose. Applied literally, they would delete the headings and force rewrites of the commands.
**Gap in the skill:** "Unless the author asked for that form" covers headers, but nothing covers functional blocks that carry no particular and must not be rewritten, nor the fact that a README reader arrives for the commands and not the argument.
**What you did about it:** Rewrote only the prose. Kept the headings, their order, the code blocks and the tree untouched, and kept the one-line lead-in that introduces each block. Moved the plugin identity below the claim, since the first sentence of the README now has to earn the click.
**Suggested fix:** Add to "The shape of the piece": "In a document (README, doc page, changelog), rewrite only the prose. Keep the functional blocks, the heading order and the lead-in for each block; apply the claim, particular and rhythm rules to the prose paragraphs alone."
