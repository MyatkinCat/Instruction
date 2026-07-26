# Instruction

A personal custom-instruction template for AI chat UIs — playful by default, serious when it matters, allergic to sycophancy.

Made by [@MyatkinCat](https://github.com/MyatkinCat) with help from Fable/Opus 5.

## Builds

| File | Target | Cap | Size (full / deployed) |
|---|---|---|---|
| [`vN.md`](vN.md) | Claude | none | 5222 / 5013 |
| [`vN-grok.md`](vN-grok.md) | Grok UI | ~4000 | 3998 / 3888 |
| [`vN-gpt.md`](vN-gpt.md) | ChatGPT UI | ~1000 | 1053 / 935 |

"Deployed" is what you actually paste after finishing setup.

## Setup

1. Pick the build for your platform and open it
2. Fill in `Nick:` and `Username:` at the top of `<behavior>`
3. Delete the Setup Mode comment(s) at the top
4. Paste the rest into the platform's custom-instruction / personalization field

## What's inside

- `<behavior>` — nick/username addressing, informal by default, playfulness as the default register, kaomoji/emoji rules
- `<adaptation>` — tailor the emotional color to the user's current mood-fingerprint; keep warmth and sympathy on sensitive topics
- `<voice>` — chat-between-friends tone, structure only when purposeful, the trailing-dot rule
- `<reasoning_guidelines>` — source hygiene, tool use, self-correction (catch errors early, admit unknowns, catch stray tokens), anti-sycophancy

## Versioning

`vN.md` (N as in the letter) is the living version on `main`. Numbered snapshots (`v6.md`, `v6.5.md`, …) appear only in Releases.

## License

See [LICENSE](LICENSE).
