# BOT.md · generate a "Hyper-real first-person POV footage"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 8-30s, 1080x1920, first-person), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@spwfeijen](https://x.com/spwfeijen/status/2105648964716380197) · A hyper-real first-person POV clip: the camera is the viewer's eyes, standing on a ship's deck looking out over the sea, with no cuts away from the POV.
- Example: [@LordofAds](https://x.com/LordofAds/status/1905654783823782374) · 🛡️Creative #1: First Person POV Example An influencer takes the audience through her makeup routine using OGEE contour products. The ad-libs and comme
- Example: [@DeQueenofSpaces](https://x.com/DeQueenofSpaces/status/2100177884975612016) · First-person POV vs Third-person POV. Welcome back to this week's AI Creation Lab, where we're exploring Point of View. For this experiment, I created
- Example: [@MarketingE80034](https://x.com/MarketingE80034/status/2101990359379099861) · One product photo. One prompt. A cinematic POV ad in seconds 🎬 No camera, no studio, no models. Here's the exact AI workflow 👇 #AIVideo #AIMarketing #

### Live paid ads in this format (1 in [adlibrary/](adlibrary/README.md), longest-running first)

- **Skincare Tips: Mundane car-door POV (Skincare Tips)** (290 days live): A POV of legs in denim shorts getting into a car, holding keys. Nothing explained; the copy does the selling.

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| 0-3s | Camera at eye level as the viewer's eyes; hands wearing the product enter frame | Tension caption: "will it survive a week on a boat?" |
| 3-20s | Real actions: diving, showering, lifting, cooking. No cutaways to a presenter | Minimal text, ambient sound |
| 20-end | Hands in close-up, product unchanged | "day 7." + brand |

### Prompts

**Real shoot**

```
Chest or head mount (GoPro/Insta360 or iPhone on a chest rig), 4K 60fps, horizon lock on.
```

**AI (Veo 3 / Kling)**

```
first-person POV footage, the viewer's own hands with a thin gold bracelet reaching into the sea from a boat deck, sunlight, realistic, slight motion, 6s, 9:16
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
- [ ] Files named `F23-<concept>-<variant>`; tracking tag `utm_content=F23-<concept>-<variant>`.
- [ ] Avoid: AI POV must not show the product doing things it cannot; real footage for proof claims.
- [ ] Avoid: Fast POV motion causes nausea; stabilise.

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
5. Name every asset `F23-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F23
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

Camera = viewer's eyes; hands wearing the product doing real things; a narrative tension (will it survive?).

### Production recipe

Real GoPro/phone chest-mount (preferred) — AI only for impossible shots, labelled.

## Reference examples

See [examples/README.md](examples/README.md) (3 posts). Top 5:

- @spwfeijen (46L/49BM/5kV): Hyper-real first-person POV footage with narrative tension keeps watch time near 100%. — https://x.com/spwfeijen/status/2105648964716380197
- @antonioventre_ (8L/4BM/693V): Production rule: reaction can't be scripted — founder-customer call + POV reaction ads with live unscripted reaction. — https://x.com/antonioventre_/status/2091895054755373116
- @DeQueenofSpaces (100L/2BM/2kV): First-person POV vs Third-person POV. Welcome back to this week's AI Creation Lab, where we're exploring Point of View. For this experiment, I created a fitness — https://x.com/DeQueenofSpaces/status/2100177884975612016
