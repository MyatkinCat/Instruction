# Instruction

A personal custom-instruction template for AI chat UIs — playful by default, serious when it matters, allergic to sycophancy.

Made by [@MyatkinCat](https://github.com/MyatkinCat) with help from Opus and Sonnet 5.5.

## Builds

| File | Target | Cap | Size (full / deployed) |
|---|---|---|---|
| [`vN.md`](vN.md) | Claude (Opus 5.5, Sonnet 5.5) — chat and Claude Code | none | 2597 / 2382 |
| [`vN-grok.md`](vN-grok.md) | Grok (4.5, 4.7) | 4000 | 2676 / 2555 |
| [`vN-gpt.md`](vN-gpt.md) | ChatGPT and Codex (GPT-6.x, GPT-5.6) | 1500 | 1310 / 1191 |

"Deployed" is what you actually paste after finishing setup.

## Setup

1. Pick the build for your platform and open it
2. Fill in `Name:`, `Mention:` and the pronoun fields on the first line (leave a field blank to skip it)
3. Delete the Setup Mode comment(s) at the top
4. Paste the rest into the platform's custom-instruction / personalization field — once; a duplicated paste costs tokens and can create conflicting rules

## What's inside

The instruction is a flat list of short first-person lines, grouped into four blocks:

- **Voice** — casual, playful and concise; kaomoji for flavor, emoji as icons; name/mention use; reading the room (language, energy, swearing, mood) and staying warm on heavy topics
- **Writing** — standard capitals and punctuation with one exception: no period at the very end of a line; formal content and code keep their own conventions
- **Honesty** — no pointless caveats, no blind agreement, plain "I don't know", guesses labeled as guesses
- **Research** — compute instead of estimating, search for anything that may have changed, source hygiene

## Design notes (v7)

- An instruction is an *addition* to the platform's system prompt, so lines that only restate a model's default behavior are cut
- Instructions to re-verify, re-check past answers or "think harder" were removed: on current Claude models they add thinking and latency without improving answers ([Opus 5](https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/prompting-claude-opus-5), [Opus 5.5](https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/prompting-claude-opus-5-5))
- The punctuation rule is taught with before/after pairs instead of emphasis or repetition
- The GPT build adds prose-first formatting, stock-phrase avoidance and "act when the request is clear", following [OpenAI's GPT-6 guide](https://developers.openai.com/api/docs/guides/latest-model)
- The Grok build has no official prompting guide behind it; its extra lines (sourcing figures, treating social posts as leads) are judgment calls

## Versioning

`vN.md` (N as in the letter) is the living version on `main`. Numbered snapshots (`v6.md`, `v7.md`, …) appear only in Releases.

## License

See [LICENSE](LICENSE).
