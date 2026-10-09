# BOT.md · generate a "Tier-list / ranking ad"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 30-60s video or 1 static), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@deepbajwacreate](https://x.com/deepbajwacreate/status/2098014748570739055) · A creator holding a printed tier list (S/A/B/C/D) and ranking popular side hustles one card at a time, with captions, ending on the product he places at the top (an Ecom Degree signup page).
- Example: [@adamtwtz](https://x.com/adamtwtz/status/2097925109155549689) · there's a gym app called Symmetry doing 150,000 downloads a month off one slideshow format the product is basically an AI body scanner, you just take 
- Example: [@fuxps32](https://x.com/fuxps32/status/2067026390588039329) · 400,000 likes, 80,000 saves, 0 sales pitches A woman scrolls her feed and stops on a supplement tier list. S tier, A tier, B tier, ranked on screen. S
- Example: [@ViralSpyApp](https://x.com/ViralSpyApp/status/2106822218961293724) · Tutti put piano in 'easy to learn' and its own practice app among the hardest. The one-screen instrument tier list got 824k plays and 4,532 comments. 
- Example: [@JamestheUGCguy](https://x.com/JamestheUGCguy/status/2027472175339332091) · UGC example video for custom promo products in a tier list format. Really enjoy using formats that showcase products in fun ways. Brands, if you need 
- Example: [@BuckleUp99](https://x.com/BuckleUp99/status/2074426426942722118) · Everyone's using AI to fake UGC ads. I used it to invent a new ad format. An AI doctor. A live tier list. Real supplement verdicts. No script feel. No
- Example: [@adswithcami](https://x.com/adswithcami/status/2095208948764668068) · I Ranked Every AI Ad Format For Ecom Brand Owners Whether your struggling to find winners with AI ads, or just need to know which AI formats work best

### Live paid ads in this format (6 in [adlibrary/](adlibrary/README.md), longest-running first)

- **FurryWell Philippines: Report-card rating static (FurryWell "A+ / 9.7")** (188 days live): An "Overall Guide A+ / Total Rating 9.7/10" card with bars (Ingredient quality 9.7, Flavour 10, Scent 10, Value 9) and a SHOP NOW button.
- **Smooche · Cosmetic Times: “Revlon color stay. Six out of ten. Yes, she stays put…”** (9 days live): Opens: “Revlon color stay. Six out of ten.”
- **Smooche · Korean Beauty Tips: “See this orange? That is not your skin. That is your foundation…”** (7 days live): Opens: “See this orange? That is not your skin.”
- **Smooche · Korean Beauty Tips: “This is how your skin looks bare. And this is what 40 years of the…”** (7 days live): Opens: “This is how your skin looks bare. And this is what 40 years of the wrong foundation did to it.”
- **Smooche · Korean Beauty Tips: “This is what you're found in your fine lines by lunch. Let me show you…”** (7 days live): Opens: “This is what you're found in your fine lines by lunch. Let me show you the four worst offenders.”
- **Smooche · Korean Beauty Tips: “and this is what your foundation is really doing to your face. Let me…”** (6 days live): Opens: “and this is what your foundation is really doing to your face. Let me rank the one.”

**Do not copy (seen in these live ads):** The ranking presenter is an AI persona with an invented credential, posted from pages like "Korean Beauty Tips" and "James Miami MUA". Use a real, disclosed reviewer.

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| 0-2s | Creator holding or in front of an S/A/B/C/D/F tier board | "Ranking every type of gold jewelry for people who never take it off" |
| 2-40s | Places each option card, explains each placement in one line | Fair, specific reasons (plated: D, vermeil: B, solid: A, PVD: S) |
| 40-50s | Product placed in S with a reason | Why it wins |
| End | Full board | Offer |

### Prompts

**Board**

```
Use tiermaker.com or a printed board; cards with category names, not competitor brands.
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
- [ ] Files named `F31-<concept>-<variant>`; tracking tag `utm_content=F31-<concept>-<variant>`.
- [ ] Avoid: Ranking named competitors unfairly is risky; rank categories.
- [ ] Avoid: The product must deserve its tier; give a real reason.

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
5. Name every asset `F31-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F31
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

The creator (or a static) ranks options in S/A/B/C/D/F tiers — e.g. "every type of gold jewelry ranked for people who never take it off" — explaining each placement; the product lands in S-tier with the reason. Works as video (talking over a tier-maker board) or static image.

### Why it works

- Feels organic and borrows authority — the ranker looks like an impartial expert (@mattdenegri).
- People can't scroll past a ranking: they want to see where their pick lands; disagreement drives comments.
- Educates the category (plated vs vermeil vs PVD vs solid) while positioning LC.
- Cheap to produce and endlessly re-rankable.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0-2s | Empty tier board on screen + creator face cut-out (green screen) | "Ranking every type of gold jewelry for people who never take it off" |
| 2-10s | F/D tier: gold-plated brass, "gold tone" | "Turns green in a week. F." |
| 10-18s | C/B: gold-filled, vermeil | "Okay, but not in the ocean." |
| 18-26s | A: solid 14K | "Amazing… if you have $900." |
| 26-35s | S: 14K PVD (LC piece image) | "Bonded, shower-proof, and any 7 are $85. S-tier." |
| 35-40s | Full board | "Where would you put yours?" |

### Hooks

- "Ranking every type of gold jewelry (I'm going to make people mad)"
- "Jewelry you can shower in: tier list"
- "Tier-ranking my most-worn pieces after 6 months"
- "Gifts for her ranked by how often she'll actually wear them"
- "Every way to stop your jewelry turning green, ranked"

### Production recipe

1. Tier board template (Figma/Canva) in LC colors + generic tiermaker version for native feel.
2. Script: 5-7 items, each with a one-line verdict; LC never ranks competitor brands by name — rank categories/materials.
3. Shoot creator on green screen over the board; or make static 4:5 version.
4. Organic: invite disagreement ("where would you put yours?").

### Existing bot prompt

```
Write 5 tier-list ad scripts for Louise Carter. Topics: materials (plated, filled, vermeil, sterling, solid 14K, 14K PVD), stack types, gift ideas, "ways to stop green neck", travel jewelry. Each: hook ≤10 words, 6 items with tier + 1-line verdict (≤12 words), LC lands S with a factual reason from {{PDP_FACTS}}. No competitor brand names; no false claims about other materials (keep generalised, factual).
```

### Variants to test

- Video vs static
- Creator ranker vs faceless board
- Material vs gifting topic
- Controversial F-tier pick vs safe

## Reference examples

See [examples/README.md](examples/README.md) (13 posts). Top 5:

- @ads4apps (412L/930BM/27kV): 39 Meta formats that convert (930 bookmarks): X reasons, IG story, us vs them, Venn, don't buy this, iPhone notes, text message, low stock, we're sorry, breakin — https://x.com/ads4apps/status/2081785032679518490
- @FedotOff90 (110L/208BM/9kV): 37 formats printing (with days active): AI podcast 280d, report card, iPhone Notes, text on skin, Reddit, cross-out, fake PDP, tier list, myth vs fact, zero sta — https://x.com/FedotOff90/status/2104949773539442831
- @MethodByVid (37L/67BM/4kV): 12 no-edit video formats: text story over gameplay, would-you-rather, guess-the-X quizzes, rankings, restoration, recipes from above. — https://x.com/MethodByVid/status/2087570057262256130
- @masterhooks_ (12L/13BM/1kV): 10 organic formats from a creator agency: storytelling, talking head, reaction, ranking, tier list, object lesson, play/pause reaction, AMA, comparison, before/ — https://x.com/masterhooks_/status/2100071930074390796
- @raph_guilhem (9L/6BM/377V): 35 static/native formats tree: Trustpilot, text msg, email screenshot, Reddit, text on skin, crossed-out, tier list, Venn, breaking news. — https://x.com/raph_guilhem/status/2090725512976970065
