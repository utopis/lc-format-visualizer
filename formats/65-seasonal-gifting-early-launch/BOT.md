# BOT.md · generate a "Seasonal gifting campaign — launch 3-4 weeks early, urgency only in the final week"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: Campaign: 3-4 week gifting runway (statics, videos, gift guide)), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@PowerbyMomBlog](https://x.com/PowerbyMomBlog/status/1733284392045543691) · A sponsored mom-blogger video (marked AD) for a personalised sterling silver heart locket: her daughter chose the photos, including their cat Ollie who died in July. Slow close-ups open the locket on a denim pouch next to purple flowers, and the post says it is on her Holiday Gift Guide. Emotional, gift-led and seasonal.
- Example: [@sayuri_quietjp](https://x.com/sayuri_quietjp/status/1997519250903482686) · クリスマスの贈り物に、 アクセサリーを選んでもらいました🎁✨ たくさん並ぶ宝石の中から、 「これが似合うよ」って言われた瞬間が いちばん輝いていた気がします…💎 大切な人と、大切な時間を そっと胸にしまって。 A special Christmas gift — a beautiful piece 
- Example: [@ecomchasedimond](https://x.com/ecomchasedimond/status/2047313886848925761) · ChatGPT Images 2.0 made this full Father’s Day campaign system with one prompt. One prompt gave me the landing page, email, SMS, ad creative, and popu
- Example: [@lifemaximised](https://x.com/lifemaximised/status/2107617132104036607) · STOP waiting for November to begin your Black Friday prep or you’ll get lapped by everyone starting NOW… BFCM is in 7 weeks already. It’s time to set 

### Live paid ads in this format (2 in [adlibrary/](adlibrary/README.md), longest-running first)

- **Smooche · Smooche: “Prime day SALE EXTRA on smooche.com”** (10 days live): "Prime day SALE EXTRA on smooche.com", 60% off, with a dropper shot.
- **Smooche · Smooche: “Prime day 60% off ONLY on smooche.com”** (10 days live): "Prime day 60% off ONLY on smooche.com" on a minimal grey background.

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| Week -4 to -3 | Gift-problem creative: "What do you get the friend who has everything?" | Gift guide carousel |
| Week -3 to -2 | Emotional gift moments (real customers) | "My mum hasn't taken it off since Christmas." |
| Week -2 to -1 | Bundle + gift box | "7 pieces, wrapped, $85." |
| Final week | Shipping-deadline urgency | "Order by Dec 18 for Christmas delivery." |
| Post-holiday | Gift-card and self-gifting | "You got cash? Treat yourself." |

### Prompts

**Calendar**

```
Map the 4 weeks, assign creatives to each, set real shipping cut-offs by region.
```

**Claude**

```
Write a gift guide carousel: 6 recipients, one stack each, with price and a one-line reason.
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
- [ ] Files named `F65-<concept>-<variant>`; tracking tag `utm_content=F65-<concept>-<variant>`.
- [ ] Avoid: Shipping deadlines must be real per region.
- [ ] Avoid: Urgency only in the final week.
- [ ] Avoid: Plan stock for the bundle you push.

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
5. Name every asset `F65-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F65
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

A season-long creative arc: weeks -4 to -2 = problem-framed gift ideas ("for the mom who never takes jewelry off"), week -1 = urgency and shipping cutoffs; creatives framed around the recipient's gifting problem, not seasonal clichés (hearts, red bows).

### Why it works

- Captures early researchers before competitors start.
- Gifting-problem framing beats generic seasonal visuals.
- Urgency saved for the final week stays credible.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| Week -4 | "Gifts for the mom who has everything (but takes her jewelry off)" | — |
| Week -3 | Recipient carousels (F57) | — |
| Week -2 | Testimonials from last season's gift buyers (F40) | — |
| Week -1 | Cutoff countdown + any 7 for $85 (F37/F64) | — |

### Hooks

- "The gift she'll actually wear in the shower"
- "Gifts for the friend who loses every necklace"
- "Order by [real date] for delivery"

### Production recipe

1. Calendar per season with week-by-week creative mix; one concept ID across ads/email/SMS.
2. Recipient personas: mom, partner, best friend, bridesmaids, self-gift.

### Existing bot prompt

```
Build a 4-week seasonal plan for {{SEASON}} with weekly creative types, 3 hooks per recipient persona, and the real shipping cutoff messaging.
```

### Variants to test

- Recipient persona
- Launch week

## Reference examples

See [examples/README.md](examples/README.md) (8 posts). Top 5:

- @PowerbyMomBlog (0L/0BM/0V):  — https://x.com/PowerbyMomBlog/status/1733284392045543691
- @herrmanndigital (160L/150BM/12kV): My Black Friday strategy on Meta is just leave on the ads you’ve had on all year. Then a second campaign on lifetime budgets with the sale ads. On Applovin, tak — https://x.com/herrmanndigital/status/2098058544654450850
- @chasebfisher (27L/12BM/795V): for Black Friday, swap your landing page and keep your winning creative running. a lot of brands do the opposite. they pause the ads that worked all year and la — https://x.com/chasebfisher/status/2107114066741231664
- @chasebfisher (20L/11BM/615V): build a separate batch of creative just for the week after Black Friday. a lot of brands pour everything into Black Friday and Cyber Monday, then pull way back  — https://x.com/chasebfisher/status/2105334969371447475
- @M__Operators (11L/6BM/747V): We are 87 days away from Black Friday. @codyplof, @couuor + @connorrolain open up their Q4 playbooks. Reuse top creative from 2025 Scale-up tests before BFCM La — https://x.com/M__Operators/status/2094809174907535497
