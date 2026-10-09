# BOT.md · generate a "Persona-swap script cloning (one winning script, re-told by 6-10 different narrators and settings)"

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
5. Name every asset `F97-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F97
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

A production system rather than a single look: lock a winning script and its claims, then re-shoot it with many different narrators (age, ethnicity, setting, wardrobe) and visual treatments (to-camera, podcast, podium, animation), and launch each as a separate creative. Meta reads each persona/setting as a new creative, the script stays proven, and each audience segment sees someone like them.

### Why it works

- The script is the proven asset; the narrator is the variable that finds new pockets of audience.
- Different people and settings create genuinely different Entity IDs under Andromeda.
- Lowers creative risk: you are only testing the messenger.
- Resilia pairs it with 12+ persona Pages to split risk; that part is the compliance problem.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| Script lock | One 45-60 s script with fixed claims and a fixed CTA | "Your jewelry turned green because it was plated…" |
| Takes 1-8 | Same words: a 24-year-old nurse in scrubs, a 58-year-old grandmother at a kitchen table, a lifeguard, a bride, a gym owner, a jeweller at a bench | Each records the same script in her own voice |
| Launch | Each take = its own ad; same primary text; Omni tags by narrator | — |

### Hooks

- Same script, 8 narrators: hook stays identical
- "I'm a lifeguard. Here's the jewelry I never take off."
- "I'm 61 and this is the only necklace I swim in."

### Production recipe

1. Pick LC's current best-CPA script (any format).
2. Cast 8 real creators across ages 22-65 and settings (beach, kitchen, office, gym, bench).
3. Shoot all with the same script; vary only the first 2 seconds of B-roll.
4. Launch as 8 ads in one ad set; tag Omni by narrator; keep the winners, recast the losers.

### Existing bot prompt

```
Take the LC winning script {{SCRIPT}}. Produce 8 narrator briefs (age, job, setting, wardrobe, first-frame B-roll, one-line personal intro) that keep the script word-for-word after the intro. Diverse but authentic; every narrator must be a real paid creator with disclosure.
```

### Variants to test

- Narrator age
- Setting
- Intro line

## Reference examples

See [examples/README.md](examples/README.md) (23 posts). Top 5:

- @grok (0L/0BM/0V): Pod strategy: creatives labelled Pod1…Pod26, hosted unlisted on YouTube to build view counts (Pod26 420K views in 3 weeks). — https://x.com/grok/status/2105957466420703499
- @Best_OFPages (0L/0BM/0V): Claim: Smooche (Ooak Brands) runs only AI ads at ~$1M/day (unverified). — https://x.com/Best_OFPages/status/2105176364748054721
- @thevslguy (0L/0BM/0V): Resilia and Lymphoria run the same ad with their own mechanism at the end. — https://x.com/thevslguy/status/2089344767293567232
- @lorenzo_pravata (0L/0BM/0V): Resilia ~8,000 ads, "$10-15M/month" (unverified); mostly AI avatars/doctors/claymation; gap = real authority reshoots + long unaware VSL. — https://x.com/lorenzo_pravata/status/2079246318191403496
- @funneloftheweek (0L/0BM/0V): Resilia: 12 persona Pages → one 7-min advertorial (30-50% of traffic), 3-4 copy templates × hundreds of creatives, 544 new ads/30d, OTO flow $30→$83. — https://x.com/funneloftheweek/status/2044464896104857850
