# better-prose-writing

A Claude Code plugin and skills-marketplace entry for writing prose that reads
like a person with an opinion.

Model prose sounds the same because the model avoids risk, and the clichés are
what risk avoidance sounds like. A banned-word list does not fix that: cut
"in today's fast-paced world" and the next draft opens with "in an era of
constant distraction". A reader trusts prose that takes a position and shows
something that happened.

## What it does

The plugin ships one skill, `better-prose-writer`. It has two modes, chosen
by the input:

- **Draft mode.** No draft was supplied. It interviews the author for a claim
  and at least one real particular, then writes.
- **Rewrite mode.** A draft was supplied. It keeps the structure, order and
  points, and rewrites it sentence by sentence.

The rules it enforces:

- The claim appears flat, in one sentence, within the first three paragraphs.
- Every paragraph carries one checkable particular: a name, a number, a date,
  a place, a quote, a thing that happened.
- Outside facts come with their source, named and quoted where possible.
- Sentence length swings: at least one sentence past 25 words, at least one
  under 8, and both in any paragraph of four or more sentences.
- The ending is the last point. No summary, no restated thesis, no
  aphorism, no question to the reader.

And one rule above all: **never invent an episode.** A paragraph with nothing
checkable gets a bracketed ask, not a made-up fact. A fake particular is
worse than a cliché, because the author publishes it under their name.

## Install

As a Claude Code plugin:

```bash
/plugin marketplace add johnluther/better-writing-plugin
/plugin install better-prose-writing@johnluther-writing
```

As a skill for any agent that reads `SKILL.md`:

```bash
npx skills add johnluther/better-writing-plugin
```

## Layout

```
better-writing-plugin/
├── .claude-plugin/
│   ├── marketplace.json      # marketplace catalog
│   └── plugin.json           # plugin manifest
├── skills/
│   └── better-prose-writer/
│       ├── SKILL.md          # the instructions
│       ├── ISSUES.md         # friction log for the next revision
│       └── references/
│           ├── samples.md    # ten paragraphs by different writers
│           └── tells.md      # the AI tells to strip
└── LICENSE
```

## Upstream

The skill lives in its own repository,
[github.com/johnluther/better-prose-writer](https://github.com/johnluther/better-prose-writer),
vendored here with `git subtree` so the plugin can be published as one
unit. To pull in upstream changes:

```bash
git subtree pull --prefix=skills/better-prose-writer \
  https://github.com/johnluther/better-prose-writer.git main --squash
```

## License

MIT. Use freely, share widely.
