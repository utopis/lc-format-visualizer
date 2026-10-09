# BOT.md · generate a "Persona pages: ads run from named narrator pages (catalog of the pattern + LC-safe version)"

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
5. Name every asset `F80-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F80
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

Big direct-response brands run hundreds of ads from pages named after a narrator ("Sarah Bennett", "Your Health Journal", "Dr. Lisa Downing") instead of the brand page. Each persona has an age, situation and voice and writes first-person natives. LC-safe version: real people (founder, CS lead, real customers with consent) as named narrators, clearly connected to LC, never invented people presented as independent.

### Why it works

- A first-person narrator page reads like a person, not a brand.
- Persona × angle multiplies ad diversity (more distinct "entities").
- Lets one product speak to many avatars (brides, mothers, swimmers).

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| Page | "Notes from Louise" (real founder) or "Jess from LC customer care" | first-person natives |
| Ad | Long-copy native about a real customer story (with consent) | "Here's what Maria told me…" |

### Hooks

- "Notes from our customer-care desk"
- "A bride wrote to us last week…"
- "I'm the founder, and this email made me cry"

### Production recipe

1. Map 6 real LC avatars (bride, swimmer, nurse, mother-of-the-bride, gift-giver, traveller).
2. Use real narrators with consent; ads clearly from LC.
3. Write 4 natives per avatar; rotate.

### Existing bot prompt

```
Using real stories {{CUSTOMER_STORIES}} (with consent), write 6 first-person natives, one per LC avatar, each ≤250 words, told by the real customer or a named LC staff member.
```

### Variants to test

- Avatar
- Founder vs customer narrator

## Reference examples

See [examples/README.md](examples/README.md) (20 posts). Top 5:

- @FedotOff90 (3L/8BM/1kV): Prime Prometics x-ray: 2,828 active ads, 24 avatars (6 life-event), ~28 narrator personas across 15 pages — persona-page scale pattern + MCP prompt. — https://x.com/FedotOff90/status/2108188222710862166
- @funneloftheweek (0L/0BM/0V): Resilia: 12 persona Pages → one 7-min advertorial (30-50% of traffic), 3-4 copy templates × hundreds of creatives, 544 new ads/30d, OTO flow $30→$83. — https://x.com/funneloftheweek/status/2044464896104857850
- @FedotOff90 (110L/208BM/9kV): 37 formats printing (with days active): AI podcast 280d, report card, iPhone Notes, text on skin, Reddit, cross-out, fake PDP, tier list, myth vs fact, zero sta — https://x.com/FedotOff90/status/2104949773539442831
- @Seanfrank (140L/113BM/55kV): "Ill just whitelist" Whitelisting is fine. But meta is REWARDING accounts that commit to partnership ads. This is fully tin foil hat theory now... but I have se — https://x.com/Seanfrank/status/2094988024211812654
- @vincenzo_micale (50L/69BM/4kV): Menopause bracelet brand: 1,592 active Meta ads, 107 days, 59% US — saturation-level creative volume in wearable/jewelry. — https://x.com/vincenzo_micale/status/2105349586717950002
