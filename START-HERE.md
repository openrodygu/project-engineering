# Start Here

A short orientation. Browsing takes about 5 minutes; a skill quick start takes 15–30 minutes.

## 0. Access the handbook

- **Browser:** read here. Use the file list or the links on each page.
- **Obsidian:** install Obsidian, get the files in step 2, then choose **Open folder as vault** and select the folder.

New to Obsidian? [Obsidian basics](guides/obsidian/00-obsidian-basics.md) covers install, setup, and use.

Then continue with step 1.

## 1. Choose your path

- **Browse** — keep reading. No setup.
- **Learn** — get the files and do one skill quick start.
- **Adopt** — copy a template or practice into your own workspace.
- **Contribute** — fork, branch, and open a pull request. Optional.

## 2. Get the files

If you are reading in the browser, skip this step.

**Download only (no Git):** [download the ZIP](https://github.com/openrodygu/project-engineering/archive/refs/heads/main.zip) and extract it. To use the templates, copy a template folder out and open the copy in Obsidian.

**With Git:**

```sh
git clone https://github.com/openrodygu/project-engineering.git
cd project-engineering
```

The [Git skill](guides/git/) will teach clone later.

To read the handbook in Obsidian, open the cloned or extracted repo folder as a vault. See [Obsidian basics](guides/obsidian/00-obsidian-basics.md).

## 3. Create a practice workspace (optional)

If you want a place for the exercises, create this structure in your file explorer or terminal:

```text
local-project/
├── pm-vault/
├── personal-project-notes/
└── source/

backup-remote-location/         # optional local bare remote
hosted-service/                 # GitHub, not a local folder
```

Then:

1. Copy the contents of `templates/team-vault/` into `local-project/pm-vault/`, including the hidden `.obsidian` folder. Use a desktop file manager.
2. Copy the contents of `templates/personal-vault/` into `local-project/personal-project-notes/`, including the hidden `.obsidian` folder.
3. If you use Git, run `git init` inside `local-project/source/`. If you do not, skip this line; you do not need Git for the exercises.

The full structure is explained in [templates/project-workspace/README.md](templates/project-workspace/README.md). You can use any folder names you like.

## 4. Pick one skill

Open [guides/README.md](guides/README.md) and choose one.

If you are not sure, start with:

- **Project management** if you need to plan work.
- **Git** if you need version control.
- **Obsidian** if you want to use the vault templates.
- **Self-management** if your own task list is the problem.
- **Team lead** if people are the hard part.

## 5. Do the quick start

Every skill README begins with **Do this now**.

- It takes 15–30 minutes.
- It produces a concrete artifact.
- It does not require the other skills.

## 6. Stop or go deeper

After the quick start, you can:

- Stop there.
- Read the skill’s deeper chapters.
- Read the [handbook](handbook/) for the system view.
- Adopt the [templates](templates/) in a real project.
- Contribute an improvement to the repo.

## The first loop

1. Pick a skill.
2. Read **Do this now**.
3. Produce the artifact.
4. Reflect on what helped.
5. Choose the next skill.

That is the whole learning model.

## Where to go next

- [README](README.md)
- [Skill catalog](guides/README.md)
- [Handbook](handbook/README.md)
- [Templates](templates/README.md)
- [Contributing](CONTRIBUTING.md)
