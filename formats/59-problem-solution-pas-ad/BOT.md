# BOT.md · generate a "Problem → agitation → solution → proof (4-part PAS ad, video or static)"

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
5. Name every asset `F59-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F59
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

The classic direct-response structure: name one specific pain so the right person thinks "that's me", agitate it (consequences, failed fixes), introduce the product as THE fix for that pain, close with specific proof and one CTA. One problem per ad — five benefits = five ads.

### Why it works

- Meets the viewer where they already are emotionally.
- Specific proof ("4.8★ from 12,000 reviews") beats generic.
- Scales cleanly: one ad per pain point.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0-5s | Close-up green ring mark on finger | "If your rings leave a green line, this is for you." |
| 5-20s | Taking jewelry off before every shower/pool; tangled tray | "I tried clear nail polish, 'hypoallergenic' plating… still green in a week." |
| 20-40s | LC piece in shower and pool | "This is what finally let me stop taking it off: 14K PVD, bonded not plated." |
| 40-60s | Real review count + any 7 for $85 | "[real rating/count]. Any 7 for $85." |

### Hooks

- "If your rings leave a green line, this is for you"
- "Tired of taking your necklace off every night?"
- "Still buying gifts she never wears?"

### Production recipe

1. List LC pain points from reviews; one ad per pain.
2. Cover-the-product test: first 15s must stand alone as a portrait of the problem.
3. Proof must be real and specific (review count/rating from the actual platform).

### Existing bot prompt

```
For each LC pain point in {{PAINS}}, write a 45-60s PAS script with the 4 timed phases; proof only from {{REAL_PROOF}}. Also a static version: headline (pain) / body (agitation) / product visual / CTA.
```

### Variants to test

- Pain point
- Video vs static
- Creator vs founder

## Reference examples

See [examples/README.md](examples/README.md) (2 posts). Top 5:

- @alexpagepilot (11L/19BM/1kV): Top 5 dropship formats: UGC problem/solution, "TikTok made me buy it", us vs them split, founder talking head (retargets 2-3x), text-overlay slideshow. — https://x.com/alexpagepilot/status/2099438014456045990
- @ayomikunszn (26L/5BM/1kV): Created these Weekender Bag ad concepts after studying what's working for leading DTC travel brands on Meta. Each creative focuses on a different conversion ang — https://x.com/ayomikunszn/status/2078116608069800131
