# BOT.md · generate a "Sweepstakes / celebrity giveaway campaign ad"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

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
