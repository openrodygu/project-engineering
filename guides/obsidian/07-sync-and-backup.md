# Sync and backup

A vault is a folder of files, so sync and backup are file operations. You do not need a special export step.

## Sync options

| Option | Good for | Watch out for |
| --- | --- | --- |
| Shared drive or network folder | Team vault | One editor per file at a time |
| OneDrive, iCloud, Dropbox | Personal vault across devices | Conflict copies |
| Obsidian Sync | Paid, built-in, selective sync | Separate from your file backup |
| Git | Version history and review | Merge conflicts on binary or plugin files |

The team vault usually lives in a shared drive. The personal vault can live wherever you like. Do not point both vaults at the same sync folder; the boundary is easier to keep when the folders are separate.

## Conflict copies

If two devices edit the same note before sync resolves, the sync tool may create a file such as:

```text
define-scope.conflict-2026-11-04.md
```

Treat it like any other conflict:

1. Open both files.
2. Compare the differences.
3. Keep the correct content in the original.
4. Delete the stale copy.

One file per task keeps conflicts rare. Two people editing two different tasks are editing two different files.

## Back up the vault folder

A backup is a copy of the whole folder, including `.obsidian`. Make one on a schedule that matches how much work you would hate to lose.

- Keep at least one backup outside the sync service.
- Name backups with a date, for example `pm-vault-2026-11-04`.
- Test a restore once. A backup you have never restored is a hope, not a backup.

Obsidian's **File recovery** core plugin keeps a local undo history. It helps after an accidental edit, but it is not a substitute for a real backup.

## Do not sync secrets

The vault is plain text. Do not store API tokens, passwords, or private customer data in it. If a plugin offers a local API, treat its token as a secret and keep it out of the vault and out of version control.

## Try it

Make a dated copy of your personal vault. Then delete a practice note, open **File recovery**, and restore it. Finally, compare the restored note with the backup copy.

Next: [08 Sharing and publishing](08-sharing-and-publishing.md)
