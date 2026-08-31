# Agent37 Creator Upload — AI Humanizer Pro (Onboarding Brief)

Prep'd for the 1-on-1 onboarding / "Book a call". Everything to fill the upload form is below.

## Metadata
- **Name:** AI Humanizer Pro
- **Skill slug:** `ai-humanizer-pro`
- **One-line pitch:** Paste AI slop, get back copy that sounds like a real person — in your brand's voice, with a measurable confidence score.
- **Category:** Creative / Writing
- **Tags:** writing, editing, humanize, anti-ai-slop, voice, brand-voice, marketing, copywriting

## Description (store listing)
> AI Humanizer Pro turns obvious AI-written text into natural, human copy. It detects 34 common AI-writing tells, rewrites them, and applies a chosen voice preset — sales, tech reviewer, casual blogger, corporate, academic, journalist, customer support, or social media. It also saves a reusable brand-voice profile so every run sounds like the same brand. Each run returns a confidence report: how AI the input was, how AI the output still is, and which voice was applied.

## Pricing suggestion
- **$6/mo** (benchmark: top Agent37 creator at 43 subs; aim mid-range for a skill that pays for itself with light usage). Adjust after 2 weeks of trial data.

## Free-trial config
- Free: first **10 messages** ("try before buy"). Then subscribe via Stripe to unlock full access.

## MCP servers / extras
- **None** — skill is self-contained, no API keys, no MCP servers, no external service.

## Hosting notes
- Runs under a **Hermes**-style agent reading `SKILL.md` (Claude/Anthropic-compatible skill format).
- No local runtime dependency, no docker needed by the user.
- Deterministic, safe: only text I/O, no network calls.

## Source repo
- https://github.com/sajibmiahdv99/AI-Humanizer-Pro (public) — `SKILL.md` (11.8 KB), `LICENSE` (MIT), `README.md`, `store-listing.md`.

## Legal / attribution
- MIT licensed. Original "Humanizer" patterns credit **Siqi Chen (@blader)** (https://github.com/blader/humanizer). Voice presets, brand-voice profile engine, and confidence report are original additions by **Sajib Miah**. Attribution preserved per MIT.
