# BOT.md · generate a "Customer-photo hashtag UGC turned into Story & retargeting ads"

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
5. Name every asset `F87-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F87
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

Run a branded hashtag ("#LCinTheOcean"), collect customer photos with explicit rights, and turn them into Story ads and retargeting carousels, with the customer's handle shown. Real wearers in real places beat studio shots for warm audiences.

### Why it works

- Real customers in the wild are the strongest proof for a durability claim.
- A constant supply of fresh creative fights fatigue.
- Featuring customers builds community and more submissions.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| Story ad | Customer selfie in the sea, handle tag | "@handle · 4 months, still gold" |
| Carousel | 6 customer photos | "Where our stacks have been" |

### Hooks

- "Where have your LC pieces been?"
- "Real customers, real oceans"

### Production recipe

1. Launch the hashtag on packaging and in the post-purchase email.
2. Collect written usage rights (e.g. reply "#yesLC").
3. Refresh the retargeting carousel weekly.

### Existing bot prompt

```
Write a hashtag launch kit for LC: hashtag, packaging insert copy, rights-request DM, 3 Story ad templates and 1 carousel template using customer photos.
```

### Variants to test

- Story vs carousel
- With vs without handle

## Reference examples

See [examples/README.md](examples/README.md) (5 posts). Top 5:

- @huejewellers (0L/0BM/0V):  — https://x.com/huejewellers/status/2099792841115386168
- @NahFlo2n (169L/147BM/12kV): $74k/mo from AI UGC avatars (promo). — https://x.com/NahFlo2n/status/2082463906694648266
- @paula_bearr (63L/125BM/2kV): If you ever run out of things to post on Instagram, save this. Here’s a general content idea bank you can tailor to almost any brand: REELS / SHORT-FORM VIDEO • — https://x.com/paula_bearr/status/2107067561619693949
- @lifemaximised (17L/12BM/1kV): Google Ads funnels are one of the biggest untapped opportunities in eCom right now. A huge portion of your GADs performance comes down to JUST optimizing the la — https://x.com/lifemaximised/status/2086552616679756212
- @ceorazwan (3L/0BM/339V): A new EU law is about to change how AI-generated content can be used in ads and if you're running AI UGC, this affects you. Starting August 2, 2026, the EU AI A — https://x.com/ceorazwan/status/2079691741666377989
