# BOT.md · generate a "Shock & gross visual (the problem in close-up)"

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
5. Name every asset `F83-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F83
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

The opening image is the ugliest, most specific version of the problem: a green ring mark on a finger, black flakes of plating, a discoloured line on the neck. The shock stops the scroll; the solution follows.

### Why it works

- Disgust and recognition are strong stop signals.
- A specific problem visual beats an abstract claim (7 Trends #1).
- The viewer self-identifies instantly.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0-2s | Macro: green band on a finger | "This is what cheap gold does to your skin." |
| 2-10s | Flaking chain under a loupe | — |
| 10-20s | LC piece, same finger after 3 months | "14K PVD. Bonded." |

### Hooks

- "This is what cheap gold does to your finger"
- "Zoom in on your plated necklace"

### Production recipe

1. Shoot real green-stain marks (own tests); no customer photos without consent.
2. Keep it tasteful: no medical skin conditions.
3. Static + 15s video.

### Existing bot prompt

```
Write 4 shock-visual openers for LC (what the macro shot shows, first line), each followed by a 15s solution arc. No medical claims.
```

### Variants to test

- Static vs video
- Shock level

## Reference examples

See [examples/README.md](examples/README.md) (3 posts). Top 5:

- @FedotOff90 (238L/632BM/20kV): 7,500+ winning Meta ads sorted by format across public boards (top-50 DTC, beauty, natives, listicles, shock & gross, BOFU). — https://x.com/FedotOff90/status/2093350155751924213
- @FedotOff90 (30L/31BM/3kV): Dog joint pain 4 formats, all 200+ days: "SCAM ALERT… turns out it works?" static, brace carousel, sticky-note UGC, quote carousel — format | lander | offer | d — https://x.com/FedotOff90/status/2097694037050642468
- @FedotOff90 (3L/7BM/2kV): Gross ads get banned in every "clean creative" guide. They keep making money anyway. A gross picture (the parasite, the plaque, the gunk in your pillow) stops t — https://x.com/FedotOff90/status/2099967483071582480
