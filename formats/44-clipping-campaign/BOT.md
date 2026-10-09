# BOT.md · generate a "Clipping campaign (pay-per-view clippers distribute founder/podcast content)"

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
5. Name every asset `F44-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F44
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

Post a campaign on a clipping marketplace (Content Rewards, Whop clipping, Sideshift-type) paying a fixed rate per 1k views; dozens of clippers cut your long-form (founder podcast, lives, interviews) or a template format into shorts on their own accounts.

### Why it works

- Pay only for views; massive account diversity.
- One proven format × 100 clippers = outlier scale (Musa 522M views).

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| Source | Qirra 30-60 min podcast/live with stories | — |
| Campaign | Rules: min length, must show product/name, disclosure, $ per 1k views, cap | — |
| Clips | Clippers post on own pages | — |
| Pay | Verified views only | — |

### Hooks

- Clip prompt: "the moment Qirra explains why she started LC"
- "Customer story that made Qirra cry"

### Production recipe

1. Need source content first (F27 founder content, podcast).
2. Pick reputable marketplace with view verification; set CPM cap and budget cap.
3. Require #ad disclosure and approved claims list.

### Existing bot prompt

```
From this transcript {{TRANSCRIPT}} of Qirra's long-form content, list 15 clip-worthy 20-45s moments with hook line, timestamp, and on-screen caption.
```

### Variants to test

- $/1k views
- Source type

## Reference examples

See [examples/README.md](examples/README.md) (14 posts). Top 5:

- @SeoulJosephK (720L/2243BM/98kV): App marketing reading list: paid (athcanft), organic UGC (Superwall pod), Sideshift/Posted/Noise view-based campaigns, Jake Castillo for influencers. — https://x.com/SeoulJosephK/status/2072291737536803119
- @alexzgirbu (39L/36BM/2kV): Clipper earns ~$3k per 1M views cutting streams/vlogs into short clips submitted to Content Rewards/Clipping Net/Clipster campaigns. — https://x.com/alexzgirbu/status/2092441815739670637
- @Dkevs_ (13L/9BM/1kV): App clipping campaign hit 140K+ views while still testing formats; trained teen clippers (agency pitch). — https://x.com/Dkevs_/status/2104045499208831116
- @leonclipping (44L/66BM/3kV): Musa app: ONE format (4-sec shocked reaction to a body fact → mascot explains) = 522M views, 930 videos >100K, 100+ creators. — https://x.com/leonclipping/status/2107903429490135362
- @LinoLeighton (82L/170BM/11kV): I ran a clipping campaign at 10X ROAS previously. Here’s exactly how I did it: • Paid anywhere from $0.20–$0.60 CPM depending on the country • Sourced clippers  — https://x.com/LinoLeighton/status/2096622664223707174
