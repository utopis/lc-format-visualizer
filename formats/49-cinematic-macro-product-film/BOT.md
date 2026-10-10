# BOT.md · generate a "Cinematic macro product film (15s, no dialogue)"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 10-15s, no dialogue, 1080x1920 and 1080x1350), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@prompthanem](https://x.com/prompthanem/status/2108225912957186085) · An AI-generated cinematic jewelry commercial: a macro of an emerald, a velvet box opening, white-gloved hands lifting the ring, a hand reveal, and the box closing for the final shot. No people, just light, texture and slow camera moves.
- Example: [@LachezarVoynov](https://x.com/LachezarVoynov/status/2082493438520439242) · ASMR ads like this one literally print money for products that don’t require too much education. As an agency, we always try to focus on heavy TOF ads
- Example: [@rirahcreates](https://x.com/rirahcreates/status/2086324982892605618) · AI formats to watch: Pixar storytelling, claymation, timeline/notes videos, cinematic product ads, virtual influencers, 3D product animation, AI docum
- Example: [@Balentin_J](https://x.com/Balentin_J/status/2080581505441480774) · &gt; What if a familiar kitchen moment could become a product story? 🥤 I explored that idea by reimagining the Vitamix A3500 as the centerpiece of a f
- Example: [@alohaproxy](https://x.com/alohaproxy/status/2104226192085987378) · Every founder wants to see their product here👑 Ankon AI is currently at HOF on HopUp. I thought that deserved more than a leaderboard card......So I t
- Example: [@gptproto](https://x.com/gptproto/status/2077709443165507626) · Can AI create luxury brand advertisements? This fragrance commercial was created with AI. Workflow: 🖼️ GPT Image 2 → storyboard &amp; visual concept 🎬
- Example: [@Imagvio_AI](https://x.com/Imagvio_AI/status/2088473026098774492) · Your weekend challenge starts now. 🎬 We created this entire cinematic product ad with Imagvio AI — from the luxury store to the product reveal, ingred

### Live paid ads in this format (1 in [adlibrary/](adlibrary/README.md), longest-running first)

- **Solvaderm Skin Care: Clean product-on-podium static (Solvaderm, "Unlock your best skin yet")** (690 days live): A pastel 3D podium, a tall serum bottle, the headline "Unlock Your Best Skin Yet!" and a sub-line. DCO.

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| 0-3s | Extreme macro of the chain links, light sweeps across | No text, or brand only |
| 3-7s | Water droplets running off the pendant, slow motion | - |
| 7-11s | Piece on skin, hand movement | - |
| 11-15s | Hero shot on a dark surface, logo | "[Brand]. 14K PVD." |

### Prompts

**Real shoot**

```
100mm macro lens, 4K 60-120fps, black acrylic surface, one hard key light + a moving strip light, spray bottle for droplets.
```

**AI (Seedance / Veo)**

```
luxury jewelry commercial, extreme macro of a thin gold chain, a soft light sweep across the links, water droplets, black background, slow motion, 5s
```

**Sound**

```
Subtle whoosh + chime library sounds, no music or a minimal pulse.
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
- [ ] Files named `F49-<concept>-<variant>`; tracking tag `utm_content=F49-<concept>-<variant>`.
- [ ] Avoid: AI jewelry often invents detail; only use AI for environments, keep the product real.
- [ ] Avoid: Pure beauty shots work as retargeting, not as cold hooks; test with a text hook.

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
5. Name every asset `F49-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F49
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

A 6-15s premium macro film: water droplets on 14K gold, slow-motion splash, light sweep — no dialogue, one text line, logo. YouTube/CTV and solution-aware audiences.

### Why it works

- Premium perception; works sound-off.
- YouTube solution-aware format per one operator; 6s bumper cut.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0-3s | Macro water drop on herringbone | Sound design |
| 3-8s | Necklace through splash, slow-mo | — |
| 8-12s | On skin in sunlight | Text: "Shower-proof 14K PVD" |
| 12-15s | Logo + any 7 for $85 | — |

### Hooks

- Visual hook only: water hitting gold
- "Built for water."

### Production recipe

1. Shoot macro with phone macro lens + water spray, or AI image-to-video from real product photos (don't alter product).
2. Cuts: 15s, 6s bumper, 9:16/16:9.

### Existing bot prompt

```
Write a 15s shot list + AI video prompts for an LC macro film from these product photos {{IMAGES}}; preserve exact product design.
```

### Variants to test

- Real vs AI
- 15s vs 6s

## Reference examples

See [examples/README.md](examples/README.md) (12 posts). Top 5:

- @nicktheriot_ (219L/348BM/12kV): 2026 FB creative styles tier list: S = long primary text + organic image, LTO, UGC, VSL, reaction, news; A = demo, us vs them, testimonial, close-up, founder st — https://x.com/nicktheriot_/status/2108173638033871013
- @zackpaid (9L/20BM/2kV): 11 AI formats (agency pitch): native UGC, founder, claymation, Pixar 3D, jingle, screen recording, before/after, testimonial compilation, cinematic demo, mini-d — https://x.com/zackpaid/status/2085621175292670183
- @rirahcreates (18L/7BM/454V): AI formats to watch: Pixar storytelling, claymation, timeline/notes videos, cinematic product ads, virtual influencers, 3D product animation, AI documentary. — https://x.com/rirahcreates/status/2086324982892605618
- @lifemaximised (12L/9BM/990V): Highest-ROAS YouTube ad anatomy: outcome text hook, 9-shot claymation villain arc, CTA last 3s, non-discount offer, custom-intent audiences, 6s Shorts bumper. — https://x.com/lifemaximised/status/2087086851148660816
- @lifemaximised (8L/5BM/1kV): Top 4 YouTube ad formats by awareness: claymation 9-shot (unaware), hybrid AI UGC (problem-aware), 15s cinematic no-dialogue product film (solution-aware), 6s S — https://x.com/lifemaximised/status/2094059955472990517
