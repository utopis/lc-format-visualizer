# BOT.md · generate a "Testimonial mashup (real customer clip montage)"

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
5. Name every asset `F40-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F40
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

A fast montage of 6-12 real customers each saying one line (selfie video, review screenshot, unboxing) stitched into a 20-40s ad. Volume of real voices = proof.

### Why it works

- Social proof at scale; MOF retargeting staple (@williamkast_).
- Many faces → broad identification across age/skin tone.
- Uses content LC can collect via post-purchase flows.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0-3s | Rapid 3 faces | "I shower in it" / "6 months" / "still gold" |
| 3-25s | 8 more one-liners with name/city captions | Real audio |
| 25-30s | Review count + offer | "300,000+ customers" |

### Hooks

- "We asked customers one question: do you ever take it off?"
- "300,000 people can't be wrong (here are 12)"

### Production recipe

1. Omnisend post-purchase flow (day 30): "Send us a 10s selfie video answering X → $15 credit" with usage-rights consent.
2. Same question for everyone → clean edit.
3. Disclose incentive where required ("customers received store credit").

### Existing bot prompt

```
From these customer clip transcripts {{CLIPS}} pick 10 one-liners (≤8 words) that together cover: waterproof, compliments, gift, value, longevity. Order for a 30s montage with an opening 3-clip hook.
```

### Variants to test

- Question asked
- Length 15 vs 30s

## Reference examples

See [examples/README.md](examples/README.md) (5 posts). Top 5:

- @williamkast_ (252L/400BM/13kV): Formats by funnel: TOF founder/yapper/AI animation/natives/3 reasons/voiceless overlay; MOF comment reply/testimonial mashup/text wall; BOF urgency statics. — https://x.com/williamkast_/status/2103910235005935644
- @zackpaid (9L/20BM/2kV): 11 AI formats (agency pitch): native UGC, founder, claymation, Pixar 3D, jingle, screen recording, before/after, testimonial compilation, cinematic demo, mini-d — https://x.com/zackpaid/status/2085621175292670183
- @williamkast_ (12L/14BM/967V): 15 formats to repackage winners into (scaled to $30k/day on 3-4 angles): founder, yapper, AI animation, voiceless overlay, carousel, reply ad, text wall, review — https://x.com/williamkast_/status/2083616523134841035
- @nicktheriot_ (219L/348BM/12kV): 2026 FB creative styles tier list: S = long primary text + organic image, LTO, UGC, VSL, reaction, news; A = demo, us vs them, testimonial, close-up, founder st — https://x.com/nicktheriot_/status/2108173638033871013
- @ashvinmelwani (31L/7BM/12kV): One ad format that will always crush is a mashup of raw customer testimonials. The fastest way to get this content for us was to post in our 117K+ member Facebo — https://x.com/ashvinmelwani/status/2105710765151752218
