# BOT.md · generate a "Comedy sketch with a full direct-response pitch hidden inside the joke"

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
5. Name every asset `F78-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F78
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

A 30-90s scripted comedy sketch (heist, courtroom, interrogation, office) in which every joke delivers a selling point: the mechanism, social proof, the offer, and the CTA ("click the button below"). Funny is the costume; direct response is the body.

### Why it works

- Entertainment earns watch time and shares, which buys cheaper CPMs.
- It doesn't feel like an ad until the punchline.
- It still sells, because every beat carries a claim.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0-5s | Night, two sisters in black, flashlights at a jewelry box | "Tonight we take the Herringbone." |
| 5-40s | Heist gags: "it's waterproof, we can escape through the pool" | proof joke with a real count |
| 40-60s | Caught by mom, who is wearing all 7 | "Any 7 for $85. Click below before she takes them all." |

### Hooks

- "Tonight… we steal the necklace"
- "The jewelry heist"
- "Courtroom: the necklace that wouldn't turn green"

### Production recipe

1. Write the sales beats first, then the jokes around them.
2. Hire local comedians or creators; one location.
3. Cut a 60s, a 30s and a 15s version.

### Existing bot prompt

```
Write 3 comedy sketches (60s) for LC where each joke carries one selling point: mechanism, proof ({{REAL_PROOF}}), offer, CTA. Mark which line does which job.
```

### Variants to test

- Sketch type
- Length

## Reference examples

See [examples/README.md](examples/README.md) (5 posts). Top 5:

- @briannjho (138L/338BM/10kV): Ad picks: Smooche AI song ad, Ryze AI skit, UndrDog big-enemy, Everyday Dose skit, Serene Herbs AI identity, Nuora apology mash-up, Mama Bear "this is what happ — https://x.com/briannjho/status/2094662259746480410
- @Daniloecom (4L/1BM/117V): What if an anti-snoring ad felt more like a ridiculous comedy sketch than an ad? So I made one. Claymation characters, absurd escalation, deadpan VO, and a fake — https://x.com/Daniloecom/status/2107749101823574297
- @imranullah (5L/1BM/12kV): The sad part is that this brand thought this was going to be a funny ad. I have pulled the calaway woods from my bag. #calawaygolf #goodgood https://t.co/aMWwQU — https://x.com/imranullah/status/2091907704734257203
- @Teavetua1971 (7L/0BM/10kV): QT With Your Funny Ad (Inspired by an old ad for a famous brand 😁😁) #digitalart #AIart️️️️️️️️️️️️️️️️️️️️️️️️️️️️️️️️️️️️️️️️️️️️️️️️️️️ https://t.co/WstSXVN5d — https://x.com/Teavetua1971/status/2104205130413273395
- @nedfulmer (3L/0BM/6kV): “Is influencer marketing dead?" While hiking through a medieval castle (lol, I know), I recently had a conversation with a founder who had shifted nearly all of — https://x.com/nedfulmer/status/2080780729852526953
