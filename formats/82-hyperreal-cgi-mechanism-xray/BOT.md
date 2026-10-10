# BOT.md · generate a "Hyperreal CGI mechanism / 'x-ray' shot (inside the material) + villain monologue"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 15-25s, 1080x1920, CGI + real product end), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@FedotOff90](https://x.com/FedotOff90/status/2106401392374186396) · A woman in a white coat with a stethoscope talking to camera, with a hook caption ("Chronic bad breath has 3 layers!") pinned on top for the whole video and cutaways to mouth CGI.
- Example: [@adamtaylorl](https://x.com/adamtaylorl/status/2102759896789713340) · 3. The "This is why" cutaway A 3D inside-the-body visual stops the scroll, and "this is why" promises an answer they've never heard. Show what's happe
- Example: [@adamtaylorl](https://x.com/adamtaylorl/status/2092576938309386363) · If you're in ecom Pay the f*ck attention to what Lymphoria is doing with their creative right now 4,000+ ads live. This will be taught in every guru c
- Example: [@D_Only_Aji](https://x.com/D_Only_Aji/status/2091972209178796230) · Just wrapped up this 3D animated performance ad for Rejuvenate, built from the ground up using an AI-assisted production workflow. From creative direc
- Example: [@FedotOff90](https://x.com/FedotOff90/status/2072477830861254686) · 66-day cartoon AI ad: people know it is AI and still buy; 278 AI animation board.
- Example: [@HikeMyTraffic](https://x.com/HikeMyTraffic/status/2082004242471268500) · Team HikeMyTraffic created this stunning Wilkinson Sword Hydro 5 razor commercial entirely with AI. 🎬AI Product Videos | CGI Ads | Social Creatives Hi

### Live paid ads in this format (4 in [adlibrary/](adlibrary/README.md), longest-running first)

- **StellaLife, Inc.: Clinical CGI explainer (mouth lesions)** (1189 days live): "Suffering from mucositis? Natural relief from lesions and inflammation…" A clinical 3D mouth animation with captions. 98 s.
- **Deborah Hayes: "Spa treatments for belly fat don't work" two-layer explainer** (286 days live): "Spa treatments for belly fat don't work. And there's a scientific reason why… I did six spa sessions… $1,200… Your belly fat has two types of fat… these only work on surface fat." UGC plus a medical-paper insert plus CGI. 126 s.
- **Petra Weber: "Swiss urologist challenge" CGI x-ray explainer (prostate)** (265 days live): "Swiss urologist challenge: if you're not sleeping through the night within five days using this method, your prostate problems aren't what you think… Austrian urologists found… inflamed prostate tissue blocks the active ingredients…" CGI anatomy plus a plant-
- **Dr. Lisa Downing: Pixar-style organ-and-pills CGI (kidneys)** (217 days live): Pixar-style 3D characters around organs and a pill bottle, with captions like "That foam was protein leaking through stressed kidneys… By day 15…" 123 s.

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| 0-2s | Extreme macro CGI: the camera dives into a chain link until the metal layers are visible like geological strata | Villain VO (gravelly): "I'm Tarnish. I live on cheap jewellery." |
| 2-6s | Cutaway: a cheap plated chain under shower water; the thin top layer flakes off, grey metal shows through | "A little water. A little sweat. I eat the plating right off." |
| 6-12s | Same water hits the PVD chain; droplets bead and roll off; a glowing bonded layer stays intact | Villain, confused: "Wait... why can't I get in?" |
| 12-16s | Labelled cross-section: stainless steel core / bonded PVD gold layer | Narrator (warm): "14K PVD gold, bonded to stainless steel. Nothing to flake." |
| 16-20s | Real product footage: a hand in the sea wearing the stack | Villain, defeated: "Fine. I'll go find a $9 necklace." |
| End card | Product grid + offer | "Any 7 for $85. Waterproof." |

### Prompts

**Veo 3 / Kling 2**

```
hyperreal CGI macro, camera dives into a single gold chain link, cross-section reveals a stainless steel core with a thin glowing gold bonded layer, water droplets bead and roll off, cinematic lighting, 5s, 9:16
```

**Contrast shot**

```
macro, cheap gold-plated chain under shower spray, plating flaking to reveal grey base metal, slow motion, 4s, 9:16
```

**ElevenLabs (villain)**

```
Gravelly theatrical villain, slightly comic, stability 35, style 60. Narrator: warm female voice, stability 55.
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
- [ ] Files named `F82-<concept>-<variant>`; tracking tag `utm_content=F82-<concept>-<variant>`.
- [ ] Avoid: The CGI must match the real material and process; don't show layers or effects that don't exist.
- [ ] Avoid: Show the cheap plating failing in a way that is true; don't exaggerate it.
- [ ] Avoid: Finish on real product footage; ads that are all CGI read as fake.
- [ ] Avoid: Keep the villain under 4 lines; it is a device, not the star.

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
5. Name every asset `F82-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F82
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

An AI/CGI shot goes where no camera can: inside the metal, the bonded layer, shower spray hitting the surface. Often paired with a villain monologue (Tarnish, Green Stain) failing to get in. Rotate styles (claymation → CGI → Pixar → diorama) so the feed never learns the pattern.

### Why it works

- Shows the mechanism visually, the hardest thing to film.
- Novel visuals stop the scroll; audiences accept that it is CGI.
- Villain framing turns a spec into a story.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0-3s | Macro CGI: water droplets hit gold at 1000× | "This is your necklace in the shower." |
| 3-15s | Villain "Tarnish" (claymation goo) tries to get through the bonded layer and bounces off | villain VO: "Ugh, PVD again." |
| 15-25s | Pull out to a real necklace on real skin | "14K PVD. Any 7 for $85." |

### Hooks

- "What happens to your gold necklace in the shower (1000× zoom)"
- "Meet Tarnish. He hates this necklace."

### Production recipe

1. Storyboard 6 shots; generate frames first, then animate (Higgsfield/Kling-class tools).
2. End on real product footage on real skin.
3. Label as animation; no "real result" implication.

### Existing bot prompt

```
Storyboard a 25s LC CGI mechanism ad: 6 shots (macro water on PVD gold, a villain "Tarnish" bouncing off, pull-back to real skin), shot prompts, and VO. Accurate to {{PDP_FACTS}}.
```

### Variants to test

- CGI vs claymation villain
- Style rotation each batch

## Reference examples

See [examples/README.md](examples/README.md) (10 posts). Top 5:

- @FedotOff90 (103L/205BM/8kV): 5 AI formats scaling: AI podcast (280 days live), AI UGC, AI doctor avatar, AI listicle, AI animation (claymation/CGI). — https://x.com/FedotOff90/status/2106401392374186396
- @FedotOff90 (71L/129BM/10kV): 66-day cartoon AI ad: people know it is AI and still buy; 278 AI animation board. — https://x.com/FedotOff90/status/2072477830861254686
- @adamtaylorl (493L/741BM/77kV): Lymphoria 4,000+ ads live. — https://x.com/adamtaylorl/status/2092576938309386363
- @adamtaylorl (0L/0BM/0V):  — https://x.com/adamtaylorl/status/2102759896789713340
- @adamtaylorl (0L/0BM/0V):  — https://x.com/adamtaylorl/status/2097686470941438260
