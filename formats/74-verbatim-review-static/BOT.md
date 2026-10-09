# BOT.md · generate a "'The Verbatim': one raw customer review as the whole creative"

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
5. Name every asset `F74-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F74
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

One unedited customer review, typos and all, set in large type (or as a screenshot of the review), with only a small logo and product photo. The brand steps back: "this review says it better than we could."

### Why it works

- Raw voice is more believable than polished copy.
- One specific story beats a star average.
- Fastest possible production: choose a review, set the type.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| Static | Big serif quote from a real verified review about months of ocean wear | Primary: "This review says it better than we can." |

### Hooks

- "This review says it better than we could"
- "Read what Jess wrote after 4 months"
- "We didn't write this. Jess did."

### Production recipe

1. Export the top 50 reviews; tag them by theme (ocean, shower, gift, compliments).
2. Get consent if a name or photo is used; keep spelling as written.
3. Make 10 statics; rotate themes.

### Existing bot prompt

```
From {{REVIEWS}}, pick the 10 most specific reviews (time worn, situation, emotion). For each: verbatim quote (unaltered), visual idea, 1-line primary text.
```

### Variants to test

- Typeset vs screenshot
- Short vs long review

## Reference examples

See [examples/README.md](examples/README.md) (5 posts). Top 5:

- @FedotOff90 (17L/18BM/3kV): Rebuilt the formats list with proof: 30-day survival column = "this works" bar; copy the structure, not the words. — https://x.com/FedotOff90/status/2100948331136782532
- @FedotOff90 (110L/208BM/9kV): 37 formats printing (with days active): AI podcast 280d, report card, iPhone Notes, text on skin, Reddit, cross-out, fake PDP, tier list, myth vs fact, zero sta — https://x.com/FedotOff90/status/2104949773539442831
- @williamkast_ (252L/400BM/13kV): Formats by funnel: TOF founder/yapper/AI animation/natives/3 reasons/voiceless overlay; MOF comment reply/testimonial mashup/text wall; BOF urgency statics. — https://x.com/williamkast_/status/2103910235005935644
- @williamkast_ (214L/374BM/13kV): Best creative formats on Meta for each funnel stage: TOF: - Founders Ad - UGC - AI Animation - Yapper Ad - Native Statics - Long form VS - Podcasts - 3 reasons  — https://x.com/williamkast_/status/2077818070580548013
- @Ecombos_Ai (46L/80BM/9kV): Winning ad formats before AI: - Real UGC testimonials - Product demos - Before/after transformations - Carousels - Static benefit/review ads Winning ad formats  — https://x.com/Ecombos_Ai/status/2099559565721206890
