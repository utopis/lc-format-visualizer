# BOT.md · generate a "Seasonal gifting campaign — launch 3-4 weeks early, urgency only in the final week"

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

See [examples/README.md](examples/README.md) (7 posts). Top 5:

- @herrmanndigital (160L/150BM/12kV): My Black Friday strategy on Meta is just leave on the ads you’ve had on all year. Then a second campaign on lifetime budgets with the sale ads. On Applovin, tak — https://x.com/herrmanndigital/status/2098058544654450850
- @chasebfisher (27L/12BM/795V): for Black Friday, swap your landing page and keep your winning creative running. a lot of brands do the opposite. they pause the ads that worked all year and la — https://x.com/chasebfisher/status/2107114066741231664
- @chasebfisher (20L/11BM/615V): build a separate batch of creative just for the week after Black Friday. a lot of brands pour everything into Black Friday and Cyber Monday, then pull way back  — https://x.com/chasebfisher/status/2105334969371447475
- @M__Operators (11L/6BM/747V): We are 87 days away from Black Friday. @codyplof, @couuor + @connorrolain open up their Q4 playbooks. Reuse top creative from 2025 Scale-up tests before BFCM La — https://x.com/M__Operators/status/2094809174907535497
- @umzrs (7L/6BM/1kV): How to add 30,000-50,000 new Email contacts to your list before BFCM 👇 Right now in September, ad costs are still baseline By mid-November, everyone and their m — https://x.com/umzrs/status/2103513124632449171
