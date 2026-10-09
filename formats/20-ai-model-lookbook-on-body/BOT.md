# BOT.md · generate a "AI model lookbook / on-body try-on (from real product photos)"

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
5. Name every asset `F20-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F20
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

Diverse models wearing the exact piece in lifestyle scenes (beach, office, wedding); or a 15s photoreal UGC try-on clip generated from the product photo (prompt structure from [@Arina_hoqe](https://x.com/Arina_hoqe/status/2095071815483986241): PRODUCT · DURATION exactly 15s · STYLE photorealistic UGC · scene beats · camera · audio).

### Production recipe

Nano Banana / GPT Image edit with the real product photo as reference; QC each image against the real piece (chain link pattern, clasp, width) — reject any hallucinated detail; real photos for PDP hero.

## Reference examples

See [examples/README.md](examples/README.md) (9 posts). Top 5:

- @rirahcreates (70L/53BM/8kV): AI fashion content: lookbooks, campaign images. — https://x.com/rirahcreates/status/2106081343566381455
- @Arina_hoqe (42L/36BM/4kV): Full prompt for 15s photoreal UGC watch ad from your own product photo ('Running Late'). — https://x.com/Arina_hoqe/status/2095071815483986241
- @MimiTheDesigner (31L/13BM/2kV): Fashion: every model/dress in video AI-generated; boutiques advertising this way. — https://x.com/MimiTheDesigner/status/2080184317771227394
- @KarinaRed123 (0L/0BM/0V):  — https://x.com/KarinaRed123/status/2099477629078307041
- @girlincrypto007 (89L/9BM/4kV): You need the right AI model for every task so you don’t burn through your limits too fast 👀 My stack is simple: > @claudeai Fable - for building a portfolio, la — https://x.com/girlincrypto007/status/2077765449371025600
