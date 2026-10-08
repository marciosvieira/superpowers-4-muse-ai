# Superpowers (lite, for Muse)

A stripped-down copy of [Superpowers](https://github.com/obra/superpowers) by Jesse Vincent (MIT license, see LICENSE). It keeps only the skills and what Muse needs to use them. No plugin install is required.

## Layout

- `skills/` holds the skills, including the helper scripts some of them call.
- `AGENTS.md` is the bootstrap. It replaces the session-start hook that the plugin normally uses, so Muse loads it from the project root.
- `LICENSE` is the original MIT license and copyright notice. Keep it.

## Use it

1. Put `skills/` and `AGENTS.md` in the root of the project you are working on (or clone this repo as the project).
2. Start a fresh Muse session and send: `Let's make a react todo list`
3. If the brainstorming skill starts before any code is written, the bootstrap is working.

## Update the skills from upstream

```
git remote add upstream https://github.com/obra/superpowers
git fetch upstream
git checkout upstream/main -- skills/
```

This can bring back files removed from this copy. Re-apply the trims afterward. If `skills/using-superpowers/SKILL.md` changed, rebuild `AGENTS.md` by keeping its header and replacing everything after it with the new skill text from line 6 onward.
