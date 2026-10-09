# BOT.md · generate a "Mini-documentary / founder mini-VSL ('how it's made', mission)"

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
5. Name every asset `F50-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F50
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

A 60-180s documentary-style piece: open loop, problem, failed solutions, mechanism (PVD bonding process), product, mission. Longer form for warm audiences and YouTube.

### Why it works

- Mechanism education justifies price/claims.
- Open-loop structure holds attention.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0-5s | Open loop | "I almost shut Louise Carter down in year one." |
| 5-40s | Problem: jewelry turning green | Story |
| 40-80s | Mechanism: PVD process footage | VO |
| 80-110s | Customers, mission | — |
| 110-120s | Offer | — |

### Hooks

- "How waterproof gold is actually made"
- "I almost shut this brand down"

### Production recipe

1. Interview Qirra; supplier process footage (with permission).

### Existing bot prompt

```
Using {{FOUNDER_NOTES}} and {{PROCESS_FACTS}}, write a 120s mini-doc script in the Eskiin structure.
```

### Variants to test

- Length 60 vs 120s

## Reference examples

See [examples/README.md](examples/README.md) (11 posts). Top 5:

- @zackpaid (9L/20BM/2kV): 11 AI formats (agency pitch): native UGC, founder, claymation, Pixar 3D, jingle, screen recording, before/after, testimonial compilation, cinematic demo, mini-d — https://x.com/zackpaid/status/2085621175292670183
- @rirahcreates (18L/7BM/454V): AI formats to watch: Pixar storytelling, claymation, timeline/notes videos, cinematic product ads, virtual influencers, 3D product animation, AI documentary. — https://x.com/rirahcreates/status/2086324982892605618
- @luisfelipebfr2 (0L/0BM/166V): Eskiin founder mini-VSL breakdown: vision-board open loop → problem → failed solutions → mechanism → product → mission → retire mom. — https://x.com/luisfelipebfr2/status/2101018997508669891
- @lorenzo_pravata (0L/0BM/0V): Resilia ~8,000 ads, "$10-15M/month" (unverified); mostly AI avatars/doctors/claymation; gap = real authority reshoots + long unaware VSL. — https://x.com/lorenzo_pravata/status/2079246318191403496
- @adamtaylorl (36L/36BM/3kV): Dead in 2026: polished studio, "hey guys" UGC, discount statics, founder-story VSLs. Printing: ugly advertorial statics, long-form yapper, comment-reply hooks,  — https://x.com/adamtaylorl/status/2086814826177679660
