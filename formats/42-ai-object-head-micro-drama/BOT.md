# BOT.md · generate a "AI object-head micro-drama (talking-fruit-style soap opera)"

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
5. Name every asset `F42-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F42
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

Serialized 1-2 min AI soap operas where characters are objects/fruit heads on human bodies (love, betrayal, plot twist). Massive organic views category; product placement is the play for a brand.

### Why it works

- Serialized cliffhangers drive follows and binge views.
- Novel aesthetic; huge category per claims.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0-5s | Fruit-head characters argue | Plot hook |
| 5-60s | Drama, twist | Lip-synced dialogue |
| 60-70s | Cliffhanger; LC piece as plot device | "Part 2" |

### Hooks

- "She found the necklace in his car…"
- "The ring that ruined the wedding (part 1)"

### Production recipe

1. Only as an experiment on a separate page; consistent characters via reference images; label AI.

### Existing bot prompt

```
Write a 6-episode outline for an AI object-head soap opera where an LC necklace is the plot device (heirloom, gift, mystery). Each episode: 60s, cliffhanger, no disparagement.
```

### Variants to test

- Characters
- Episode length

## Reference examples

See [examples/README.md](examples/README.md) (6 posts). Top 5:

- @bmx_ai13 (44L/6BM/1kV): AI micro-drama production skill (script → storyboard → consistent characters) — tool promo. — https://x.com/bmx_ai13/status/2103701345563812177
- @seergioo_gil (9L/12BM/6kV): Talking-fruit micro-dramas (+20B views claimed): 1-2 min love/betrayal story, fruit heads on human bodies, AI lip-sync, plot twist. Tool promo. — https://x.com/seergioo_gil/status/2089472288001347867
- @CodewizzyX (32L/22BM/3kV): THESE VIRAL "FRUIT DRAMA" AI VIDEOS AREN'T RANDOM - THERE'S AN ACTUAL FORMULA AND IT'S FREE TO COPY No camera, no writers room, no editing. Absurd fruit soap op — https://x.com/CodewizzyX/status/2096695495590568092
- @SmartEye_ADSpy (3L/0BM/242V): 🔥July 30 Global Micro Dramas & AI Micro Dramas: Multiple NetShort Horror Campus AI Dramas Secure Chart Rankings; Fruit-Themed AI Micro Drama Jumps to No.3 on Ti — https://x.com/SmartEye_ADSpy/status/2082748308293071171
- @SmartEye_ADSpy (3L/0BM/158V): Top 3 Claim Over 40% of Global Market Revenue; Breakout AI Micro Drama App VibeShort Cracks the Chart Market Revenue Is Highly Concentrated: In H1 2026, the Top — https://x.com/SmartEye_ADSpy/status/2087111287184728470
