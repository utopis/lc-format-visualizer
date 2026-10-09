# BOT.md · generate a "Podcast-style ad (two mics, conversation clip)"

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
5. Name every asset `F13-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F13
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

Two people at podcast mics, warm studio, captions; clip starts mid-conversation with a strong opinion; host asks the question the viewer has; guest explains; product mentioned naturally. "They're not trying to make a podcast ad feel like an ad" ([@tryatria_AI](https://x.com/tryatria_AI/status/2097763972325745046)). "Best format for anything that needs explaining" ([@CEO_Vlad](https://x.com/CEO_Vlad/status/2096569603761827953)).

### Production recipe

Real: rent a podcast studio 2h → 15 clips. Metric: hold, CPA, Omni. Founder face also feeds organic (strategy 31).

## Reference examples

See [examples/README.md](examples/README.md) (13 posts). Top 5:

- @lorenzo_pravata (150L/196BM/10kV): "Ads that don't look like ads": podcast clips, street interviews, skits with studio actors; pet brand $29K→$150K/mo spend in 60 days, CPA $188→$124. — https://x.com/lorenzo_pravata/status/2104536224488738839
- @CEO_Vlad (88L/169BM/5kV): AI UGC formats tiered: S = podcast, talking head, in-car... — https://x.com/CEO_Vlad/status/2096569603761827953
- @LachezarVoynov (86L/102BM/10kV): $300k/mo strategy: wrappers that became top spenders = skits, carpool ads, Suno songs, AI Pixar-character podcasts; hooks must target different people. — https://x.com/LachezarVoynov/status/2097351286094021034
- @tryatria_AI (62L/74BM/3kV): Heights podcast ads: don't feel like ads, underrated performance format. — https://x.com/tryatria_AI/status/2097763972325745046
- @sixugc (6L/3BM/233V): genuinely confused why apps still don't get it they need to scale with content not ads found one tiktok account posting podcast style talking head clips single  — https://x.com/sixugc/status/2088316130070790246
