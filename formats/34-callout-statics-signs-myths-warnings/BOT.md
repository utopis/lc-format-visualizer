# BOT.md · generate a "Call-out statics: '3 signs…', myth vs fact, 'don't buy this', warning"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 1 static 1080x1350 per variant (4 variants)), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@FedotOff90](https://x.com/FedotOff90/status/2096964245485449453) · A product callout static: the headline "See Clearly. Drive Safely. Instantly." over the ClearVision box, four benefit callouts with icons (Instant Clarity, Anti-Fog Protection, Water Repellent, Long-Lasting Effect) and a review bar ("4.8/5.0 based on 10,000+ reviews").

### Live paid ads in this format (7 in [adlibrary/](adlibrary/README.md), longest-running first)

- **Libby Babet: Women's-body myth-bust talking head (fitness coach)** (305 days live): Libby Babet (coach/founder) talking head at home: hook text 'This is why fasted workouts backfire for women' → explains cortisol/muscle → 'for my pro babes' → shows the empty wrapper of the collagen bar she ate this morning → 'go train strong, my ladies'. Burn
- **Pinch Magic Fiber: Product callout-label static ('This cleared my stuck poop')** (258 days live): Close-up of a scoop over the jar, black pill headline 'THIS CLEARED MY STUCK POOP' and 3 small callout labels pointing at the product (perfect poops / high-quality psyllium husk / tastes great).
- **Wellness Way UK: "Regain your confidence, without pills" device static (Wellness Way UK)** (252 days live): A hand holds a black device: "REGAIN YOUR CONFIDENCE, WITHOUT PILLS", "Harder, stronger erections in just 10 minutes", "50% OFF today" badge.
- **Aurivita Cayenne: "WARNING: Fake websites!" brand notice static (Aurivita)** (197 days live): A red "WARNING Fake websites!" banner with screenshots stamped "FAKE": "We are the original brand, and we don't sell on Amazon… if you see ads offering Auri Cayenne Pepper in huge discounts, do not place an order."
- **Smooche · Smooche: “DON'T TRY THIS COLOR CHANGING FOUNDATION UNLESS YOU WANT TO”** (10 days live): "DON'T TRY THIS COLOR CHANGING FOUNDATION UNLESS YOU WANT TO…" with a 3-tick list (look 10 years younger…).
- **Resilia · Vascular Wellness Report: “STOP THE LEAK. SUPPORT BLOOD FLOW”** (1 days live): "STOP THE LEAK. SUPPORT BLOOD FLOW." with a garlic pouch.

**Do not copy (seen in these live ads):** The "you're hosting parasites" style of reframe makes an unsupported health claim.

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| "3 signs" variant | Numbered list beside a close-up of a cheap chain | "3 signs your necklace is about to turn green: 1. It's light 2. It says 'gold tone' 3. It cost $9" |
| Myth vs fact | Two-column card, red X / gold tick | Myth: "You can't shower in gold jewellery." Fact: "You can in 14K PVD." |
| "Don't buy this" | Product photo with a sticker | "Don't buy this if you like taking your jewellery off." |
| Warning | Yellow warning bar at the top | "Warning: may cause you to never take it off." |
| Corner | Logo + offer | "Any 7 for $85" |

### Prompts

**Figma**

```
Template: headline 88px, list items 44px with gold number badges, product photo 50% width on the right; export 1080x1350.
```

**Claude**

```
Write 10 "3 signs" lists and 10 myth/fact pairs for [category], each true and checkable.
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
- [ ] Files named `F34-<concept>-<variant>`; tracking tag `utm_content=F34-<concept>-<variant>`.
- [ ] Avoid: Every "sign" and "fact" must be true.
- [ ] Avoid: Don't attack a named competitor.
- [ ] Avoid: The warning variant must be clearly playful, not a real warning.

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
5. Name every asset `F34-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F34
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

A plain, lo-fi static (or 15s text video) that calls out the viewer with a diagnostic list ("3 signs your necklace won't survive summer"), a myth-vs-fact pair, a cross-out ("~~gold-plated~~ PVD bonded"), or a negative/warning hook ("don't buy this if…"). Universal, undated, evergreen — the format that runs for years.

### Why it works

- Self-diagnosis hooks make the viewer check themselves against the list — high relevance with zero targeting.
- No dated references or offers → can run for 1,500+ days (@FedotOff90 PetJoy).
- Negative framing ("don't buy", "should be banned") outperforms in some accounts (@KanishDigital).
- Educates on the mechanism (PVD vs plating) which is LC's real differentiator.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| Static A | White bg, bold black text "3 signs your gold jewelry is plated (and will turn green)" + 3 numbered lines | Primary text: mechanism story → LC |
| Static B | Myth vs Fact two-column: "Myth: waterproof gold doesn't exist / Fact: 14K PVD is bonded at the molecular level" | — |
| Static C | Cross-out: "~~take off before showering~~" over LC necklace photo | — |
| Static D | Warning: "Don't buy this necklace if you like taking jewelry off" | Reverse-psychology primary text |

### Hooks

- "3 signs your necklace is about to turn green"
- "Myth: you can't shower in gold jewelry"
- "Don't buy this if you like taking your jewelry off"
- "Stop buying gold-plated jewelry (read this first)"
- "Warning: this stack is addictive"

### Production recipe

1. Pick 5 mechanism truths from the PDP (PVD bonding, 14K, waterproof, hypoallergenic if on PDP, warranty if any).
2. Write 4 template types × 5 truths = 20 statics; deliberately plain design (system font, white or kraft background).
3. Long primary text: personal story of the green-neck problem → mechanism → LC → offer.
4. No dates, no seasonal offers in evergreen versions; separate offer version for BFCM.

### Existing bot prompt

```
Using only these LC PDP facts {{PDP_FACTS}}, write: 5 "3 signs…" callouts, 5 myth-vs-fact pairs, 5 cross-out lines, 5 "don't buy this if…" warnings. ≤14 words on image. Then a 250-word first-person primary text for the 3 strongest. No claims about competitors by name; no medical claims.
```

### Variants to test

- Template type
- Plain vs branded design
- Positive vs negative framing
- Short vs 7,000-char primary text

## Reference examples

See [examples/README.md](examples/README.md) (13 posts). Top 5:

- @ads4apps (412L/930BM/27kV): 39 Meta formats that convert (930 bookmarks): X reasons, IG story, us vs them, Venn, don't buy this, iPhone notes, text message, low stock, we're sorry, breakin — https://x.com/ads4apps/status/2081785032679518490
- @FedotOff90 (110L/208BM/9kV): 37 formats printing (with days active): AI podcast 280d, report card, iPhone Notes, text on skin, Reddit, cross-out, fake PDP, tier list, myth vs fact, zero sta — https://x.com/FedotOff90/status/2104949773539442831
- @FedotOff90 (38L/33BM/4kV): PetJoy "three signs your dog has…" ad live 1,525 days: universal callout, free sample, no dated reference, lo-fi. — https://x.com/FedotOff90/status/2095601512592675094
- @FedotOff90 (17L/18BM/3kV): SafeRoad: 7,800-character confession (reading Amazon reviews at 1:23 AM) → comparison advertorial, 200 days live; port formats from outside your niche. — https://x.com/FedotOff90/status/2096964245485449453
- @KanishDigital (13L/13BM/824V): Negative hooks ("this product should be banned", "don't buy this…") — for one baby brand the best ad is a fully negative ad. — https://x.com/KanishDigital/status/2101549415467213023
