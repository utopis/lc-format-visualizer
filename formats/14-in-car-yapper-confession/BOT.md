# BOT.md · generate a "In-car / "yapper" confession talking head"

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
5. Name every asset `F14-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F14
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

Creator in a parked car (or walking), phone propped, talking fast and personal: "I couldn't even wait to go inside to tell you." One continuous story, light jump cuts, captions. Why it works ([@jennamediaco](https://x.com/jennamediaco/status/2106209597526540312)): car looks organic, a story the whole time, feels private and unscripted.

### Production recipe

Brief 10 creators via Trybe/creator network (strategy 28) with 3 story prompts; allow improvisation; run as Partnership ads. Metric CPA; Omni new-customer.

## Reference examples

See [examples/README.md](examples/README.md) (16 posts). Top 5:

- @hectorserrranoo (210L/251BM/15kV): Wispr Flow paid UGC program: what companies get wrong. — https://x.com/hectorserrranoo/status/2107526350605070475
- @CEO_Vlad (88L/169BM/5kV): AI UGC formats tiered: S = podcast, talking head, in-car... — https://x.com/CEO_Vlad/status/2096569603761827953
- @FedotOff90 (74L/143BM/7kV): "Yappers are printing" — 299 raw talking-head yapper ads in one public swipe board (GetHookd "Yapper Ads (raw talking-head UGC) - Oct 2026"). — https://x.com/FedotOff90/status/2108198291242676622
- @LachezarVoynov (86L/102BM/10kV): $300k/mo strategy: wrappers that became top spenders = skits, carpool ads, Suno songs, AI Pixar-character podcasts; hooks must target different people. — https://x.com/LachezarVoynov/status/2097351286094021034
- @hectorserrranoo (99L/83BM/8kV): Panel: you're nothing without your creators (Comfrt: 10 creators = big share of revenue). — https://x.com/hectorserrranoo/status/2106136430556672384
