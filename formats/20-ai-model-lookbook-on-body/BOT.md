# BOT.md · generate a "AI model lookbook / on-body try-on (from real product photos)"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: Image set 1080x1350 (6-10 looks) or a 15s try-on clip), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@KarinaRed123](https://x.com/KarinaRed123/status/2099477629078307041) · A photoreal AI runway shot: a model in a velvet mini-dress and thigh-high boots on a lit catwalk with an audience. It is an AI "photoshoot" used as an on-body lookbook image.
- Example: [@MimiTheDesigner](https://x.com/MimiTheDesigner/status/2080184317771227394) · Fashion: every model/dress in video AI-generated; boutiques advertising this way.
- Example: [@girlincrypto007](https://x.com/girlincrypto007/status/2077765449371025600) · You need the right AI model for every task so you don’t burn through your limits too fast 👀 My stack is simple: > @claudeai Fable - for building a por
- Example: [@MirrAIHQ](https://x.com/MirrAIHQ/status/2085708930588557789) · Every fashion brand has a folder of flat product photos. Watch what happens when you run a whole catalog through MirrAI Studio 👇 On-model try-ons for 

### Live paid ads in this format (1 in [adlibrary/](adlibrary/README.md), longest-running first)

- **Quality of Life Labs: Model-holding-bottle DCO (Quality of Life Labs, 5 headlines)** (583 days live): The same blonde model holding the bottle across 5 headline variants: "Outsmart the signs of skin aging", "Clinically-tested. Skin approved.", "Transform your skin diet". 35 media each.

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| Look 1 | AI model in a lifestyle scene (beach, office, wedding) wearing the EXACT product composited from real product photos | Caption: occasion + piece name |
| Looks 2-6 | Different ages, skin tones and settings, same product | "wore it to work / to the beach / to her wedding" |
| Clip version | 15s photoreal try-on: hands fasten the necklace, mirror glance | Text: "how it looks on" |

### Prompts

**Nano Banana / GPT-image (edit mode)**

```
Place the exact necklace from image 1 on the woman in image 2, keep chain length, pendant size and gold tone identical, natural shadow on skin, do not change the jewelry design
```

**Kling / Seedance (clip)**

```
photoreal UGC, a woman in a bright bathroom fastening a thin gold necklace, glancing in the mirror, handheld phone footage, 5s, 9:16
```

### QA checklist (all must pass before hand-off)

- [ ] Hook lands in the first 1.5 s (video) or is readable at thumbnail size (static / slide 1).
- [ ] Removal test: delete the product from the script. If it still makes sense, rewrite so the product is the payoff.
- [ ] Matches the reference structure (same beat order and length band) before any creative twist.
- [ ] Uses only real product imagery for the product; AI is for backgrounds, characters or b-roll, and is disclosed where required.
- [ ] Every claim is on the brand's approved-claims list (PDP); no invented stats, reviews, doctors or customers.
- [ ] Captions burned in and inside the safe zone; sound-off still understandable.
- [ ] One clear CTA that matches the landing page offer.
- [ ] Three hook variants delivered for the same body (test hooks, not whole new ads).
- [ ] Files named `F20-<concept>-<variant>`; tracking tag `utm_content=F20-<concept>-<variant>`.
- [ ] Avoid: AI must not change the product's size, finish or design; check every image against the real piece.
- [ ] Avoid: Label AI-generated models where required.
- [ ] Avoid: The featured example is a fashion AI photoshoot; for jewelry, close crops of neck and wrist matter more than full-body runway shots.

<!-- QUICKSTART:END -->

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
5. Name every asset `F20-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F20
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

Diverse models wearing the exact piece in lifestyle scenes (beach, office, wedding); or a 15s photoreal UGC try-on clip generated from the product photo (prompt structure from [@Arina_hoqe](https://x.com/Arina_hoqe/status/2095071815483986241): PRODUCT · DURATION exactly 15s · STYLE photorealistic UGC · scene beats · camera · audio).

### Production recipe

Nano Banana / GPT Image edit with the real product photo as reference; QC each image against the real piece (chain link pattern, clasp, width) — reject any hallucinated detail; real photos for PDP hero.

## Reference examples

See [examples/README.md](examples/README.md) (9 posts). Top 5:

- @rirahcreates (70L/53BM/8kV): AI fashion content: lookbooks, campaign images. — https://x.com/rirahcreates/status/2106081343566381455
- @Arina_hoqe (42L/36BM/4kV): Full prompt for 15s photoreal UGC watch ad from your own product photo ('Running Late'). — https://x.com/Arina_hoqe/status/2095071815483986241
- @MimiTheDesigner (31L/13BM/2kV): Fashion: every model/dress in video AI-generated; boutiques advertising this way. — https://x.com/MimiTheDesigner/status/2080184317771227394
- @KarinaRed123 (0L/0BM/0V):  — https://x.com/KarinaRed123/status/2099477629078307041
- @girlincrypto007 (89L/9BM/4kV): You need the right AI model for every task so you don’t burn through your limits too fast 👀 My stack is simple: > @claudeai Fable - for building a portfolio, la — https://x.com/girlincrypto007/status/2077765449371025600
