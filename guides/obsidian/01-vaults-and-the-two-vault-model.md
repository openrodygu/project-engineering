# Vaults and the two-vault model

A vault is a folder that Obsidian opens as a workspace. Inside it, every note is a plain Markdown file and every folder is a real folder. Obsidian stores its settings in a hidden `.obsidian/` folder beside your notes.

That is the whole idea. There is no database and no import step. You can copy a vault, back it up, or open it in another editor without losing anything.

## Why two vaults

Most project work has two different audiences:

| | Team vault | Personal vault |
| --- | --- | --- |
| **Purpose** | Team visibility and coordination | Your individual execution |
| **Tool** | dotpm | TaskNotes |
| **Visibility** | Whole team | Private to you |
| **Answers** | What is the team doing? | What am I doing today? |
| **Location** | `local-project/pm-vault/` | `local-project/personal-project-notes/` |

If you put both jobs in one vault, private plans and team commitments blur together. Someone opens a project view and sees your personal errands. Or you track a team commitment in your private list and the team never sees it. Separate vaults keep the boundary clear.

## The rules that matter

- **The team vault is the team's view.** If work is not there, the team cannot see it.
- **The personal vault is yours.** Keep private notes and daily planning there.
- **Nothing syncs automatically.** No live sync, no import, no cross-vault links.
- **Promote by hand.** When personal work becomes team work, create a matching dotpm task in the team vault. Note the reference in plain text, for example `Shared: Projects/Example Project/define-scope`.
- **One authoritative copy.** Do not keep editing the same commitment in both vaults.

Obsidian links work only inside one vault. A link in the team vault cannot open a note in the personal vault, and the reverse is also true. That is a feature: it makes the boundary visible.

## What goes where

Put a deliverable, blocker, dependency, milestone, or team decision in the team vault. Put your daily plan, personal reminders, research, and uncommitted follow-ups in the personal vault.

When in doubt: if the team needs to see it to coordinate, it belongs in the team vault. If it only affects how you spend your own time, keep it personal.

## Try it

Open your personal vault and create a note called `Vault boundary`.

Write one sentence in your own words:

> Team commitments live in ______, personal execution lives in ______, and I promote work when ______.

Then open the team vault and read its `_README.md`. Compare its rules with your sentence.

Next: [02 Opening the templates](02-opening-the-templates.md)
