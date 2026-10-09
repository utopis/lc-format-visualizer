# BOT.md · generate a "Talking product (AI-animated product as narrator)"

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
5. Name every asset `F41-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F41
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

The product itself gets eyes/mouth (AI animation) and speaks to camera: "I'm the necklace she wore in the ocean 47 times." Personification makes the mechanism a story.

### Why it works

- Novelty stops the scroll; product is literally the protagonist.
- Ran 183 days for a hair brand (@FedotOff90).

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0-3s | Animated LC necklace on vanity | "Hi. I'm the necklace she refuses to take off." |
| 3-15s | Cuts to necklace "experiencing" shower, pool | "Shampoo? Fine. Chlorine? Fine. 14K PVD, baby." |
| 15-20s | Stack of friends | "Bring my friends. Any 7 for $85." |

### Hooks

- "I'm the necklace she never takes off"
- "Day 180 on her neck. Still gold."

### Production recipe

1. Generate base product shots; animate with an image-to-video model + lip-sync voice.
2. Keep voice consistent (persona); label as AI animation.
3. 15-25s.

### Existing bot prompt

```
Write 5 first-person scripts (≤55 words) for an animated LC necklace/ring narrator with a witty, warm persona; include one PDP fact each.
```

### Variants to test

- Character voice
- Product

## Reference examples

See [examples/README.md](examples/README.md) (8 posts). Top 5:

- @FedotOff90 (25L/20BM/3kV): Hair-thinning ads 180+ days: persona page with AI-animated shampoo bottle (199 ads, 183d), pool side-by-side test (215d), "don't put this on your face" UGC (309 — https://x.com/FedotOff90/status/2097761790621057320
- @Ecombos_Ai (22L/14BM/793V): AI ecom format tiers: S = AI animation, AI singing, AI native statics → advertorial; A = AI before/after, AI podcast, talking product; F = AI avatar reading scr — https://x.com/Ecombos_Ai/status/2107157131010965744
- @koloveski (183L/112BM/191kV): 🚨 I made a fully animated product video for Amazon without touching a traditional editing workflow. I used Dreamina Octo as my AI creative partner, and it took  — https://x.com/koloveski/status/2076868032002150833
- @AgentOpusAI (16L/22BM/6kV): Making an animated product ad used to be a project. Making them at scale used to take a month. We took down both. Full tutorial 👇 https://t.co/6pMG6dfEhs https: — https://x.com/AgentOpusAI/status/2082224622255374394
- @raph_guilhem (8L/5BM/1kV): Our best clients are generating their highest performing Meta ads with one format: animated product videos. Origami style. Voxel. Minecraft. Pixar. Paper craft. — https://x.com/raph_guilhem/status/2076713068982100369
