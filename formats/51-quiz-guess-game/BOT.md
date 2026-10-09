# BOT.md · generate a "Quiz / guess-the-price / street quiz game"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

## Inputs you need

- `BRAND`: name, product, price, offer, audience, 3-5 proof points, claims you may NOT make
- `REVIEWS`: 20+ customer reviews or comments (voice of customer)
- `ASSETS`: real product photos / video, logo, fonts, colors
- `CHANNEL`: organic (TikTok/IG/Shorts) or paid (Meta/TikTok/YouTube)

## Steps

1. Read **Format DNA** below and 3-5 files in `examples/` (prefer `curated`). Note the hook, the beat structure and the length.
2. Mine `REVIEWS` for the 3 strongest angles (problem, desire, objection) in the customer's words.
3. Write 3 concepts. For each: title, angle, hook (first line / first 2 seconds), full script or slide-by-slide copy, shot list or layout, on-screen text, CTA, caption.
4. Follow the **Production recipe** below for tools and prompts. Use real product imagery for the product itself; never invent product features or results.
5. Name every asset `F51-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F51
concept: <short name>
angle: <problem | desire | objection>
hook: "<first line / first 2s>"
beats:
  - t: "0-2s"
    visual: "..."
    text: "..."
    audio: "..."
caption: "..."
cta: "..."
production: {tools: [...], prompts: [...], est_cost: "...", est_time: "..."}
test: {channel: "...", budget: "...", success_metric: "..."}
```

## Guardrails

- No fake reviews, fake customers, undisclosed AI people presented as real customers, or invented stats. Disclose AI where the platform requires it.
- Follow `../_COMPLIANCE.md` and the brand's claim rules.

## Format DNA (from the playbook)

### What it is

Viewer or passerby is quizzed: "solid gold or $12 a piece?", "guess the price of this 7-piece stack". Participation hook; answer reveal = offer.

### Why it works

- Interactive; comments with guesses boost reach.
- Reveal of low price = value shock.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0-2s | Two necklaces | "One is $900 solid gold. One is from a $85 stack. Guess." |
| 2-10s | Close-ups | Countdown |
| 10-15s | Reveal | "any 7 for $85" |

### Hooks

- "Real gold or $85? Guess"
- "Guess the price of this stack"

### Production recipe

1. Use honest comparisons; no "can't tell the difference" claims unless tested.

### Existing bot prompt

```
Write 8 quiz scripts for LC; reveals must be factual.
```

### Variants to test

- Street vs studio

## Reference examples

See [examples/README.md](examples/README.md) (5 posts). Top 5:

- @nicktheriot_ (219L/348BM/12kV): 2026 FB creative styles tier list: S = long primary text + organic image, LTO, UGC, VSL, reaction, news; A = demo, us vs them, testimonial, close-up, founder st — https://x.com/nicktheriot_/status/2108173638033871013
- @MethodByVid (37L/67BM/4kV): 12 no-edit video formats: text story over gameplay, would-you-rather, guess-the-X quizzes, rankings, restoration, recipes from above. — https://x.com/MethodByVid/status/2087570057262256130
- @masterhooks_ (12L/13BM/1kV): 10 organic formats from a creator agency: storytelling, talking head, reaction, ranking, tier list, object lesson, play/pause reaction, AMA, comparison, before/ — https://x.com/masterhooks_/status/2100071930074390796
- @0xJeyx (15L/3BM/889V): Generate the same product as every format at once (street quiz, review, GRWM, DITL) and let the feed pick — example: "$50 street quiz" video. — https://x.com/0xJeyx/status/2063387846803673406
- @LewisSylvi3994 (0L/0BM/0V):  — https://x.com/LewisSylvi3994/status/2105450856086917518
