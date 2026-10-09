# BOT.md · generate a "Day in the life / behind the scenes (founder or customer)"

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
5. Name every asset `F45-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F45
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

Vlog-style sequence of a day — founder running LC or a customer living in her jewelry (gym → shower → work → date) — with the product present in every scene. Paid version: 20-30s cut with text hook.

### Why it works

- Parasocial, native vlog grammar; product proof through continuity (same necklace all day).
- Framework that converts one message into a new Entity ID (@williamkast_).

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0-2s | 0.5x POV alarm, necklace on nightstand? No — already on | "Day in my life wearing the same necklace for 24h" |
| 2-8s | Gym | Sweat |
| 8-12s | Shower | "still on" |
| 12-20s | Work / coffee | Compliment from coworker (real) |
| 20-25s | Pool/dinner | "any 7 for $85" |

### Hooks

- "Day in the life of a jewelry founder (the unglamorous version)"
- "24 hours in the same necklace"
- "A day packing 1,000 orders"

### Production recipe

1. Film with phone 0.5x lens; 8-12 scenes; natural audio.
2. Organic first; paid cut only if organic retention ≥ average.

### Existing bot prompt

```
Turn this list of a real day's scenes {{SCENES}} into a 25s DITL script: hook text, scene captions (≤6 words), and one product moment per scene.
```

### Variants to test

- Founder vs customer
- 0.5x POV vs standard

## Reference examples

See [examples/README.md](examples/README.md) (10 posts). Top 5:

- @nicktheriot_ (219L/348BM/12kV): 2026 FB creative styles tier list: S = long primary text + organic image, LTO, UGC, VSL, reaction, news; A = demo, us vs them, testimonial, close-up, founder st — https://x.com/nicktheriot_/status/2108173638033871013
- @williamkast_ (38L/46BM/3kV): Turn 1 winning ad into 5: same message, different frameworks (DITL, 3 reasons, old me/new me, phone call). — https://x.com/williamkast_/status/2086835243474985414
- @Ecombos_Ai (28L/26BM/2kV): 10 AI UGC styles: talking-head testimonial, product-in-hand, first-try reaction, fake podcast, street interview, comment reply, unboxing, DITL/GRWM, before/afte — https://x.com/Ecombos_Ai/status/2103180929057407425
- @rirahcreates (12L/17BM/1kV): 20 UGC types: talking head, review, unboxing, testimonial, demo, problem/solution, before/after, GRWM, DITL, voiceover, routine, how-to, FAQ, 3 reasons why, POV — https://x.com/rirahcreates/status/2089827933561016787
- @ugcAshleyRJ (13L/5BM/534V): The 0.5x ultra-wide POV filming technique for demos, GRWM and day-in-the-life — immersive, native. — https://x.com/ugcAshleyRJ/status/2067636022251290725
