# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repo is

Markdown-only repo with no code, package manifest, test suite, or build step. It holds personal custom-instruction templates for AI chat UIs. The user pastes a build into a platform's custom-instruction field, so the files are prompt text, not documentation.

## Commands

There are no build, lint, or test commands. Verification is manual:

- Character count (the README size column counts characters, not bytes): `LC_ALL=C.UTF-8 wc -m vN.md`
- Behavior check: paste the build into a fresh chat and see how it replies. Only the user can do this, since it needs a live chat UI.

## Layout and how the builds relate

- `vN.md` is the living Claude build (Opus 5.5, Sonnet 5.5) and the source of truth. It has no character cap.
- `vN-grok.md` (4000 cap) and `vN-gpt.md` (1500 cap) are platform-specific rewrites of the same rules. Keep their line structure and voice rules in step with `vN.md`.
- `README.md` holds the build table with "full" and "deployed" sizes, the setup steps, and design notes.
- Every build starts with a setup comment that the user deletes, and a `Name: | Handle: @ | ...` line the user fills in. Keep both.

When a voice or writing rule changes, apply it to all three builds. The most recent commit (`bbd00ea`) did this for the kaomoji-to-emoji swap.

## Editing rules that come from the README's design notes

- The instruction is appended to each platform's own system prompt. Don't add lines that only restate default model behavior.
- Don't add "re-verify" or "think harder" instructions. The README says these add latency without improving answers.
- Keep the punctuation rule (no period at the very end of a line) taught with before/after pairs, not emphasis.

## Size table

After changing a build, recount it and update the README table's "full" column to match the character count. The "deployed" column reflects the text after setup fields are filled in, so it can't be recomputed from the repo alone. Leave it alone unless the user gives you a new value.

## Versioning

`vN.md` on `main` is the living version. Numbered snapshots (`v6.md`, `v7.md`, ...) belong in GitHub Releases, not in the tree.
