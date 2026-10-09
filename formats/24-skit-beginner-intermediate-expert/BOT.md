# BOT.md · generate a "Skit + "Beginner / Intermediate / Expert" tiers"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 20-45s, 1080x1920), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@TheKhushLife](https://x.com/TheKhushLife/status/2079287229164442041) · A skit where one creator plays several levels of the same person (beginner, intermediate, expert) in different outfits and locations: outside a house, in sunglasses, in a car, at a desk. It ends on the app screen ("Real locals. Reviewed and verified.").

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| 0-2s | Title card over the creator: "Beginner vs Intermediate vs Expert: wearing gold" | - |
| Beginner (2-10s) | Creator in outfit A takes jewelry off for everything, loses an earring | Self-deprecating line |
| Intermediate (10-20s) | Outfit B, keeps a jewelry dish by the sink, still forgets | Slightly smarter line |
| Expert (20-35s) | Outfit C, showers and swims wearing the product | "Expert: never takes it off" + product name |
| End | Product close-up | Offer |

### Prompts

**Script (Claude)**

```
Write a 30-second beginner/intermediate/expert skit about [task]. Each tier: one costume change, one visual gag, one line. Product appears only at expert level.
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
- [ ] Files named `F24-<concept>-<variant>`; tracking tag `utm_content=F24-<concept>-<variant>`.
- [ ] Avoid: Costume changes sell the tiers; a hat or glasses is enough.
- [ ] Avoid: Keep each tier under 10s.

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
5. Name every asset `F24-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F24
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

Skit: 2-character comedic scene with a relatable problem; B-I-E: same task done at 3 skill levels, product at "expert".

## Reference examples

See [examples/README.md](examples/README.md) (5 posts). Top 5:

- @LachezarVoynov (396L/1453BM/88kV): 29 TOF video ad formats to test on Meta (transformation, Suno song, skit, beginner-intermediate-expert...). — https://x.com/LachezarVoynov/status/2086842038457098499
- @lorenzo_pravata (150L/196BM/10kV): "Ads that don't look like ads": podcast clips, street interviews, skits with studio actors; pet brand $29K→$150K/mo spend in 60 days, CPA $188→$124. — https://x.com/lorenzo_pravata/status/2104536224488738839
- @LachezarVoynov (86L/102BM/10kV): $300k/mo strategy: wrappers that became top spenders = skits, carpool ads, Suno songs, AI Pixar-character podcasts; hooks must target different people. — https://x.com/LachezarVoynov/status/2097351286094021034
- @TheKhushLife (10L/0BM/467V): #ugcexample 13/30 Lately I've been doing a lot more skit ADs &amp; SUPER excited to film one at the grocery store this week!🛒 Throwback to a Karrot AD I did, 5M — https://x.com/TheKhushLife/status/2079287229164442041
- @briannjho (138L/338BM/10kV): Ad picks: Smooche AI song ad, Ryze AI skit, UndrDog big-enemy, Everyday Dose skit, Serene Herbs AI identity, Nuora apology mash-up, Mama Bear "this is what happ — https://x.com/briannjho/status/2094662259746480410
