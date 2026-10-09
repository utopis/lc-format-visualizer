# BOT.md · generate a "Result reveal → expert stitch ('Y'all, this is my dad… after listening to this man. Just listen.')"

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
5. Name every asset `F96-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F96
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

Two layers in one vertical video: a relatable person shows a result on someone close (their dad, themselves on Day 1 vs Day 42) and credits "this woman/this man", then the video hands over to an expert clip that explains the mechanism. The personal result earns attention; the expert carries the explanation.

### Why it works

- Third-person proof ("my dad") feels less like bragging and more like a recommendation.
- "Just listen" sets up the expert as a discovery, not an ad.
- Stitch/duet grammar is native to TikTok and Reels.
- The expert clip can be reused under many result intros.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0:00-0:08 | Daughter holds up a photo of mom's green-stained wrist, then mom now wearing an LC stack in the pool | "Y'all, this is my mom's wrist last summer. This is her now. Just listen to this woman." |
| 0:08-0:45 | Stitched clip: LC jeweller or founder at the bench | "Most gold jewelry is plated: a layer thinner than a hair over brass. We bond 14K PVD to steel…" |
| 0:45-0:55 | Back to daughter + CTA | "She hasn't taken it off in a year. Link's below." |

### Hooks

- "Y'all, this is my mom's wrist last summer. Just listen."
- "Day 1 vs day 365 of never taking it off."
- "I didn't believe this woman until I tried it."

### Production recipe

1. Film 1 expert clip (founder or jeweller) explaining PVD in 30-40 s.
2. Collect real customer result intros (with consent) and stitch each onto the expert clip.
3. Keep the result honest: time worn, what she did (showers, pool).

### Existing bot prompt

```
Write 5 result-reveal intros (≤8 s each) from real LC customer stories {{STORIES}} and one 35-second expert explanation of bonded 14K PVD for the stitch. No exaggerated results.
```

### Variants to test

- Third-person vs self
- Expert = founder vs jeweller

## Reference examples

See [examples/README.md](examples/README.md) (4 posts). Top 5:

- @valentinszabadi (49L/58BM/3kV): How to iterate a winning creative as a strategist? Easy. - Change the talent - Change the format - UGC, VSL, Stitch, Street Interview, Podcast, AI slop, Pixar,  — https://x.com/valentinszabadi/status/2079614879309185498
- @EvoBradley (18L/31BM/1kV): The #1 most viral format in entire ugc industry. Here are a few hits from past few days… Let me break it down for you; &gt; Stitch format: inherits trust and re — https://x.com/EvoBradley/status/2082416231353590174
- @nicktheriot_ (29L/23BM/3kV): Begging every brand owner to stop this mistake: Sitting on 50 pieces of B-roll footage… And launching zero variations of it. Do THIS instead: ⦁ Find one hook →  — https://x.com/nicktheriot_/status/2085544771150352632
- @CalixAVelarde (4L/1BM/461V): this girl-in-car ai ugc format is actually insane this entire clip is ONE generation i didn't stitch anything together. dropped the script in and it came back t — https://x.com/CalixAVelarde/status/2083448214431351004
