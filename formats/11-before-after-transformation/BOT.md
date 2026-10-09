# BOT.md · generate a "Before → After (static + video), incl. "Me before / me after" and Polaroid proof"

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
5. Name every asset `F11-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F11
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

Split image or 2-slide: left/first "before" (problem state), right/second "after" (result), with a date or condition label; video version = jump-cut transition. "People stop because they see a real change, not a product… then long primary text tells the story" ([@antonioventre_](https://x.com/antonioventre_/status/2078512377616589256)).

### Production recipe

Collect real wear-test photos from 10 customers/creators (send product, pay $50, 6-month check-in); meanwhile staff test. Metric: CTR, CPA; Omni.

## Reference examples

See [examples/README.md](examples/README.md) (12 posts). Top 5:

- @LachezarVoynov (396L/1453BM/88kV): 29 TOF video ad formats to test on Meta (transformation, Suno song, skit, beginner-intermediate-expert...). — https://x.com/LachezarVoynov/status/2086842038457098499
- @tryatria_AI (107L/147BM/6kV): Before->after ads printing; top 50 swipe (reply-bait for file). — https://x.com/tryatria_AI/status/2092961578974896447
- @antonioventre_ (79L/64BM/5kV): Before/after photos are best native ad image: change creates curiosity; long copy tells story. — https://x.com/antonioventre_/status/2078512377616589256
- @FedotOff90 (138L/247BM/16kV): Before and after format fucking prints. Nothing tells the story and shows the results of the product like before/ after image. Got a swipe file (freshly updated — https://x.com/FedotOff90/status/2085874661460713583
- @adamtaylorl (139L/203BM/13kV): Tier list of ecom formats: F = AI UGC, street interviews, read scripts; B = founder, testimonial compilations, listicle statics... — https://x.com/adamtaylorl/status/2097641383355879452
