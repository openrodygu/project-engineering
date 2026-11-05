# Markdown and notes

Every note in Obsidian is a Markdown file. You do not need to be a Markdown expert, but you should recognize the basics because dotpm and TaskNotes write Markdown for you.

## The syntax you need

```markdown
# Heading 1
## Heading 2

**bold** and *italic*

- bullet
- another bullet

1. numbered
2. list

- [ ] open checkbox
- [x] done checkbox

| Column | Value |
| --- | --- |
| Status | In progress |

[A link](https://help.obsidian.md)
```

Markdown is readable as plain text. That matters when you search the vault, diff a file, or open it outside Obsidian.

## Callouts

Callouts are blockquotes with a type. Obsidian renders them as colored boxes.

```markdown
> [!tip] Helpful
> This is a tip.

> [!warning] Careful
> This is a warning.
```

Use callouts for onboarding notes, warnings, and short context that should stand out. Do not use them on every note.

## How notes are stored

A note is a file. Its name is its filename, and its folder is its real folder. There is no hidden database.

That simple fact gives you:

- **Search** across the whole vault, including properties.
- **Backlinks** that show which notes point to the current note.
- **Portability** across editors and sync tools.
- **One file per task** in dotpm and TaskNotes, which keeps conflicts small.

## Write for the next reader

A useful note answers three questions quickly:

1. What is this?
2. Why does it exist?
3. What should someone do next?

Put the answer near the top. Long notes with no opening sentence are hard to reuse.

## Try it

In your personal vault, create `Practice note.md` with:

- One heading.
- Three bullets describing what you are working on.
- One open checkbox for the next action.
- One callout with a tip or warning.
- A small table with two columns.

Then switch to source mode and look at the Markdown. Notice that the rendered note and the source are the same file.

Next: [04 Links, properties, and dotpm](04-links-properties-and-dotpm.md)
