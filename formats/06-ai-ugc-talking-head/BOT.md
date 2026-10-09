# BOT.md · generate a "AI UGC talking-head (avatar) — and its realism stack"

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
5. Name every asset `F06-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F06
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

A phone-selfie video of a "creator" talking to camera — bedroom, bathroom, car, kitchen — holding/wearing the product, 15-45s, casual captions. Sub-formats ranked by @CEO_Vlad: **S** podcast ad, talking head ("cleanest test of whether your angle works"), in-car ("reads private, cheapest to render well"); **A** street interview, multi-scene demo; **B** reply-to-comment overlay, split-screen day.
Example (jewelry): GIVA collection "I'm obsessed with these tiny little things and I've been stacking them like this…" (Arcads promo, [@SparkifyAI](https://x.com/SparkifyAI/status/2101869170937958407)).

Script skeleton (30s): 0-3s hook line + gesture ("I don't usually film unboxings but…") · 3-15s problem/story · 15-25s product proof (close-up, real product footage cut-in) · 25-30s CTA.

### Production recipe

Angles from real reviews (Claude: cluster LC reviews into motivators: shower-proof, gifting, compliments, sensitive skin feel, value of stack) → script per motivator → avatar (Arcads/HeyGen/Higgsfield; or Seedance/Veo with reference image) → voice (ElevenLabs, matched) → **real LC product B-roll cut-ins** (never render the jewelry with AI in close-up) → CapCut captions.

## Reference examples

See [examples/README.md](examples/README.md) (37 posts). Top 5:

- @jakecastilloooo (984L/3090BM/290kV): Ex-Cal AI UGC lead's full AI UGC workflow (article): customer context → outlier videos vs creator baseline → reverse-engineer → believable first frame → test ta — https://x.com/jakecastilloooo/status/2107873317369581751
- @kristian_jennin (1123L/3024BM/231kV): AI UGC looks fake because of a missing step (realism workflow video). — https://x.com/kristian_jennin/status/2101352217089282066
- @eliasrrecom (266L/548BM/54kV): Realistic AI UGC ads tutorial. — https://x.com/eliasrrecom/status/2092612451623694388
- @zedmadeit (347L/472BM/20kV): Intentional AI ad system starting from brand/product/customer, visuals matched to script. — https://x.com/zedmadeit/status/2107552798842003488
- @adamtaylorl (266L/426BM/22kV): Hike Footwear ad 100% AI. — https://x.com/adamtaylorl/status/2089713928511345017
