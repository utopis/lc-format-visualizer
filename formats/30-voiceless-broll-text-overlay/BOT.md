# BOT.md · generate a "Voiceless B-roll + text-overlay ad (mute-first)"

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
5. Name every asset `F30-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F30
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

No one talks. Product and lifestyle B-roll (pool, shower, beach, stacking hands) with the script delivered as short on-screen text beats, one per shot, plus music. The "mute text overlay" version of a winning message — cheap to scale into dozens of variants.

### Why it works

- Most feed video is watched muted; the message survives with sound off.
- Fast to scale: same footage, new text = new ad (@williamkast_ "clean, fast, easy to scale").
- A different production format = new Entity ID for a proven message.
- Short phrases highlighting key points read faster than VO.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0-2s | Macro: water droplets on gold herringbone | TEXT: "you can shower in this" |
| 2-4s | Hand in pool, rings | TEXT: "and swim in it" |
| 4-6s | Gym, sweat, huggies | TEXT: "and sweat in it" |
| 6-8s | 6-month-old necklace vs new | TEXT: "6 months later 👇" |
| 8-10s | Stack being built | TEXT: "any 7 for $85" |
| 10-12s | Logo/end card | TEXT: "Louise Carter · 14K PVD" |

### Hooks

- "you can shower in this"
- "things I never take off (and why)"
- "my jewelry rules after 30"
- "if your necklace turns green, read this"
- "the 7 pieces I live in"

### Production recipe

1. Build a B-roll library tagged by scene (water, gym, beach, office, stack, gift, macro).
2. Write text beats from a winning script: max 7 words per beat, 5-7 beats.
3. Edit in CapCut/Premiere template (9:16 + 4:5), safe-zone text, 1-2s per beat, licensed music.
4. Generate 10 variants by swapping beat 1 and the music.
5. Optional AI B-roll for scenes LC lacks — label if realistic people are AI.

### Existing bot prompt

```
Convert this winning LC ad script {{SCRIPT}} into 6 voiceless text-overlay beats (≤7 words each, sentence case, no emojis except 👇). For each beat pick a B-roll scene tag from {{LIBRARY_TAGS}}. Then write 10 alternative first beats (hooks) of ≤6 words. No claims beyond PDP.
```

### Variants to test

- Beat count 4 vs 7
- Music: trending vs calm
- Text style: native TikTok vs serif brand
- Real vs AI B-roll

## Reference examples

See [examples/README.md](examples/README.md) (19 posts). Top 5:

- @williamkast_ (227L/549BM/17kV): 5 formats that win in every account, each with a live Atria ad link: founder, yapper, AI educator, B-roll text overlay, long VSL. — https://x.com/williamkast_/status/2084298521251860579
- @williamkast_ (252L/400BM/13kV): Formats by funnel: TOF founder/yapper/AI animation/natives/3 reasons/voiceless overlay; MOF comment reply/testimonial mashup/text wall; BOF urgency statics. — https://x.com/williamkast_/status/2103910235005935644
- @williamkast_ (28L/34BM/3kV): 5 formats to test: founder talking head, voiceless B-roll text overlay, yapper (uncut), AI educational, camouflage static + long copy. — https://x.com/williamkast_/status/2078179704050246125
- @jhueri (25L/24BM/5kV): UGC formats ranked by conversion: talking head > hook-and-demo > skit … long text on screen last. — https://x.com/jhueri/status/2101054562253631699
- @alexpagepilot (11L/19BM/1kV): Top 5 dropship formats: UGC problem/solution, "TikTok made me buy it", us vs them split, founder talking head (retargets 2-3x), text-overlay slideshow. — https://x.com/alexpagepilot/status/2099438014456045990
