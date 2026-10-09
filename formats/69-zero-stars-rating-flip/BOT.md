# BOT.md · generate a "Zero Stars rating flip ('5 stars from you / zero stars from them')"

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
5. Name every asset `F69-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F69
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

A two-line rating joke: you give it five stars, while an "enemy" (the shower, the pool, tarnish, the jealous friend) gives it zero. Social proof and a benefit packed into a meme-like card.

### Why it works

- A star rating is instantly readable; the twist makes people read the second line.
- It turns the product's durability into a joke the viewer gets.
- Cheap: one image and two lines.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| Static | Necklace on wet skin; top: "5 stars from you ⭐⭐⭐⭐⭐"; bottom: "Zero stars from the shower" | Primary text: "It's been through 400 showers and refuses to turn green." |

### Hooks

- "5 stars from you. Zero stars from your shower."
- "Zero stars from tarnish"
- "Zero stars from my sister (she wanted it first)"

### Production recipe

1. Write 10 "enemy" lines: shower, pool, chlorine, tarnish, the sister who borrows it.
2. Pair each with a real product photo.
3. Rotate weekly; the format fatigues fast.

### Existing bot prompt

```
Write 10 "5 stars from you / zero stars from ___" statics for LC: enemy, photo idea, 60-word primary text. Durability claims must match the PDP.
```

### Variants to test

- Enemy type
- Joke vs proof tone

## Reference examples

See [examples/README.md](examples/README.md) (2 posts). Top 5:

- @FedotOff90 (110L/208BM/9kV): 37 formats printing (with days active): AI podcast 280d, report card, iPhone Notes, text on skin, Reddit, cross-out, fake PDP, tier list, myth vs fact, zero sta — https://x.com/FedotOff90/status/2104949773539442831
- @Yannlce (3L/2BM/1kV): Same 40-format list (adds claymation, AI podcast). — https://x.com/Yannlce/status/2085017654364958737
