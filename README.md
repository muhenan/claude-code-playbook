# claude-code-playbook

A personal repository for quickly setting up Claude Code on a new machine. Clone this repo and copy the files to the appropriate paths to restore your configuration.

## Useful skills on GitHub

A list of community skills you can install alongside the ones in this repo:

- **[Frontend Slides](https://github.com/zarazhangrui/frontend-slides)** — A Claude Code skill for creating stunning, animation-rich HTML presentations — from scratch or by converting PowerPoint files. It helps non-designers create beautiful web presentations without knowing CSS or JavaScript, using a "show, don't tell" approach: instead of asking you to describe your aesthetic preferences in words, it generates visual previews and lets you pick what you like.

## Files

### `settings/settings.json`

The global configuration file for Claude Code, corresponding to `~/.claude/settings.json`.

Contains permissions, tool preferences, and other personal settings. Copy it to take effect:

```bash
cp settings/settings.json ~/.claude/settings.json
```

### `skills/`

Custom skills for Claude Code, corresponding to `~/.claude/skills/`.

Each subdirectory is an independent skill with a `SKILL.md` file defining its trigger conditions and execution steps. Copy the folder to take effect:

```bash
cp -r skills/ ~/.claude/skills/
```
