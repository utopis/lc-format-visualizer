# BOT.md · generate a "'We're sorry, we keep selling out' apology notice"

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
5. Name every asset `F75-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F75
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

A notice-style static written as an apology: "We're sorry. We didn't expect to keep selling out of ___." The body explains why demand spiked (the mechanism) and that it is back in stock now. Scarcity and social proof wrapped in humility.

### Why it works

- An apology reads as an announcement, not an ad.
- "Keeps selling out" is evergreen demand-based urgency (7 Trends #6).
- The story explains why others buy it.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| Static | Plain cream notice card, signature at the bottom: "We're sorry. Chelsea Herringbone sold out [N] times this summer." | Body: why (waterproof), it's back, any 7 for $85 |

### Hooks

- "We're sorry, it sold out again"
- "An apology from Louise Carter"
- "To everyone on the waitlist: we're sorry"

### Production recipe

1. Run it only for SKUs that really sold out (log the dates).
2. Signed by the founder or team.
3. Retarget waitlist and visitors first, then go cold.

### Existing bot prompt

```
Write 3 "we're sorry, we keep selling out" notices for LC SKUs with real sell-out history {{SELLOUTS}}: ≤70-word card text + 120-word primary text.
```

### Variants to test

- Founder signature vs team
- Cold vs retargeting

## Reference examples

See [examples/README.md](examples/README.md) (10 posts). Top 5:

- @briannjho (138L/338BM/10kV): Ad picks: Smooche AI song ad, Ryze AI skit, UndrDog big-enemy, Everyday Dose skit, Serene Herbs AI identity, Nuora apology mash-up, Mama Bear "this is what happ — https://x.com/briannjho/status/2094662259746480410
- @FedotOff90 (17L/18BM/3kV): Rebuilt the formats list with proof: 30-day survival column = "this works" bar; copy the structure, not the words. — https://x.com/FedotOff90/status/2100948331136782532
- @FedotOff90 (110L/208BM/9kV): 37 formats printing (with days active): AI podcast 280d, report card, iPhone Notes, text on skin, Reddit, cross-out, fake PDP, tier list, myth vs fact, zero sta — https://x.com/FedotOff90/status/2104949773539442831
- @OmologatoUK (0L/0BM/0V):  — https://x.com/OmologatoUK/status/2099497006158725545
- @ChichiChachaha (251L/24BM/10kV): #Overdo sets a new pre-release advertising record. ~RMB 120M secured from ads &amp; sponsorships bef. its premiere date is even announced. 20+ brand partnership — https://x.com/ChichiChachaha/status/2076303701426471059
