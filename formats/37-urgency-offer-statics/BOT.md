# BOT.md · generate a "Urgency/offer statics: low stock, back in stock, limited-time offer, BFCM"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 1 static 1080x1350 per offer type), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@johntech778](https://x.com/johntech778/status/2106885699374829636) · A product page shot as an offer static: a dog holding a treat bag, a countdown timer at the top, and a bundle picker (Single Pack, Buy 2 Get 1 Free and so on) with ratings and trust badges. The offer, not the product, is the hero.
- Example: [@johntech778](https://x.com/johntech778/status/2102744531489751066) · "6,200+ Bottles Sold This Month" is the most under-used line on any product page. Here's how I structured a Goli Ashwagandha buy box around it 10 conv
- Example: [@usmanstrategist](https://x.com/usmanstrategist/status/2087306011849965645) · Here's a breakdown of the three funnel stages and the best creative formats for each, so you can drive more purchases and scale your brand more profit
- Example: [@kylaugccreator](https://x.com/kylaugccreator/status/2096744141031981406) · Here’s an ugc example I created for Bucketlisters Nashville app The goal was to showcase a limited-time 90s throwback bar while positioning Bucketlist
- Example: [@hey_ankita](https://x.com/hey_ankita/status/2102704237805547557) · 90% OFF Seedance 2.5 on Pippit AI, now only $1.5/month for a limited time. Pippit AI is giving creators access to the official, native Seedance 2.5 mo
- Example: [@johntech778](https://x.com/johntech778/status/2101658718647521629) · Buy 1 Get 1 Free" is the most under-used conversion lever in supplement DTC. Here's how I structured a product page around it. 8 conversion decisions 
- Example: [@jackolivieri_](https://x.com/jackolivieri_/status/2097798592010547583) · Smooche static "847 Orders in Last Hour, Almost Gone" / "LIVE UPDATE" stock copy (GetHookd share).
- Example: [@aditiasiswara](https://x.com/aditiasiswara/status/2105304476890648987) · Get the official, native Seedance 2.5 for as low as $1.50 for your first month with a Limited-Time 90% OFF offer! Seedance 2.5 at 720P starts at just 

### Live paid ads in this format (11 in [adlibrary/](adlibrary/README.md), longest-running first)

- **Solvaderm Skin Care: Clean product-on-podium static (Solvaderm, "Unlock your best skin yet")** (690 days live): A pastel 3D podium, a tall serum bottle, the headline "Unlock Your Best Skin Yet!" and a sub-line. DCO.
- **Muscle Mat: "FREE" baby-on-topper static (Muscle Mat)** (533 days live): A baby asleep on the topper with a "FREE" banner and a gift offer.
- **Phantom Athletics: Catalog DCO grid with big % badge (German)** (445 days live): Dynamic-creative carousel: hero model holding the bag, three product variants stacked left, red 'JETZT -42%' badge, Trustpilot-style 4.75 rating strip.
- **BioRoot Labs: "A message from our founder" scarcity text static** (378 days live): A white text static: "A MESSAGE FROM OUR FOUNDER 💔 We never expected this. Thousands of people are turning to BioRoot Labs' Doctor-Formulated Turmeric daily, and our limited Buy Two, Get One Free offer is about to expire… our stock is dangerously low… Sale end
- **Shopmenvault: "BUY 2, GET 2 FREE – We won't do this again" offer static** (251 days live): A black static: "BUY 2, GET 2 FREE", "WE WON'T DO THIS AGAIN", 3 boxer briefs, "50% OFF deals", "Trusted by 10,000+ men after prostate surgery".
- **Smooche · Smooche: “IT'S OFFICIAL: WE'RE ENDING IT”** (53 days live): "IT'S OFFICIAL: WE'RE ENDING IT": the #1 product is "flying off the shelves… last 60% off sale until our stock lasts".

**Do not copy (seen in these live ads):** The stock counts and "ending it" claims run for weeks, so they are not literally true. Only state real stock.

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| Low stock | Product photo + a live-looking stock bar | "Only 38 left of the Mae Necklace." |
| Back in stock | Bold "BACK" headline over the product | "Back in stock. Sold out in 9 days last time." |
| Limited-time offer | Offer in big type, end date | "Any 7 for $85 · Ends Sunday" |
| BFCM | Black background, gold type | "Black Friday: the stack deal, once a year." |

### Prompts

**Figma**

```
Headline 110px, offer line 56px, product 50% of canvas; a version per offer, same layout so only the message changes.
```

**Inventory link**

```
Pull the real stock number from Shopify on the day you post; update or pause the ad when it changes.
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
- [ ] Files named `F37-<concept>-<variant>`; tracking tag `utm_content=F37-<concept>-<variant>`.
- [ ] Avoid: Low-stock and deadline claims must be true (consumer law).
- [ ] Avoid: Turn ads off when the offer ends.
- [ ] Avoid: Don't run urgency all year; it stops working.

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
5. Name every asset `F37-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F37
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

Bottom-of-funnel statics built around a real time/stock constraint: "back in stock", "only N left", "ends Sunday", "BFCM: any 7 for $85 + free gift". Clean product + offer + deadline. For retargeting and seasonal pushes.

### Why it works

- Converts warm audiences who already know the product.
- LTO S-tier in a 2026 operator tier list.
- Mirrors Omnisend/OneText calendar → consistent offer across channels.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| Static A | "Back in stock" stamp on Chelsea Herringbone | — |
| Static B | "Any 7 for $85 — ends Sunday" over stack flat-lay | — |
| Static C | Low-stock bar "87% claimed" | Only with real data |

### Hooks

- "It's back (for now)"
- "Any 7 for $85 ends Sunday"
- "BFCM early access: build your stack"
- "Last restock before the holidays"

### Production recipe

1. Pull real stock/deadline from Shopify; schedule start/stop.
2. Templates for back-in-stock, ends-X, BFCM, gift-deadline (shipping cutoff).
3. Retarget 30-day engagers + site visitors; exclude purchasers 7d.
4. Mirror in email (Omnisend) + SMS (OneText) with same UTM concept.

### Existing bot prompt

```
Given the live offer {{OFFER}}, deadline {{DATE}} and stock data {{STOCK}}, write 8 urgency static headlines (≤8 words) and 8 subheads; only use scarcity that the data supports. Add matching Omnisend subject line and OneText SMS (≤140 chars).
```

### Variants to test

- Deadline vs stock framing
- Product vs stack image

## Reference examples

See [examples/README.md](examples/README.md) (16 posts). Top 5:

- @ads4apps (412L/930BM/27kV): 39 Meta formats that convert (930 bookmarks): X reasons, IG story, us vs them, Venn, don't buy this, iPhone notes, text message, low stock, we're sorry, breakin — https://x.com/ads4apps/status/2081785032679518490
- @williamkast_ (252L/400BM/13kV): Formats by funnel: TOF founder/yapper/AI animation/natives/3 reasons/voiceless overlay; MOF comment reply/testimonial mashup/text wall; BOF urgency statics. — https://x.com/williamkast_/status/2103910235005935644
- @nicktheriot_ (219L/348BM/12kV): 2026 FB creative styles tier list: S = long primary text + organic image, LTO, UGC, VSL, reaction, news; A = demo, us vs them, testimonial, close-up, founder st — https://x.com/nicktheriot_/status/2108173638033871013
- @raph_guilhem (9L/6BM/377V): 35 static/native formats tree: Trustpilot, text msg, email screenshot, Reddit, text on skin, crossed-out, tier list, Venn, breaking news. — https://x.com/raph_guilhem/status/2090725512976970065
- @EmerieOnoh (6L/6BM/498V): Static formats printing: us vs them, whiteboard, breaking news, doodle, low stock, iPhone notes, Google search, we're sorry, Reddit, tweet screenshot, text on p — https://x.com/EmerieOnoh/status/2098426706612683154
