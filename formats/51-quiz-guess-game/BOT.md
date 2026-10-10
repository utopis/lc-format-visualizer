# BOT.md · generate a "Quiz / guess-the-price / street quiz game"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 30-60s, 1080x1920), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@LewisSylvi3994](https://x.com/LewisSylvi3994/status/2105450856086917518) · A guess-the-price game: a creator asks you to guess how much a necklace cost ("Everyone assumes it's fine jewelry"), shows the pieces close up, reveals "It's under $70 from XN Jewelry", then "Stop overpaying" and "Tap the link in bio!".
- Example: [@syinsyon](https://x.com/syinsyon/status/1979373551137489020) · Can you guess how much this gold jewelry?
- Example: [@SophieElodie](https://x.com/SophieElodie/status/2010785671498383613) · I just weighed the stainless steel jewelry I wear every day. Guess how much it weighs? 😏⛓️
- Example: [@big_damola](https://x.com/big_damola/status/1864240379110867128) · Guess the price of this jewelry 🌚

### Live paid ads in this format (1 in [adlibrary/](adlibrary/README.md), longest-running first)

- **Astrid Zeegen: 60-year-old founder quiz talking head (collagen)** (208 days live): A woman of 60 to camera: "Quick quiz. Do you know the difference between marine collagen and bovine collagen? …Does that help your skin, your joints or your gut?" 357 s (with a 392 s sibling).

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| 0-3s | Street: host stops a passer-by, holds up a stacked wrist | "Guess how much this whole stack cost." |
| 3-15s | Guesses: "$400?" "$250?" | Reactions on camera |
| 15-25s | Reveal | "Seven pieces. $85." |
| 25-40s | Passer-by puts it on | "Wait, and it's waterproof?" |
| End | Offer | - |

### Prompts

**Shoot**

```
Handheld mic with logo, two phones (wide + close), signed releases from everyone shown.
```

**Variant**

```
Weight version: "guess how much the stainless jewellery I wear every day weighs" (SophieElodie-style).
```

### QA checklist (all must pass before hand-off)

- [ ] Hook lands in the first 1.5 s (video) or is readable at thumbnail size (static / slide 1).
- [ ] Removal test: delete the product from the script. If it still makes sense, rewrite so the product is the payoff.
- [ ] Matches the reference structure (same beat order and length band) before any creative twist.
- [ ] Uses only real product imagery for the product; AI is for backgrounds, characters or b-roll, and is disclosed where required.
- [ ] Every claim is on the brand's approved-claims list (PDP); no invented stats, reviews, doctors or customers.
- [ ] Captions burned in and inside the safe zone; sound-off still understandable.
- [ ] One clear CTA that matches the landing page offer.
- [ ] Three hook variants delivered for the same body (test hooks, not whole new ads).
- [ ] Files named `F51-<concept>-<variant>`; tracking tag `utm_content=F51-<concept>-<variant>`.
- [ ] Avoid: Get releases from everyone on camera.
- [ ] Avoid: The reveal price must be the real price.
- [ ] Avoid: Don't fake guesses with actors without saying so.

<!-- QUICKSTART:END -->

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

See [examples/README.md](examples/README.md) (6 posts). Top 5:

- @nicktheriot_ (219L/348BM/12kV): 2026 FB creative styles tier list: S = long primary text + organic image, LTO, UGC, VSL, reaction, news; A = demo, us vs them, testimonial, close-up, founder st — https://x.com/nicktheriot_/status/2108173638033871013
- @MethodByVid (37L/67BM/4kV): 12 no-edit video formats: text story over gameplay, would-you-rather, guess-the-X quizzes, rankings, restoration, recipes from above. — https://x.com/MethodByVid/status/2087570057262256130
- @masterhooks_ (12L/13BM/1kV): 10 organic formats from a creator agency: storytelling, talking head, reaction, ranking, tier list, object lesson, play/pause reaction, AMA, comparison, before/ — https://x.com/masterhooks_/status/2100071930074390796
- @0xJeyx (15L/3BM/889V): Generate the same product as every format at once (street quiz, review, GRWM, DITL) and let the feed pick — example: "$50 street quiz" video. — https://x.com/0xJeyx/status/2063387846803673406
- @LewisSylvi3994 (0L/0BM/0V):  — https://x.com/LewisSylvi3994/status/2105450856086917518
