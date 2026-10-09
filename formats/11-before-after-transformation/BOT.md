# BOT.md · generate a "Before → After (static + video), incl. "Me before / me after" and Polaroid proof"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: Static 1080x1350 split, or 2 slides, or 8-15s jump-cut video), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@tryatria_AI](https://x.com/tryatria_AI/status/2092961578974896447) · Two images: a mirror-selfie before/after side by side with a caption, and a whiteboard diagram ("lose the weight, keep the glow") with a hand holding the pink product tub.
- Example: [@ZedNilm1](https://x.com/ZedNilm1/status/2027004587232657441) · $220k+ months don’t start with “design something creative” they start with proof people can understand in one second before → after same angle same li
- Example: [@Design__Lord](https://x.com/Design__Lord/status/2091625281077260728) · A static ad concept for this hydration skincare product. Clean visuals, product-focused composition, and a premium before → after concept designed to 
- Example: [@nicktheriot_](https://x.com/nicktheriot_/status/2027206415253684227) · This Brickell ad is a MASTERCLASS in removing every objection a guy has to trying skincare. And it’s, by far, one of the cleanest men's skincare stati
- Example: [@MatsMa68231](https://x.com/MatsMa68231/status/2099623924325658683) · Before → After. this skincare static ad to grab attention, communicate the value faster, and make the product harder to ignore. Stop posting ads that 
- Example: [@gresswoodhao](https://x.com/gresswoodhao/status/2064597459846987997) · AI-made this UGC skincare ad in ~30 min — looks hand-shot, not AI. Real-person feel, before/after proof, ready to A/B test. Run paid social for a skin
- Example: [@antonioventre_](https://x.com/antonioventre_/status/2078512377616589256) · Before/after photos are best native ad image: change creates curiosity; long copy tells story.

### Live paid ads in this format (5 in [adlibrary/](adlibrary/README.md), longest-running first)

- **Muscle Mat: "I transform your bed today" demo (Muscle Mat)** (819 days live): A man sits on a hard bed, rolls out the topper, sits again and smiles; end card "SALE ON NOW · swipe up to save". 27 s.
- **Deborah Hayes: "Spa treatments for belly fat don't work" two-layer explainer** (286 days live): "Spa treatments for belly fat don't work. And there's a scientific reason why… I did six spa sessions… $1,200… Your belly fat has two types of fat… these only work on surface fat." UGC plus a medical-paper insert plus CGI. 126 s.
- **Resilia · Resilia: Mirror-selfie before/after in gym wear** (1 days live): Mirror-selfie before/after in gym wear, with the pouch in the corner.
- **Resilia · Gut Health Insider: “Bye-bye bloat belly”**: "Bye-bye bloat belly": August / September / October line-drawn waists and the pouch.
- **Resilia · Resilia: “GIVE YOUR GUT SOME SUPPORT”**: "GIVE YOUR GUT SOME SUPPORT": before / 24 hours / 1 week / 4 weeks progression photos.

**Do not copy (seen in these live ads):** Weight-loss before/afters are restricted on Meta and these imply unsupported results.

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| Before (left / slide 1 / 0-3s) | The problem state shot in harsh, honest light: green ring mark, tarnished chain, broken clasp | Label: "Before: 3 weeks of gold-plated" (date or condition) |
| After (right / slide 2 / 3-8s) | Same angle, same framing, the product after the same use | Label: "After: 6 months of [product], showered daily" |
| Video transition | Jump cut on a hand clap / swipe | Caption carries the time gap |
| End | Product close-up | Offer |

### Prompts

**Shoot spec**

```
Tripod, same lens and distance for both shots, same daylight. Mark the spot on the table with tape. Shoot RAW, no beauty filter on the "after".
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
- [ ] Files named `F11-<concept>-<variant>`; tracking tag `utm_content=F11-<concept>-<variant>`.
- [ ] Avoid: Before/after must be real and of the same item/person; staged results are deceptive and get ads rejected.
- [ ] Avoid: Meta restricts before/after for health and weight claims; keep it about the product's condition, not body changes.
- [ ] Avoid: Different lighting between the two halves makes people assume a trick.

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
5. Name every asset `F11-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F11
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

Split image or 2-slide: left/first "before" (problem state), right/second "after" (result), with a date or condition label; video version = jump-cut transition. "People stop because they see a real change, not a product… then long primary text tells the story" ([@antonioventre_](https://x.com/antonioventre_/status/2078512377616589256)).

### Production recipe

Collect real wear-test photos from 10 customers/creators (send product, pay $50, 6-month check-in); meanwhile staff test. Metric: CTR, CPA; Omni.

## Reference examples

See [examples/README.md](examples/README.md) (12 posts). Top 5:

- @LachezarVoynov (396L/1453BM/88kV): 29 TOF video ad formats to test on Meta (transformation, Suno song, skit, beginner-intermediate-expert...). — https://x.com/LachezarVoynov/status/2086842038457098499
- @tryatria_AI (107L/147BM/6kV): Before->after ads printing; top 50 swipe (reply-bait for file). — https://x.com/tryatria_AI/status/2092961578974896447
- @antonioventre_ (79L/64BM/5kV): Before/after photos are best native ad image: change creates curiosity; long copy tells story. — https://x.com/antonioventre_/status/2078512377616589256
- @FedotOff90 (138L/247BM/16kV): Before and after format fucking prints. Nothing tells the story and shows the results of the product like before/ after image. Got a swipe file (freshly updated — https://x.com/FedotOff90/status/2085874661460713583
- @adamtaylorl (139L/203BM/13kV): Tier list of ecom formats: F = AI UGC, street interviews, read scripts; B = founder, testimonial compilations, listicle statics... — https://x.com/adamtaylorl/status/2097641383355879452
