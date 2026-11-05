# Plugins and themes

Obsidian stays small by default and grows through plugins. The templates already include the plugins this workspace needs.

## Core and community plugins

**Core plugins** ship with Obsidian. The useful ones here are:

- Search, quick switcher, backlinks, and outgoing links.
- Properties and graph view.
- **Bases**, which TaskNotes needs.
- Templates, daily notes, and file recovery.

**Community plugins** are installed separately. This workspace uses two:

- **dotpm**, listed in the store as **Project Manager**, for the team vault.
- **TaskNotes** for the personal vault.

Obsidian disables community plugins in **Restricted mode**. To use them, open **Settings → Community plugins** and turn restricted mode off. The template vaults already have the plugins installed and enabled.

## The theme

Both templates use the **Border** theme. A theme changes appearance, not data. You can switch back to the default theme at any time under **Settings → Appearance**.

## Installing something new

Only install plugins you trust. A plugin runs with access to your vault files. Before adding one:

1. Check the author and the source repository.
2. Read the permissions or local API settings.
3. Test it in a copy of the vault, not the shared team vault.
4. Never paste API tokens into a note or commit them.

The templates exclude credentials on purpose. Keep it that way.

## Updating plugins

Let Obsidian manage the plugin folder under **Settings → Community plugins**. If you update dotpm or TaskNotes, read the release notes for changes to properties or views. Newer versions usually work, but a major update can change settings.

If a plugin update breaks a view, disable the plugin, reopen Obsidian, and check the template's tested versions before rolling back.

## Keep the setup small

Every plugin adds settings, update work, and a possible failure point. The two plugins in this workspace cover team projects and personal tasks. Add another only when it solves a problem you can name.

## Try it

Open **Settings → Community plugins** in both vaults and write down which plugins are enabled. Then open **Settings → Appearance** and confirm the theme. Change one harmless setting, such as font size, and change it back.

Do not install anything new in the shared team vault without agreement from the people who use it.

Next: [07 Sync and backup](07-sync-and-backup.md)
