# BOT.md · generate a "Cinematic macro product film (15s, no dialogue)"

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
5. Name every asset `F49-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F49
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

A 6-15s premium macro film: water droplets on 14K gold, slow-motion splash, light sweep — no dialogue, one text line, logo. YouTube/CTV and solution-aware audiences.

### Why it works

- Premium perception; works sound-off.
- YouTube solution-aware format per one operator; 6s bumper cut.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0-3s | Macro water drop on herringbone | Sound design |
| 3-8s | Necklace through splash, slow-mo | — |
| 8-12s | On skin in sunlight | Text: "Shower-proof 14K PVD" |
| 12-15s | Logo + any 7 for $85 | — |

### Hooks

- Visual hook only: water hitting gold
- "Built for water."

### Production recipe

1. Shoot macro with phone macro lens + water spray, or AI image-to-video from real product photos (don't alter product).
2. Cuts: 15s, 6s bumper, 9:16/16:9.

### Existing bot prompt

```
Write a 15s shot list + AI video prompts for an LC macro film from these product photos {{IMAGES}}; preserve exact product design.
```

### Variants to test

- Real vs AI
- 15s vs 6s

## Reference examples

See [examples/README.md](examples/README.md) (9 posts). Top 5:

- @nicktheriot_ (219L/348BM/12kV): 2026 FB creative styles tier list: S = long primary text + organic image, LTO, UGC, VSL, reaction, news; A = demo, us vs them, testimonial, close-up, founder st — https://x.com/nicktheriot_/status/2108173638033871013
- @zackpaid (9L/20BM/2kV): 11 AI formats (agency pitch): native UGC, founder, claymation, Pixar 3D, jingle, screen recording, before/after, testimonial compilation, cinematic demo, mini-d — https://x.com/zackpaid/status/2085621175292670183
- @rirahcreates (18L/7BM/454V): AI formats to watch: Pixar storytelling, claymation, timeline/notes videos, cinematic product ads, virtual influencers, 3D product animation, AI documentary. — https://x.com/rirahcreates/status/2086324982892605618
- @lifemaximised (12L/9BM/990V): Highest-ROAS YouTube ad anatomy: outcome text hook, 9-shot claymation villain arc, CTA last 3s, non-discount offer, custom-intent audiences, 6s Shorts bumper. — https://x.com/lifemaximised/status/2087086851148660816
- @lifemaximised (8L/5BM/1kV): Top 4 YouTube ad formats by awareness: claymation 9-shot (unaware), hybrid AI UGC (problem-aware), 15s cinematic no-dialogue product film (solution-aware), 6s S — https://x.com/lifemaximised/status/2094059955472990517
