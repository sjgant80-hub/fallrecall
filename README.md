# fallrecall

> **Take your AI memory back.** A sovereign single-HTML PWA for liberating your AI history from the frontier labs. Import → analyse → generate portable system prompts → paste anywhere.

**Live:** https://sjgant80-hub.github.io/fallrecall/

## The lock-in problem

Frontier labs (OpenAI, Anthropic, Google) keep your chat history, memory, custom instructions, and the model's behavioural fine-tuning on **their** servers. Switching means starting over. The lock-in is real — and increasingly the moat.

## What this does

1. **Import** — ChatGPT (`conversations.json` data export), Claude (data export JSON), Gemini (Google Takeout activity), or generic paste with role markers
2. **Library** — browse every imported conversation, locally, on your device
3. **Analyse** — run cascade analysis (WebLLM / ollama / Llama 3.3 / Gemini Flash / Claude Sonnet) to extract your **flavour**:
   - Voice notes (how you write)
   - Recurring interests
   - Preferences (what you want)
   - Anti-preferences (what you bristle at)
   - Open questions you keep returning to
   - Decision style
4. **Portable prompts** — generate copy-paste system prompts in four formats:
   - System prompt · long (~500-800 words for custom GPTs, Claude projects, ollama system messages)
   - System prompt · short (~150-200 words for fast paste)
   - Voice notes (pure bullets)
   - Anti-preferences only (what NOT to do — pair with any other prompt)
5. **Replay** — re-send any conversation through your sovereign cascade to validate the flavour survives migration
6. **Mesh** — exposes your flavour profile to other FallSeeds (fallseed-agents, fallseed-creator-os) via the cross-seed `fall-signal` protocol

## Architecture invariants

- One HTML file · IDB primary · BroadcastChannel mesh (`fall-recall` + `fall-signal`)
- P3 audit chain (prevHash + SHA-256) on every state mutation
- 8-provider LLM cascade with streaming · sovereign-first priority
- Cross-seed request/response protocol (`introspect` · `records-export` · `flavour-summary`)
- No telemetry, no analytics, no remote state

## Sovereignty in practice

If you enable WebLLM (in-browser) or ollama (local), your conversations **never leave your device**, even during analysis. The cascade tries local providers first. Cloud is fallback, not default.

## Cosmology

Prime **1231**, spine-clean mod 127 = 88 = 2³·11. Category **sovereignty**. Mesh channel **`fall-recall`**. Seal **◊·κ=1**.

Part of the FallSeed family — see [the spec](https://www.ai-nativesolutions.com/spec.html).

## Licence

MIT © Simon Gant.
