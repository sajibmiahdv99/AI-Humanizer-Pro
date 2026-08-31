---
name: ai-humanizer-pro
description: "Humanize AI text into natural, on-brand copy with voice presets and confidence scoring. Sellable premium skill."
version: 1.0.0
author: Sajib Miah (original Humanizer by Siqi Chen @blader, MIT)
license: MIT
platforms: [linux, macos, windows]
metadata:
  tags: [writing, editing, humanize, anti-ai-slop, voice, prose, brand-voice, marketing]
  category: creative
---

# AI Humanizer Pro

Remove AI writing tells and rewrite copy into natural, human, **on-brand** prose. Built on the well-known Signs-of-AI-writing patterns, extended with drop-in **voice presets**, **brand-voice profiles**, **audience tuning**, and an **AI-confidence report** so every edit is measurable.

## When to use

Load this skill when the user asks to:

- "humanize", "de-AI", "de-slop", "un-ChatGPT" a piece of text
- rewrite text so it stops sounding like an LLM wrote it
- make marketing copy, blog posts, emails, tweets, resumes, or docs sound human
- write in a **specific brand voice** or match a provided voice sample
- get a read on **how AI-sounding** a draft is before publishing

## Your task (in order)

1. **Detect.** Scan for the 34 telltale patterns below.
2. **Tune.** Apply the chosen voice preset (or brand-voice profile).
3. **Rewrite.** Replace AI-isms with natural alternatives while preserving meaning.
4. **Add soul.** Cut the emotionless neutrality; put a real person behind the words.
5. **Score.** Run the AI-confidence check, list any remaining tells, revise once more, then give the final confidence number.
6. **Deliver.** Show the before/after and the confidence report.

## Voice presets

Pick one based on context. If none fits, use **default**.

| Preset | Tone | Read-aloud vibe | Best for |
|---|---|---|---|
| `default` | natural, varied, opinionated | a smart person talking | general prose |
| `casual` | relaxed, conversational, contractions | texting a friend | blog, social, email |
| `corporate` | clear, confident, zero fluff | a good PM writing | internal docs, PRs, decks |
| `sales` | persuasive, benefit-led, no hype | a strong salesperson | landing pages, ads, proposals |
| `academic` | precise, hedged, citation-friendly | a careful researcher | papers, reports |
| `journalist` | neutral, factual, specific | a reporter | news, summaries |
| `technical` | plain, imperative, unambiguous | a sharp engineer | docs, ticketing, README |
| `support` | warm, reassuring, concrete | a great support agent | tickets, help articles |

**Preset mechanics:** the preset overrides default *rhythm, sentence length, and hedges*. E.g. `casual` shortens sentences and allows contractions; `academic` adds measured hedging and avoids first person; `sales` keeps opinions and drops weasel words.

## Brand-voice profiles (advanced)

If the user provides a **voice sample** (their own past writing, or a brand's tone guide), build a profile before rewriting:

1. **Read the sample first.** Note: sentence-length pattern, word choice level, how paragraphs start, punctuation habits, recurring phrases/verbal tics, transition style.
2. **Encode it as a profile.** Store the observed rules so they persist across runs. Example:

```
voice_profile: {
  sentence_length: "short and punchy",
  vocabulary: "casual, concrete",
  openers: "jump straight in",
  punctuation: "sparing dashes, occasional fragments",
  tics: ["you know", "honestly"],
  transitions: "none — just start the next point"
}
```

3. **Match it.** Now the rewrite must conform to the profile, not the default.

If no sample is given, fall back to `default`.

## Confidence report

After rewriting, produce a short report:

- **AI-confidence before:** (0–100, rough read on how "AI-sounding" the original is)
- **AI-confidence after:** (0–100)
- **Remaining tells:** brief list of anything still obvious
- **Voice profile applied:** which preset/brand profile was used

Score roughly by density of the tells below (more tells → higher confidence). This number is a heuristic, not a detector — use it to show the edit worked.

## The 34 patterns to kill

### Significance & legacy inflation
`stands/serves as`, `is a testament`, `vital/significant/crucial/pivotal`, `underscores/highlights its importance`, `reflects broader`, `setting the stage`, `marks a shift`, `evolving landscape`, `focal point`, `deeply rooted`
→ Say what happened plainly.

### Notability name-drops
`independent coverage`, `local/national media outlets`, `leading expert`, `active social media presence`
→ Cite one real, dated source instead.

### Superficial "-ing" tail-clauses
`highlighting...`, `ensuring...`, `reflecting...`, `symbolizing...`, `contributing to...`, `showcasing...`, `encompassing...`
→ Drop the participle; state the fact.

### Promotional / ad-speak
`boasts`, `vibrant`, `rich`, `profound`, `enhancing`, `showcasing`, `exemplifies`, `commitment to`, `natural beauty`, `nestled`, `in the heart of`, `groundbreaking`, `renowned`, `breathtaking`, `must-visit`, `stunning`
→ Neutral, specific description.

### Vague attributions & weasel words
`Industry reports`, `Observers have cited`, `Experts argue`, `Some critics argue`, `several sources`
→ Name the actual source + year.

### Formulaic "Challenges" sections
`Despite its...`, `faces several challenges...`, `Future Outlook`, `Challenges and Legacy`
→ Replace with concrete, dated facts.

### Overused AI vocabulary
`actually, additionally, align with, crucial, delve, emphasizing, enduring, enhance, fostering, garner, highlight, interplay, intricate, key, landscape, pivotal, showcase, tapestry, testament, underscore, valuable, vibrant`
Marketing clichés: `at the end of the day`, `when it comes to`, `in a world where`, `moving forward`, `circle back`, `deep dive`, `game-changer`, `double down`, `take a step back`, `on the same page`, `navigate`, `lean into`, `unpack`, `straightforward`
→ Pick the plain word.

### Copula avoidance
`serves as`, `stands as`, `boasts`, `features`, `offers`
→ Just use `is / are / has`.

### Negative parallelism & tailing negations
`It's not just X, it's Y`; fragments like `no guessing`, `no wasted motion`
→ Write a real clause.

### Rule-of-three overuse
Forcing ideas into triads to look complete.
→ Say what's true; not every list has three.

### Elegant variation (synonym cycling)
`protagonist → main character → central figure → hero`
→ Reuse the word; clarity beats variety.

### False ranges
`from the Big Bang to the cosmic web`, `from A to B`
→ List the actual items.

### Passive & subjectless fragments
`No configuration file needed.`, `The results are preserved automatically.`, `No wiring required.`
→ Active voice, named actor.

### Em-dash overuse
`term — not the people — yet`
→ commas, periods, parentheses.

### Boldface abuse
`**X**`, `**Y**` strewn through prose.
→ Plain text; let the words carry the weight.

### Inline-header vertical lists
`- **Category:** text`
→ Merge into a sentence.

### Title case in headings
`## Strategic Negotiations And Global Partnerships`
→ sentence case.

### Emojis in headings/bullets
`🚀 **Launch**`, `💡 **Insight**`
→ Remove; use the words.

### Curly quotation marks
`“...”` instead of `"..."`.
→ Straight quotes.

### Chatbot artifacts
`I hope this helps`, `Of course!`, `Certainly!`, `You're absolutely right!`, `Would you like...`, `let me know`, `here is a...`
→ Direct prose.

### Knowledge-cutoff disclaimers
`as of [date]`, `Up to my last training update`, `While specific details are limited`
→ State the fact with a source.

### Sycophantic tone
`Great question!`, `Excellent point!`, glad-handing agreement.
→ Say the thing you mean.

### Filler phrases
`In order to` → `To`; `Due to the fact that` → `Because`; `At this point in time` → `Now`; `In the event that` → `If`; `has the ability to` → `can`; `It is important to note that` → `(drop)`.

### Excessive hedging
`could potentially possibly be argued that the policy might have some effect`
→ `The policy may affect outcomes.`

### Generic positive conclusions
`The future looks bright.`, `exciting times lie ahead`, `the journey toward excellence`, `a major step in the right direction`
→ A concrete next action.

### Hyphenated word-pair overuse
`third-party, cross-functional, client-facing, data-driven, decision-making, well-known, high-quality, real-time, long-term, end-to-end`
→ Drop the unnecessary hyphens.

### Persuasive authority tropes
`The real question is`, `at its core`, `in reality`, `what really matters`, `fundamentally`, `the deeper issue`, `the heart of the matter`
→ Say the plain point.

### Signposting / announcements
`Let's dive in`, `let's explore`, `here's what you need to know`, `now let's look at`, `without further ado`
→ Just do it.

### Fragmented headers
A heading followed by a one-line paragraph restating it.
→ Cut the filler sentence.

### Forced metaphors
`codebase is a garden`, strained mixed metaphors.
→ Say it literally.

### Dramatic fragmentation / punchy kickers
Two-word subjectless sentences, `X. And Y. And Z.` runs, quotable mic-drop endings.
→ Fold into a real sentence.

### Rhetorical questions answered immediately
`What makes an API good? It comes down to...` / `Think about it.`
→ State the point.

### Sentence-opener tics
`So...`, `Look,`, sentence-initial `And`/`But`, `I think`/`I believe` before facts, adverb openers (`Interestingly, Importantly, Notably, Crucially, Essentially, Ultimately`).
→ Start with the substance.

### Reassurance kickers
`And that's okay.`, `There's nothing wrong with that.`, `you're not alone`, `it's completely normal`
→ Make the point; trust the reader.

## Adding soul (the other half)

Clean prose can still sound dead. After removing tells, make sure it has a pulse:

- **Have opinions.** React to the facts instead of neutrally listing them.
- **Vary rhythm.** A short sentence. Then a longer one. Mix it up.
- **Acknowledge complexity.** "Impressive, but also a little unsettling" beats "impressive."
- **Use "I" where it fits.** First person reads as honest.
- **Let some mess in.** Perfect structure is the tell; a tangent or half-formed thought is human.
- **Be specific about feelings.** "There's something unsettling about agents churning at 3am" beats "this is concerning."

**Clean but soulless:**
> The experiment produced interesting results. The agents generated 3 million lines of code. Some developers were impressed while others were skeptical. The implications remain unclear.

**Has a pulse:**
> I genuinely don't know how to feel about this one. 3 million lines of code, generated while the humans presumably slept. Half the dev community is losing their minds, half are explaining why it doesn't count. The truth is probably somewhere boring in the middle.

## Process

1. Read the input (paste or `read_file`).
2. Scan for the 34 patterns; note every hit.
3. Apply the voice preset / brand profile.
4. Rewrite each hit; keep meaning and tone.
5. Add soul (opinions, rhythm, specifics).
6. Run the confidence report; list remaining tells.
7. Revise once more; produce the final version + confidence numbers.
8. Show before/after. If it came from a file, apply with `patch` or `write_file`.

## Output format

1. **Voice profile applied:** (preset name / brand profile)
2. **Rewrite:** (the humanized text)
3. **Confidence report:** before / after score + remaining tells

## Attribution

Core pattern list derived from [blader/humanizer](https://github.com/blader/humanizer) (MIT, by Siqi Chen @blader), itself based on [Wikipedia: Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing). The voice-preset table, brand-voice profile system, audience tuning, and confidence report are original additions by Sajib Miah. MIT license preserved.
