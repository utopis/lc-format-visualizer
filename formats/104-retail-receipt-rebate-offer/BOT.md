# BOT.md · generate a "Retail receipt rebate offer ad (\"buy 2 at Target, upload your receipt, get 1 back\")"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 1 static 1080x1350 + one 12-15s creator aisle clip), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@GustavWalsted](https://x.com/GustavWalsted/status/2105227892309594486) · Primal Queen's live offer page behind the Meta ad. The headline is "BUY ONE GET ONE FREE". How it works: 1) buy any 2 Primal Queen products at your nearest Target; 2) enter your phone number; 3) we text you a link to upload your receipt; 4) once verified we refund via PayPal or Venmo. "That's it. One product is on us." Under that is a "FIND MY CLOSEST target" store locator with a map. Paid social 
- Example: [@eCom_Amin](https://x.com/eCom_Amin/status/2099533970484646210) · primal queen prints $2M a month and their google funnel is the most complete i've dissected all year AI youtube ads with 1M+ views, an advertorial run

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| Static headline | Hand holding 2 products in a real retail aisle | "Buy 2 at [Retailer]. Get 1 back." |
| Static body | Three icons left→right: cart, receipt photo, money back | "Upload your receipt at [brand].com/rebate" |
| Static footer | Small print bar | "Ends [date]. 1 per customer. Terms at [url]." |
| Video 0-3s | Creator walks to the shelf | "Okay [Retailer] has [brand] now" |
| Video 3-10s | Grabs two, checkout, phone uploading the receipt | "and you get one back. Like, free." |
| Video 10-15s | End card with QR | "Rebate link in bio / tap Learn More" |

### Prompts

**Copy (Claude)**

```
Write 10 headline variants for a "buy 2 at {{RETAILER}}, get 1 back via receipt upload" offer. ≤8 words each, no exclamation marks, plus a 1-line legal footer.
```

**Targeting**

```
Meta location targeting: 10-15 mile radius around stores carrying the SKU; exclude existing DTC buyers 30d.
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
- [ ] Files named `F104-<concept>-<variant>`; tracking tag `utm_content=F104-<concept>-<variant>`.
- [ ] Avoid: Check the retailer agreement before advertising a rebate.
- [ ] Avoid: Payout delays kill trust; automate refunds within 7 days.
- [ ] Avoid: LC is DTC-only today; only use the trade-in variant until it has retail or marketplace presence.

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
5. Name every asset `F104-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F104
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

A DTC brand that has just landed in a retailer runs **Meta ads that send people to the store, not the website**: *"Buy 2 Primal Queen at Target → upload your receipt → we refund one."* The ad is a simple static or creator clip of the shelf, the offer, and a QR/receipt-upload page. It turns Meta spend into retail sell-through, which is what keeps a new brand on the shelf.

### Why it works

- Getting into Target is easy compared with selling enough to stay; this pushes velocity per store (@GustavWalsted).
- "Get one free" via rebate converts better than a percentage, and the brand still books 2 retail units.
- Receipt upload gives the brand the customer's email/phone, which retail normally hides.
- It reuses the brand's DTC audiences, now pointed at a store they already visit.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| Static | Creator hand holding 2 products in a store aisle (real shelf) | Headline: "Buy 2 at [Retailer]. Get 1 back." |
| Line 2 | Three icons: cart → receipt photo → money back | "Upload your receipt at [brand].com/rebate" |
| Footer | Retailer logo usage per retailer brand rules | "Limited time · terms apply" |
| Video version 0-3s | Creator walks to the shelf: "okay so Target has [brand] now" | — |
| 3-12s | Picks 2, shows phone uploading the receipt | "you literally get one back" |

### Hooks

- "Buy 2 at [Retailer], get 1 back"
- "It's at [Retailer] now. And the second one is on us."
- "Found it at [Retailer] 😭 here's the rebate"
- LC (Amazon/retail version): "Order on Amazon, send us your order number, get a free stack piece"

### Production recipe

1. Confirm the rebate is allowed under the retailer agreement and set budget caps.
2. Build a rebate page (Typeform/Jotform + receipt upload + email/phone); auto-reply with the payout timeline.
3. Make 3 statics + 2 creator clips; geo-target store radiuses (Meta location targeting).
4. Track redemptions per store; feed rebate emails into the CRM.
5. **LC now:** adapt as an Amazon/marketplace order-number rebate only if LC sells there; otherwise use the mechanic as a DTC 'send us your old green necklace photo, get $15' trade-in.

### Existing bot prompt

```
Write 6 Meta static concepts and 2 UGC scripts (15 s) for a 'buy 2 at {{RETAILER}}, upload receipt, get 1 back' offer for {{BRAND}}. Include the exact headline, sub-line, 3-step icon copy, legal footer, and a geo-targeting note. Keep claims to {{PDP_FACTS}}.
```

### Variants to test

- Rebate vs instant code
- Store-radius vs national
- Static vs creator aisle clip

## Reference examples

See [examples/README.md](examples/README.md) (3 posts). Top 5:

- @eCom_Amin (164L/360BM/28kV): primal queen prints $2M a month and their google funnel is the most complete i've dissected all year AI youtube ads with 1M+ views, an advertorial running on SH — https://x.com/eCom_Amin/status/2099533970484646210
- @GustavWalsted (9L/0BM/376V): Honestly, genius move @abdushodmonov. Hats off to you and the team. Primal Queen is running Meta ads with a simple offer: buy 2 products at Target, upload your  — https://x.com/GustavWalsted/status/2105227892309594486
- @zarastrategy (0L/0BM/1V): Us vs Them Meta Ads are the type of ad I would always bet on. Primal Queen does this really well. Primal Queen is in the women's supplement space and reportedly — https://x.com/zarastrategy/status/2090820261574529478
