# BOT.md · generate a "Owned meme / niche page with product card ('bro vs me')"

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
5. Name every asset `F52-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F52
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

A brand-owned (disclosed) niche meme page posting relatable memes where the product appears as a small card/sticker in the image — distribution via shares, not ads.

### Why it works

- Memes travel; product card rides along.
- Separate from brand feed; tests humour angles cheaply.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| Post | Meme image (gift-giving humour) with small LC card in corner | Caption |
| Bio | "by Louise Carter" | Disclosure |

### Hooks

- "Him: what do you want for your birthday / Me:"
- "POV: you can shower in your jewelry now"

### Production recipe

1. Own the page openly ("by LC"); original memes only (no stolen images).

### Existing bot prompt

```
Write 20 gift/jewelry memes (top text/bottom text) with placement for a small LC card; original concepts only.
```

### Variants to test

- Meme style

## Reference examples

See [examples/README.md](examples/README.md) (8 posts). Top 5:

- @leonclipping (23L/25BM/1kV): Supercar "bro vs me" meme page with the app's speed card pasted on the photo: 2.2k followers, 736k likes, top post 1.4M views. — https://x.com/leonclipping/status/2107564115275501944
- @zackpaid (9L/20BM/2kV): 11 AI formats (agency pitch): native UGC, founder, claymation, Pixar 3D, jingle, screen recording, before/after, testimonial compilation, cinematic demo, mini-d — https://x.com/zackpaid/status/2085621175292670183
- @nicktheriot_ (219L/348BM/12kV): 2026 FB creative styles tier list: S = long primary text + organic image, LTO, UGC, VSL, reaction, news; A = demo, us vs them, testimonial, close-up, founder st — https://x.com/nicktheriot_/status/2108173638033871013
- @gauravsbuilding (62L/76BM/5kV): Attention all founders who don't know how to market your app, it's fr this easy. Create IG + TikTok pages for: 1. Your Brand 2. AI Influencer 3. Theme page Then — https://x.com/gauravsbuilding/status/2086540833717895480
- @cattybk (17L/15BM/886V): The most interesting companies being built right now aren't tech companies. They're ad agencies. If, like me, you want to be creative but you're not talented en — https://x.com/cattybk/status/2102397506843725858
