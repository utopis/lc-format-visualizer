# BOT.md · generate a "Offer-architecture ads: build-your-own bundle / any-N picker / mystery box / free-plus-shipping"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: Static 1080x1350 + a 15-20s screen-record video), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@mattepstein](https://x.com/mattepstein/status/1840692048787042431) · A UGC ad that sends people straight to a build-your-own-bundle page: it opens on the store's 'massive BOGO sale' bundle page, then a creator shows the sunscreen products on her skin and around the house, ending on a stack of products and "Click below to BOGO".
- Example: [@andrewdilullo](https://x.com/andrewdilullo/status/1891876658027823589) · New offer → Build your own bundle. Instead of a single product, we introduced a “Buy More, Save More” option. Customers could mix and match flavors, c
- Example: [@CORSETDEAL](https://x.com/CORSETDEAL/status/1870738559134581077) · ✨ Big Savings Alert! ✨ 🔥 Bundle & Save: Pick any 3 for $99 – Style, comfort, and elegance in one irresistible offer! 🔥 Flat 40% OFF: Treat yourself to
- Example: [@FedotOff90](https://x.com/FedotOff90/status/2094854572623675832) · 6 lander/advertorial types (news mimic, story, listicle, quiz, authority, comparison) — 53-format lander database.
- Example: [@ArijanJanes](https://x.com/ArijanJanes/status/2098456656711467183) · We changed our offer and got a $20 better AOV with roughly the same CVR... All while sending LESS items to the customer. Version 1: - Highest AOV opti

### Live paid ads in this format (4 in [adlibrary/](adlibrary/README.md), longest-running first)

- **Resilia · Metabolic Health Review: “3 FOR ONLY $20. SALE ENDS TONIGHT!”** (1 days live): "3 FOR ONLY $20. SALE ENDS TONIGHT!" with three cinnamon pouches on black.
- **Resilia · Resilia: “BUY 2 GET 1 FREE. YOUR BLOAT IS GONE IN 14 DAYS OR YOUR MONEY BACK”** (1 days live): "BUY 2 GET 1 FREE. YOUR BLOAT IS GONE IN 14 DAYS OR YOUR MONEY BACK."
- **Resilia · Vascular Wellness Report: “BUY 2 GET 1 FREE, 70% OFF”** (1 days live): "BUY 2 GET 1 FREE, 70% OFF" with three pouches on a kitchen counter.
- **Resilia · Resilia: A hand placing the pouch on a counter** (1 days live): A hand placing the pouch on a counter with a "3 for only $20" roundel.

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| 0-3s | Screen recording of the bundle picker on the site, finger taps products | Text: "Pick any 7. Pay $85." |
| 3-10s | Counter climbs: 3/7, 5/7, 7/7, price stays $85 | VO: "Mix necklaces, rings, earrings. Doesn't matter." |
| 10-15s | Cut to the 7 pieces arriving in a box, then worn stacked | "That's about $12 a piece." |
| Static version | A 3x3 grid of products with 7 ticked, a price bar at the bottom | "7 for $85 — you pick" |
| Mystery-box variant | Closed gift box, then a quick reveal | "Can't decide? Let us pick." |

### Prompts

**Figma (static)**

```
Grid of 9 products on cream, 7 with gold tick badges, a bottom bar "7/7 · $85 · Free shipping", headline 96px
```

**Screen record**

```
iPhone screen record of the real picker, 60fps, then crop to 9:16 and add taps with a touch indicator
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
- [ ] Files named `F86-<concept>-<variant>`; tracking tag `utm_content=F86-<concept>-<variant>`.
- [ ] Avoid: The ad must match the real checkout exactly (price, number of items, shipping).
- [ ] Avoid: Show the per-piece maths only if it is accurate.
- [ ] Avoid: Mystery boxes need a clear value floor; don't imply rare items you won't send.

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
5. Name every asset `F86-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F86
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

Ads whose creative is the offer mechanic itself: a picker grid "choose any 7" with a running counter, a mystery-box reveal, "free chain, just pay shipping" for first orders, or tiered "buy 4 get 20%". The landing page is the matching picker or offer page, not a generic PDP.

### Why it works

- The mechanic is the hook: choosing feels like play, and the flat price removes math.
- Offer-forward creative converts warm and product-aware traffic.
- A matching picker lander keeps the promise from the ad.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0-3s | Screen recording: tapping 7 pieces into a bundle builder, counter 1/7 → 7/7 | "Any 7. $85. Go." |
| 3-12s | Pieces dropping into a gift box | — |
| 12-15s | Price card | "Waterproof 14K PVD" |

### Hooks

- "Pick any 7. $85. That's it."
- "Build your stack in 20 seconds"
- "Mystery 3-piece box: guess what's inside"
- "First chain free, just pay shipping" (test only if margins allow)

### Production recipe

1. Record the real picker flow on louisecarter.com (or build one).
2. Make 3 mechanics: picker, mystery box, gift-box build.
3. Send each to the matching page with the bundle preloaded.

### Existing bot prompt

```
Write 5 offer-architecture ads for LC: picker screen-record script, mystery box reveal, gift-box build, "your stack, your rules" static, tiered offer static. Match each to a landing-page spec (preloaded cart or picker).
```

### Variants to test

- Mechanic
- Cold vs retargeting

## Reference examples

See [examples/README.md](examples/README.md) (8 posts). Top 5:

- @FedotOff90 (238L/632BM/20kV): 7,500+ winning Meta ads sorted by format across public boards (top-50 DTC, beauty, natives, listicles, shock & gross, BOFU). — https://x.com/FedotOff90/status/2093350155751924213
- @FedotOff90 (175L/385BM/47kV): 6 lander/advertorial types (news mimic, story, listicle, quiz, authority, comparison) — 53-format lander database. — https://x.com/FedotOff90/status/2094854572623675832
- @FedotOff90 (145L/318BM/11kV): 24 landing page formats with live ad→lander pairs (breaking news, investigation, as-seen-on-TV, doctor warning…). — https://x.com/FedotOff90/status/2092382176738202057
- @FedotOff90 (110L/208BM/9kV): 37 formats printing (with days active): AI podcast 280d, report card, iPhone Notes, text on skin, Reddit, cross-out, fake PDP, tier list, myth vs fact, zero sta — https://x.com/FedotOff90/status/2104949773539442831
- @tryatria_AI (63L/103BM/6kV): Resilia: 4,790 of 5,449 ads to same page; 2nd bag $20 + free jar (offer architecture). — https://x.com/tryatria_AI/status/2107919598917923125
