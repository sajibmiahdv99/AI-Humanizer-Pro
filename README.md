# AI Humanizer Pro

Humanize AI text into natural, on-brand copy with voice presets and a confidence score.

## What it does

Paste in AI-slop ("In today's rapidly evolving landscape, our revolutionary platform...")
and get back copy that reads like a real person — with a confidence report showing
how "AI" the output still sounds, and a chosen brand-voice applied.

- Detects 34 common AI-writing tells and rewrites them away.
- Applies a **voice preset** (sales, tech reviewer, casual blogger, corporate, academic,
  journalist, customer support, social media) so output matches your brand.
- Returns a **confidence report**: before/after AI-score, remaining tells, voice applied.
- Saves a **brand-voice profile** for consistent tone across every run.

## Usage

Drop the `SKILL.md` folder into your skills directory (e.g. `~/.hermes/skills/`),
or run with any Claude/Anthropic-style agent that reads SKILL.md.

```
skill: ai-humanizer-pro
prompt: "Humanize this, voice preset=sales"
```

## Voice presets

| Preset           | Feel                                                        |
|------------------|-------------------------------------------------------------|
| `sales`          | Persuasive, benefit-led, no hype                            |
| `tech-reviewer`  | Precise, skeptical, detail-forward                          |
| `casual-blogger`| Warm, conversational, relaxed                               |
| `corporate`      | Polished, neutral, confident                                |
| `academic`       | Formal, measured, hedged                                    |
| `journalist`     | Fact-first, neutral, readable                               |
| `support`        | Empathetic, clear, action-oriented                          |
| `social`         | Punchy, engaged, short                                      |

## Example

**Input:** AI-sloppy corporate pitch.

**Output (voice `sales`):** "Our platform replaces the status quo of work. You plan, it runs.
Real examples: a support lead who closed 40% more tickets without adding headcount, an
operations guy who stopped chasing spreadsheets at 9pm. Book a 20-minute walkthrough and
bring one task you hate doing."

**Confidence report:** before ~82/100 → after ~12/100.

## License

MIT. Original "Humanizer" patterns by Siqi Chen (@blader) —
https://github.com/blader/humanizer. Voice presets, brand-voice profile engine, and the
confidence-report flow are original additions.
