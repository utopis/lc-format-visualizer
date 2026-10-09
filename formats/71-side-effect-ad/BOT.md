# BOT.md · generate a "'Side effect' ad (a positive side effect framed as a warning)"

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
5. Name every asset `F71-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F71
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

A warning-label or "side effects may include…" framing for good outcomes: compliments, people asking where it's from, never taking it off, a friend stealing it. The form mimics a warning label; the content is a benefit.

### Why it works

- A warning label is a pattern interrupt and promises social payoff.
- It sells the emotional result (compliments) rather than features.
- Works as a static, a label graphic, or a 10s text video.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| Static | Pharmacy-style label: "Side effects may include: compliments, 'where is that from?', never taking it off" | Primary text: "Warning: people will ask" |
| Video 10s | Text bubbles popping up around a wearer | "side effects of wearing LC for a week" |

### Hooks

- "Warning: people will ask where it's from"
- "Side effects may include: 14 compliments a week"
- "Side effect: your sister stealing it"

### Production recipe

1. Use real compliments from reviews and DMs (with permission) as the side-effect list.
2. Label design: white label, black type, red warning icon.
3. No medical framing in jewelry copy.

### Existing bot prompt

```
Write 8 "side effects may include…" statics for LC with 3-5 side effects each, taken only from {{REVIEWS}}, plus a 100-word primary text.
```

### Variants to test

- Label vs text video
- Compliment vs durability side effects

## Reference examples

See [examples/README.md](examples/README.md) (7 posts). Top 5:

- @FedotOff90 (110L/208BM/9kV): 37 formats printing (with days active): AI podcast 280d, report card, iPhone Notes, text on skin, Reddit, cross-out, fake PDP, tier list, myth vs fact, zero sta — https://x.com/FedotOff90/status/2104949773539442831
- @SharylAttkisson (1358L/52BM/21kV): I see the pharmaceutical industry is still using the FDA loophole-- with FDA approval-- that lets them avoid the intended side effect warnings that are supposed — https://x.com/SharylAttkisson/status/2106877084337373536
- @tryatria_AI (19L/55BM/10kV): This AI-generated supplement ad is basically a mini documentary. It starts with a provocative hook, then tells a founder story around low testosterone, TRT, sid — https://x.com/tryatria_AI/status/2086829970228142494
- @feral_feed (28L/1BM/982V): Ads that would get a modern brand cancelled built Abercrombie’s most valuable era. Mike Jeffries didn’t hide the strategy. 2006, Salon interview: the retailer d — https://x.com/feral_feed/status/2103282293091848204
- @danisdriven (23L/0BM/2kV): YOUR CPM SHOULD NOT REQUIRE A PRESCRIPTION. If your brand is suffering from Chronic High CPM, low views, weak distribution and sudden unexplained drops in atten — https://x.com/danisdriven/status/2098523718595342565
