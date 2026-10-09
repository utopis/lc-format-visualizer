# BOT.md · generate a "Green-screen personal story / long-form yapper (brand appears late)"

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
5. Name every asset `F29-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F29
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

A creator talks straight to camera (often over a green-screen background of a relevant image — a Reddit post, a photo, a text, a map) telling a personal story in depth for 30-90 seconds; the product is not shown or named until late, when it arrives as the natural resolution. Uncut "yapper" energy; no polished B-roll.

### Why it works

- Feels like content, not an ad, so attention is earned before the pitch (@therahulissar).
- Viewers who stay through a long story arrive at the CTA with high intent.
- Uncut yapping builds trust "like a friend telling you about something" (@williamkast_).
- The execution variables (creator, pacing, captions, hook) make or break it — the same angle can flop or spend $750k (@StefanGeorgi).

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0-3s | Creator in front of green-screen image (e.g. photo of a beach / Reddit post "AITA for wearing my jewelry in the pool?") | Hook line spoken immediately, captions on |
| 3-30s | Story: setup + stakes, personal details, light jump cuts | No product, no brand |
| 30-45s | Turn: "and that's when my friend showed me…" — background switches to LC piece | First product mention |
| 45-60s | Proof: shows the piece on her, tells the after | "I haven't taken it off since" |
| 60-70s | Soft CTA | "They do any 7 for $85, link's there" |

### Hooks

- "I lost my grandmother's ring in a hotel pool and I'm still not over it"
- "Storytime: I was the bridesmaid with the green neck in every photo"
- "AITA for wearing my jewelry in the ocean?" (Reddit post on green screen)
- "I'm allergic to basically every cheap earring — here's what finally worked"
- "My husband bet me $100 this necklace would tarnish in a month"

### Production recipe

1. Mine 30 real stories from reviews/DMs/post-purchase survey ("tell us the moment you knew").
2. Brief creators with the story beats, not a script; require first line within 1s and product not before 50% of runtime.
3. Green-screen backgrounds: Reddit-style post (written by LC, clearly not a fake real post — or a real one with permission), beach photo, wedding photo, text thread.
4. Edit lightly: jump cuts only, captions, no music for first 10s.
5. Make 3 hooks per story (first 3s swapped).

### Existing bot prompt

```
From these LC reviews {{REVIEWS}}, extract 10 personal stories with stakes (loss, embarrassment, gift, allergy, travel). For each write: a spoken first line (≤14 words, mid-action), 4 story beats, the moment the piece enters, the after, and a soft CTA. Product must not appear before 50% of runtime. Keep claims to PDP wording.
```

### Variants to test

- Green screen vs plain wall
- 45s vs 90s
- Story type (loss / embarrassment / bet / gift)
- Product reveal at 40% vs 70%

## Reference examples

See [examples/README.md](examples/README.md) (19 posts). Top 5:

- @williamkast_ (227L/549BM/17kV): 5 formats that win in every account, each with a live Atria ad link: founder, yapper, AI educator, B-roll text overlay, long VSL. — https://x.com/williamkast_/status/2084298521251860579
- @StefanGeorgi (220L/280BM/39kV): Stefan Georgi: yapper-style winner ~$750k spend in <3 weeks on an angle the brand said "doesn't work"; double 80/20 rule (80% proven formats). — https://x.com/StefanGeorgi/status/2090446853565296658
- @danclipping (43L/52BM/6kV): Manifestation app 250K downloads from 2 formats: reaction + app demo, and the yap format (1.3M views, strong hook). Comment-gated guide. — https://x.com/danclipping/status/2078147137049923751
- @adamtaylorl (36L/36BM/3kV): Dead in 2026: polished studio, "hey guys" UGC, discount statics, founder-story VSLs. Printing: ugly advertorial statics, long-form yapper, comment-reply hooks,  — https://x.com/adamtaylorl/status/2086814826177679660
- @williamkast_ (28L/34BM/3kV): 5 formats to test: founder talking head, voiceless B-roll text overlay, yapper (uncut), AI educational, camouflage static + long copy. — https://x.com/williamkast_/status/2078179704050246125
