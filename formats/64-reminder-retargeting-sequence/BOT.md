# BOT.md · generate a "Reminder / retargeting sequence ads (abandoned cart, countdown, back-in-stock, wishlist, cross-sell)"

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
5. Name every asset `F64-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F64
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

A planned sequence of short reminder creatives for people who already showed intent, each matched to their moment: cart abandoners (the exact piece), bundle-incomplete ("you've picked 4 — 3 more for the same $85"), event countdowns (shipping cutoff), back-in-stock, post-purchase cross-sell (matching huggies).

### Why it works

- Highest-intent audiences; message matches the exact moment.
- Bundle-completion reminder is LC-specific AOV lever.
- Mirrors email/SMS so the story is consistent across channels.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| Day 0-1 | Cart: DPA of the exact piece + "it's waterproof" | — |
| Day 2-3 | Social proof: real review about that piece | — |
| Day 4-7 | Bundle: "3 more pieces, same $85" | — |
| Gift window | "Order by Dec 15 for delivery" | Real cutoff |
| Post-purchase D10 | Cross-sell matching piece | — |

### Hooks

- "Still in your bag: Chelsea Herringbone"
- "You picked 4. 3 more, same $85."
- "Last day for gift delivery"
- "Back: the huggies you saved"

### Production recipe

1. Audiences: ATC 7d, IC 7d, viewed 14d, purchasers 10-60d (cross-sell), engagers 30d.
2. Frequency caps; exclude recent purchasers from acquisition reminders.
3. Mirror each step in Omnisend/OneText with the same concept ID.

### Existing bot prompt

```
Design a 5-step LC reminder sequence (audience, timing, creative type, copy ≤12 words, matching email/SMS line) for: cart, bundle-incomplete, gift cutoff, back-in-stock, cross-sell. Only real deadlines/stock.
```

### Variants to test

- Message per step
- Static vs DPA

## Reference examples

See [examples/README.md](examples/README.md) (10 posts). Top 5:

- @bogdan_ai (826L/1735BM/192kV): $15K revenue in the last 30 days. $1.7K MRR. not flexing. just sharing what I learned so you can skip my mistakes. this is what worked: I stopped selling softwa — https://x.com/bogdan_ai/status/2080955204304769061
- @wizofecom (26L/18BM/4kV): Let me guess You built your abandoned cart flow when the store was doing 200 sessions a day. And nobody's touched it since. - Timing written for a smaller store — https://x.com/wizofecom/status/2099554762995708353
- @travis_mcewan (13L/12BM/579V): You can’t retarget abandoned carts if Meta can’t see the carts being abandoned. That sounds obvious, but it gets missed more often than you’d think. A brand may — https://x.com/travis_mcewan/status/2088656209180242228
- @GlennNieuwenh (19L/6BM/1kV): If I took over a struggling store tomorrow... I wouldn't open the ads manager on day one: I'd start with the numbers. First, a real P&L. - Cost of goods and shi — https://x.com/GlennNieuwenh/status/2093369535248154778
- @zakburgers (17L/4BM/1kV): II find it kinda crazy when I onboard brands that are doing 7 figs a month and they don't have email flows Just imagine the math behind email sales Say you've g — https://x.com/zakburgers/status/2080407812891455789
