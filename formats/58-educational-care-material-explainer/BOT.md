# BOT.md · generate a "Educational care / material explainer post ('how to keep gold from tarnishing', 'which metals are safe')"

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
5. Name every asset `F58-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F58
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

Teach a jewelry-care or materials lesson — how to clean gold at home, what "gold-plated vs vermeil vs PVD" means, which metals are safe for sensitive skin, how to store fine chains — with the LC piece as the example. Runs as Reels, carousels or Story tap-throughs; paid as MOF trust-builder.

### Why it works

- Positions LC as the authority in a category with purchase anxiety.
- Doesn't look like an ad; saves well; feeds retargeting pools.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0-3s | Text: "your gold jewelry is turning green because…" | VO |
| 3-12s | Diagram: plated layer vs PVD bonded | "plating sits on top; PVD bonds" |
| 12-20s | Care tips: what to avoid, how to clean | — |
| 20-25s | LC piece after 6 months | "any 7 for $85" |

### Hooks

- "why your gold jewelry turns green (it's not your skin)"
- "plated vs vermeil vs PVD in 20 seconds"
- "how to clean gold jewelry at home"
- "jewelry you should never wear in the pool (and what you can)"

### Production recipe

1. 5 lessons from support FAQs; each as 20s Reel + 6-card carousel.
2. Founder or CS lead on camera (F48 overlap) or faceless diagram.
3. Run paid only to engaged/visitor audiences (MOF).

### Existing bot prompt

```
Using only {{PDP_FACTS}} and generally accepted jewelry-care facts, write 6 educational posts (Reel script ≤60 words + 6-card carousel) on materials and care. No medical claims (e.g., "hypoallergenic") unless on PDP.
```

### Variants to test

- Reel vs carousel
- Founder vs faceless

## Reference examples

See [examples/README.md](examples/README.md) (7 posts). Top 5:

- @Halosznn_ (91L/38BM/16kV): Marek Health is hiring ‼️ 🎨 Graphic Designer 📍 Remote | Part-Time • Design static social media assets • Turn campaigns, educational content, promotions, into st — https://x.com/Halosznn_/status/2093427975350005795
- @lorenzo_pravata (36L/37BM/3kV): There are a ton of your customers who know nothing about your brand. That's what educational ads are for. Here's the first 20 seconds of one of ours. The produc — https://x.com/lorenzo_pravata/status/2095136884666052819
- @Bogzabs96 (17L/15BM/1kV): There are a ton of your customers who know nothing about your brand. That's what educational ads are for. Here's the first 20 seconds of one of ours. The produc — https://x.com/Bogzabs96/status/2096280202103927187
- @taye_afola19505 (20L/6BM/908V): Built a premium advertorial experience for @KYOM combining emotional storytelling, educational content, social proof, and conversion-focused design to transform — https://x.com/taye_afola19505/status/2077796327887450475
- @chioma_mmeje (14L/3BM/4kV): Depends on the smm and the brand’s persona -A cheeky, witty response IF you’re a witty smm and brand, and conditions are perfect. -Educational content, if their — https://x.com/chioma_mmeje/status/2082397955588301252
