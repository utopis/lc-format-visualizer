# BOT.md · generate a "Comedy sketch with a full direct-response pitch hidden inside the joke"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 30-90s, 1080x1920), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@Daniloecom](https://x.com/Daniloecom/status/2107749101823574297) · A claymation-style comedy sketch about snoring: a man snoring with sound waves, his wife suffering, a cop bursting in, a giant cartoon mouth, then the product (QuietSeal) on the nightstand.
- Example: [@Teavetua1971](https://x.com/Teavetua1971/status/2104205130413273395) · QT With Your Funny Ad (Inspired by an old ad for a famous brand 😁😁) #digitalart #AIart️️️️️️️️️️️️️️️️️️️️️️️️️️️️️️️️️️️️️️️️️️️️️️️️️️️ https://t.co
- Example: [@nedfulmer](https://x.com/nedfulmer/status/2080780729852526953) · “Is influencer marketing dead?" While hiking through a medieval castle (lol, I know), I recently had a conversation with a founder who had shifted nea
- Example: [@imranullah](https://x.com/imranullah/status/2091907704734257203) · The sad part is that this brand thought this was going to be a funny ad. I have pulled the calaway woods from my bag. #calawaygolf #goodgood https://t

### Live paid ads in this format (4 in [adlibrary/](adlibrary/README.md), longest-running first)

- **Smooche · Smooche: “I'm about to walk into brunch to meet my girlfriend that I was with to…”** (41 days live): Opens: “I'm about to walk into brunch to meet my girlfriend that I was with to figure out who tried to draw a ying yang on my forehead and guess what? I just saw my ex- boyfriend of 15 years and it's perfect…”
- **Smooche · Smooche: “Let's go. Whoa! Well, what?…”** (10 days live): Opens: “Let's go. Whoa!”
- **Smooche · Smooche: “Okay, Richard say it's one more time. Well, I'm married to you because…”** (6 days live): Opens: “Okay, Richard say it's one more time. Well, I'm married to you because I thought you were going to be hot forever.”
- **Resilia · Vascular Wellness Report: “So my 473 year old husband was bricked up at the dinner. So I'll change…”** (1 days live): Opens: “So my 473 year old husband was bricked up at the dinner. So I'll change my man's life.”

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| 0-5s | Absurd setup: a courtroom, a heist, an interrogation | "Ma'am, you're charged with showering in your jewelry." |
| 5-25s | Joke 1 delivers the mechanism | "It's 14K PVD, your honour. It's bonded." |
| 25-45s | Joke 2 delivers social proof | "We have 40,000 witnesses." (real review count) |
| 45-60s | Joke 3 delivers the offer | "Any 7 for $85? Case dismissed." |
| End | Product + CTA | - |

### Prompts

**Claude**

```
Write a 60-second comedy sketch in [setting]. Each joke must carry one selling point in this order: mechanism, proof, offer, CTA. Max 3 characters.
```

**AI version (Veo 3 / Kling claymation)**

```
claymation courtroom, a judge and a woman wearing a gold necklace, comedic, lip-sync "[line]", 8s, 9:16
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
- [ ] Files named `F78-<concept>-<variant>`; tracking tag `utm_content=F78-<concept>-<variant>`.
- [ ] Avoid: A joke that does not sell is expensive airtime; cut it.
- [ ] Avoid: Numbers in jokes (review counts, prices) must be real.

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
