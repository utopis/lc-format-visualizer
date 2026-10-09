# BOT.md · generate a "AI object-head micro-drama (talking-fruit-style soap opera)"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 60-120s episodes, 1080x1920), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@seergioo_gil](https://x.com/seergioo_gil/status/2089472288001347867) · Talking-fruit micro-drama: a broccoli-head character and a tomato-head businessman in suits in a barbershop or office, then an apple and an eggplant character. It is a 1-minute soap plot acted out by food characters.
- Example: [@bmx_ai13](https://x.com/bmx_ai13/status/2103701345563812177) · AI micro-drama production skill (script → storyboard → consistent characters) — tool promo.
- Example: [@CodewizzyX](https://x.com/CodewizzyX/status/2096695495590568092) · THESE VIRAL "FRUIT DRAMA" AI VIDEOS AREN'T RANDOM - THERE'S AN ACTUAL FORMULA AND IT'S FREE TO COPY No camera, no writers room, no editing. Absurd fru
- Example: [@SmartEye_ADSpy](https://x.com/SmartEye_ADSpy/status/2082748308293071171) · 🔥July 30 Global Micro Dramas & AI Micro Dramas: Multiple NetShort Horror Campus AI Dramas Secure Chart Rankings; Fruit-Themed AI Micro Drama Jumps to 
- Example: [@SmartEye_ADSpy](https://x.com/SmartEye_ADSpy/status/2087111287184728470) · Top 3 Claim Over 40% of Global Market Revenue; Breakout AI Micro Drama App VibeShort Cracks the Chart Market Revenue Is Highly Concentrated: In H1 202
- Example: [@SmartEye_ADSpy](https://x.com/SmartEye_ADSpy/status/2087810501686481034) · Top 3 Contribute Over 40% of Market Revenue | Maiya's NetShort Cracks the Top 3 In H1 2026, the Top 20 Chinese micro drama apps in global markets gene

### Live paid ads in this format (1 in [adlibrary/](adlibrary/README.md), longest-running first)

- **Resilia · Blood Sugar Wellness: “I'm exhausted. It's been getting knocked on all day, every day, for 30…”** (1 days live): Opens: “I'm exhausted. It's been getting knocked on all day, every day, for 30 years.”

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| 0-5s | Object-head characters (fruit/gem heads on human bodies) mid-drama | "You gave HER the necklace?" |
| 5-60s | Soap plot: love, betrayal, twist | Dialogue with lip-sync |
| 60-90s | Cliffhanger | "Part 2" |
| Placement | Product is a prop worn by a character | One mention max |

### Prompts

**Midjourney**

```
hyperreal 3D character, a man with a broccoli head wearing a navy suit in a barbershop, cinematic soft light, Pixar realism --ar 9:16
```

**Veo 3 / Kling**

```
the broccoli-head man [ref] arguing with a tomato-head woman in an office, dramatic, lip-sync "[line]", 8s
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
- [ ] Files named `F42-<concept>-<variant>`; tracking tag `utm_content=F42-<concept>-<variant>`.
- [ ] Avoid: Serial formats need consistent characters; save reference images.
- [ ] Avoid: This builds an organic page; it is not a direct-response ad.

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
5. Name every asset `F42-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F42
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

Serialized 1-2 min AI soap operas where characters are objects/fruit heads on human bodies (love, betrayal, plot twist). Massive organic views category; product placement is the play for a brand.

### Why it works

- Serialized cliffhangers drive follows and binge views.
- Novel aesthetic; huge category per claims.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0-5s | Fruit-head characters argue | Plot hook |
| 5-60s | Drama, twist | Lip-synced dialogue |
| 60-70s | Cliffhanger; LC piece as plot device | "Part 2" |

### Hooks

- "She found the necklace in his car…"
- "The ring that ruined the wedding (part 1)"

### Production recipe

1. Only as an experiment on a separate page; consistent characters via reference images; label AI.

### Existing bot prompt

```
Write a 6-episode outline for an AI object-head soap opera where an LC necklace is the plot device (heirloom, gift, mystery). Each episode: 60s, cliffhanger, no disparagement.
```

### Variants to test

- Characters
- Episode length

## Reference examples

See [examples/README.md](examples/README.md) (6 posts). Top 5:

- @bmx_ai13 (44L/6BM/1kV): AI micro-drama production skill (script → storyboard → consistent characters) — tool promo. — https://x.com/bmx_ai13/status/2103701345563812177
- @seergioo_gil (9L/12BM/6kV): Talking-fruit micro-dramas (+20B views claimed): 1-2 min love/betrayal story, fruit heads on human bodies, AI lip-sync, plot twist. Tool promo. — https://x.com/seergioo_gil/status/2089472288001347867
- @CodewizzyX (32L/22BM/3kV): THESE VIRAL "FRUIT DRAMA" AI VIDEOS AREN'T RANDOM - THERE'S AN ACTUAL FORMULA AND IT'S FREE TO COPY No camera, no writers room, no editing. Absurd fruit soap op — https://x.com/CodewizzyX/status/2096695495590568092
- @SmartEye_ADSpy (3L/0BM/242V): 🔥July 30 Global Micro Dramas & AI Micro Dramas: Multiple NetShort Horror Campus AI Dramas Secure Chart Rankings; Fruit-Themed AI Micro Drama Jumps to No.3 on Ti — https://x.com/SmartEye_ADSpy/status/2082748308293071171
- @SmartEye_ADSpy (3L/0BM/158V): Top 3 Claim Over 40% of Global Market Revenue; Breakout AI Micro Drama App VibeShort Cracks the Chart Market Revenue Is Highly Concentrated: In H1 2026, the Top — https://x.com/SmartEye_ADSpy/status/2087111287184728470
