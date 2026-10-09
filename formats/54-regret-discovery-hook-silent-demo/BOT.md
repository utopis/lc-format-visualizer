# BOT.md · generate a "'Been doing X for N years and NOW I find this???' — regret-discovery hook + silent demo"

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
5. Name every asset `F54-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F54
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

A 2-4 second selfie of genuine exasperation/disbelief (hand on forehead, near-tears, "no way") with a caption that names a long habit + a specific place/brand the viewer shares — "been shopping at ALDI for 8 years and NOW I FIND THIS ???" — then a silent, hands-only demo of the product doing the thing. Almost no words, so any creator in any country can re-shoot it.

### Why it works

- The named habit/place is the targeting: everyone who shares it stops (@pixclipper: "the store name does the targeting").
- Disbelief + regret ("8 years!") is a loss-aversion hook — viewers fear they are also missing out.
- Wordless → any creator re-shoots it in an afternoon; 18 accounts × daily posting = 702 videos in 8 weeks.
- It is among the most SAVED hook types, not just watched (@consumerxai).

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0-3s | Selfie, hand on forehead, disbelief/near-tears face; caption "been buying gold jewelry for 10 years and NOW I FIND THIS ???" | "no way" (only words) |
| 3-10s | Hands-only: LC necklace under running shower water, close-up | Shower SFX |
| 10-18s | Same necklace in pool/sea; then next to an old green-tinged chain (own, unbranded) | — |
| 18-25s | Hands build a 7-piece stack on the LC PDP / box | Caption stays on top |
| 25-30s | Price card "any 7 for $85" on screen | — |

### Hooks

- "been buying gold jewelry for 10 years and NOW I FIND THIS ???"
- "been taking my necklace off to shower for 12 years and NOW I find this ???"
- "been buying my sister birthday candles for 6 years and NOW I find this ???"
- "been shopping at [mall store] for jewelry for 8 years and NOW I FIND THIS ???" (avoid naming competitors in paid)
- "been throwing out green-turning rings since high school and NOW…"

### Production recipe

1. Write 10 caption variants: habit × years × shared context (a store, a routine, a gift occasion).
2. Brief creators (F43 swarm): 3s disbelief selfie (real reaction to first trying it), then hands-only demo; no talking.
3. Film the demo flat-lay/top-down on a real bathroom counter, shower, pool.
4. Post daily across 5-20 creator accounts; track which 3 carry views; boost winners as Spark/Partnership ads.
5. Localise: swap the shared context per market (store, season, holiday).

### Existing bot prompt

```
Write 15 regret-discovery captions for LC in the exact pattern "been [habit] for [N] years and NOW I FIND THIS ???" Habits must be real pains of women 25-55 with gold jewelry (taking it off to shower, green neck, buying gifts, tarnish). Then for the best 5, write a 20s silent hands-only demo shot list using only PDP facts {{PDP_FACTS}}.
```

### Variants to test

- Habit/years wording
- Shared context (store vs routine vs occasion)
- Crying vs annoyed vs shocked face
- Demo location

## Reference examples

See [examples/README.md](examples/README.md) (12 posts). Top 5:

- @pixclipper (134L/339BM/26kV): Mise $300K/mo: 18 UGC accounts running the SAME 43s wordless video (ALDI/LIDL/German versions); store name does the targeting; 702 videos in 8 weeks, 3 carry 60 — https://x.com/pixclipper/status/2084739019187847201
- @themariaines (25L/42BM/3kV): Herbi: 70K downloads, $20K/mo in 50 days, 20M+ views; Mise copied the playbook → $100K/mo in 5 weeks. — https://x.com/themariaines/status/2090121630538412531
- @consumerxai (12L/18BM/1kV): 30 most-SAVED app TikTok hooks in 6 types (POV moment, name the viewer, disbelief, signs/lists, result first, pattern interrupt); save rate > views as signal. — https://x.com/consumerxai/status/2107471216126906682
- @wesocialgrowth (2L/8BM/838V): Herbi + Mise: 30M+ combined views with shocked reaction + app demo + "been shopping at [supermarket] for 10 years and NOW I FIND THIS". — https://x.com/wesocialgrowth/status/2087932298939544011
- @jakeackerm (1L/0BM/88V): 2.6M views in 7 days: crying face + text, then app demo; template "been (doing X) for x years and NOW I FIND THIS ???". — https://x.com/jakeackerm/status/2079949900037415215
