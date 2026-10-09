# BOT.md · generate a "Cliffhanger-cut drama ad (stops at the peak; \"part 2\" / full episode lives on the PDP, app or profile)"

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
5. Name every asset `F106-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F106
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

The ad is **Episode 1 cut at the peak**: the shove, the slap, the necklace falling into the pool, the text that says "I know what you did". A title card says *"Part 2 → link"* or *"Watch how it ends"*, and the click lands where the ending lives (a PDP with the ending video on top, the TikTok profile, or an advertorial). It borrows the micro-drama app paywall: you pay with a click instead of coins.

### Why it works

- Open loops are the strongest retention tool in short video; the ending becomes the reason to click.
- Clicks come from curiosity, so the landing page must pay off the story first, then sell.
- Episodes can be sequenced in retargeting (Ep1 cold → Ep2 to 50% viewers → Ep3 with offer).
- Caution: it trains clicks, not purchases; judge on Omni revenue, not CTR.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0-2s | Wedding pool party; bride's cousin 'accidentally' bumps her | Text: "She did it on purpose." |
| 2-6s | Slow motion: necklace snaps off? (no, she goes in wearing it) splash | Music swells |
| 6-10s | Cousin smirks: "Hope that wasn't real gold." | — |
| 10-12s | Underwater: a glint of gold; freeze frame | "Part 2 →" |
| Landing (Ep2, 15 s) | She surfaces, necklace bright; cousin's own bracelet dull; product beat | "14K PVD · any 7 for $85" |

### Hooks

- "She pushed me in the pool on purpose."
- "I wasn't supposed to see that text."
- "My MIL swapped my wedding necklace."
- "Episode 1: the bridesmaid who hated me"

### Production recipe

1. Write the full story (3 episodes, 12-20 s each) before shooting; the product must sit in the ending.
2. Produce as F105 (character lock, 1.5-2.5 s shots, real product footage).
3. **Ep1** = cold ad, ends on a freeze frame + "Part 2" card.
4. **Landing:** PDP or advertorial with Ep2 autoplaying muted at the top, then the offer; or the TikTok profile pinned post.
5. **Retarget:** 50% Ep1 viewers get Ep2 as an ad; Ep3 = offer close (F99).

### Existing bot prompt

```
Write a 3-episode cliffhanger drama for Louise Carter (12-20 s each). Ep1 ends on a freeze frame at peak tension; Ep2 pays it off with a real LC water/sweat moment; Ep3 is an offer close (any 7 for $85). For each shot: duration, action, dialogue ≤8 words, on-screen text, AI prompt. Add landing-page copy that opens by resolving Ep1 in one line.
```

### Variants to test

- Cliffhanger vs full payoff (F105)
- Landing: PDP-with-video vs advertorial vs profile
- Episode length

## Reference examples

See [examples/README.md](examples/README.md) (4 posts). Top 5:

- @Ecombos_Ai (147L/205BM/8kV): AI drama ads are the next BIG thing printing for brands right now. They don't look like ads. They play like a drama episode, and people stay to see how it ends. — https://x.com/Ecombos_Ai/status/2108240933435400432
- @Olumide_gbenro (1L/1BM/193V): We just got 2.3M views on an AI drama in 24 hours. Here’s the secret to how we did it. → Find viral winners. Remix them your way. I found a similar story and re — https://x.com/Olumide_gbenro/status/2103922292640149628
- @SmartEye_ADSpy (3L/0BM/137V): Top 3 Contribute Over 40% of Market Revenue | Maiya's NetShort Cracks the Top 3 In H1 2026, the Top 20 Chinese micro drama apps in global markets generated a co — https://x.com/SmartEye_ADSpy/status/2087810501686481034
- @TheIvanKreimer (1L/0BM/62V): Smooche AI melodrama: ID-photo clerk scene, product at 1:54; retention: 90-95% drop before product. Try only if short DR saturated. — https://x.com/TheIvanKreimer/status/2107808445508321597
