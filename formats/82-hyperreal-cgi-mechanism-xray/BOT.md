# BOT.md · generate a "Hyperreal CGI mechanism / 'x-ray' shot (inside the material) + villain monologue"

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

See [examples/README.md](examples/README.md) (7 posts). Top 5:

- @FedotOff90 (103L/205BM/8kV): 5 AI formats scaling: AI podcast (280 days live), AI UGC, AI doctor avatar, AI listicle, AI animation (claymation/CGI). — https://x.com/FedotOff90/status/2106401392374186396
- @FedotOff90 (71L/129BM/10kV): 66-day cartoon AI ad: people know it is AI and still buy; 278 AI animation board. — https://x.com/FedotOff90/status/2072477830861254686
- @lifemaximised (26L/10BM/3kV): I spent 48h building a FULL YouTube Ads system that combines Seedance 2.5 + Images 2.0 + Opus 5 From market research to winning AI ad creatives to campaign opti — https://x.com/lifemaximised/status/2085761997526999415
- @D_Only_Aji (9L/2BM/603V): Just wrapped up this 3D animated performance ad for Rejuvenate, built from the ground up using an AI-assisted production workflow. From creative direction, visu — https://x.com/D_Only_Aji/status/2091972209178796230
- @vladdubchak_x (4L/3BM/223V): Found this in the AI and CGI swipe file. A frequency-healing device has run the same ad for one hundred and ninety-eight days, and nobody speaks in it. It's thr — https://x.com/vladdubchak_x/status/2106709668324093965
