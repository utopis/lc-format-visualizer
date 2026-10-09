# BOT.md · generate a "Hyper-real first-person POV footage"

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
5. Name every asset `F23-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F23
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

Camera = viewer's eyes; hands wearing the product doing real things; a narrative tension (will it survive?).

### Production recipe

Real GoPro/phone chest-mount (preferred) — AI only for impossible shots, labelled.

## Reference examples

See [examples/README.md](examples/README.md) (3 posts). Top 5:

- @spwfeijen (46L/49BM/5kV): Hyper-real first-person POV footage with narrative tension keeps watch time near 100%. — https://x.com/spwfeijen/status/2105648964716380197
- @antonioventre_ (8L/4BM/693V): Production rule: reaction can't be scripted — founder-customer call + POV reaction ads with live unscripted reaction. — https://x.com/antonioventre_/status/2091895054755373116
- @DeQueenofSpaces (100L/2BM/2kV): First-person POV vs Third-person POV. Welcome back to this week's AI Creation Lab, where we're exploring Point of View. For this experiment, I created a fitness — https://x.com/DeQueenofSpaces/status/2100177884975612016
