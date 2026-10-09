# BOT.md · generate a "Sweepstakes / celebrity giveaway campaign ad"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: Hero static 1080x1350 + 15s video + winner recap), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@Seanfrank](https://x.com/Seanfrank/status/2080703453853282629) · Ridge's "2026 Summer Sweepstakes" key visual: two men next to a lifted truck under the headline "Prizes worthy of a pro", with Shop Now and Learn More buttons. A celebrity-backed giveaway is the creative.
- Example: [@gleamapp](https://x.com/gleamapp/status/2094054316361269314) · NEW from Gleam. Spending money on ads and wondering if a giveaway could get you leads for less? Use the Giveaway vs Paid Ads Cost Per Lead Calculator.
- Example: [@EcomVictor](https://x.com/EcomVictor/status/2075924232333058211) · If you're not offer-stacking and valuemaxxing in 2026 as an ecom brand, scaling profitably will be MUCH harder for you. Grüns is pushing a discount + 

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| Hero static | Celebrity/creator + the big prize visual | "WIN [prize]" + entry method + end date |
| Video 0-3s | Celebrity says the prize to camera | "I'm giving away..." |
| Video 3-12s | Prize B-roll + how to enter | Email/SMS entry, no purchase necessary |
| Recap ad | Real winners announced | Social proof for the next round |

### Prompts

**Legal checklist**

```
Official rules, no-purchase-necessary entry, eligibility, odds, sponsor address, end date; use an administrator (e.g. Marden-Kane) for US sweepstakes.
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
- [ ] Files named `F25-<concept>-<variant>`; tracking tag `utm_content=F25-<concept>-<variant>`.
- [ ] Avoid: Sweepstakes law: purchase cannot be required to enter in the US; get official rules reviewed.
- [ ] Avoid: Collect consent for email/SMS properly (TCPA).
- [ ] Avoid: Celebrity likeness needs a contract.

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
5. Name every asset `F25-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F25
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

Hero creative: celebrity/creator + big prize visual; entry = email/SMS (or purchase = bonus entries); countdown; recap winners. Ridge used Marden Kane / RTM Media for administration ([@couuor](https://x.com/couuor/status/2098515153654562908)). Their 2026 mix shifted toward Facebook (46.7%) and TikTok (9.1%, ROAS +361%).

## Reference examples

See [examples/README.md](examples/README.md) (4 posts). Top 5:

- @couuor (167L/180BM/25kV): Ridge sweepstakes w/ Tony Hawk, $500k prizes: ~50% rev growth YoY at better MER; budget breakdown. — https://x.com/couuor/status/2098515153654562908
- @Seanfrank (100L/9BM/9kV): Me and Tony Hawk want to give you a Lamborghini: Every year, ridge does a sweepstakes. You have watched them evolve from tiny little campaigns, to gold plated c — https://x.com/Seanfrank/status/2080703453853282629
- @gleamapp (16L/0BM/4kV): NEW from Gleam. Spending money on ads and wondering if a giveaway could get you leads for less? Use the Giveaway vs Paid Ads Cost Per Lead Calculator. Compare y — https://x.com/gleamapp/status/2094054316361269314
- @EcomVictor (5L/1BM/482V): If you're not offer-stacking and valuemaxxing in 2026 as an ecom brand, scaling profitably will be MUCH harder for you. Grüns is pushing a discount + free gifts — https://x.com/EcomVictor/status/2075924232333058211
