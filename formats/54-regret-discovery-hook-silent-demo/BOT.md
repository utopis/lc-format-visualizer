# BOT.md · generate a "'Been doing X for N years and NOW I find this???' — regret-discovery hook + silent demo"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 15-30s, 1080x1920, silent demo), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@pixclipper](https://x.com/pixclipper/status/2084739019187847201) · A short selfie reaction ("been shopping at Lidl for 8 years and NOW I find this??"), then a long wordless screen demo of the app: tapping through store deals and recipes on a phone held over a counter. There is no voiceover; the text hook does the work.
- Example: [@themariaines](https://x.com/themariaines/status/2086845144230416463) · miso: $100K MRR and 100K downloads 5 weeks after launch with the regret-discovery hook; one video 8.0M views, 200K shares.
- Example: [@PerezHatesAI](https://x.com/PerezHatesAI/status/2107132379123077221) · I need to sit down 😭 29.3M views. 376K saves. 121K shares. For a meal planning app. The hook isn't the app. It's this line: "been shopping at Aldi lit
- Example: [@danclipping](https://x.com/danclipping/status/2075946162235011466) · $976K/month is crazy This is a study/homework helper AI app with 350 million users Just from UGC creators They run formats like "I just found this app
- Example: [@one_mtb](https://x.com/one_mtb/status/2084732666394431581) · Here’s a $1M MRR app idea that NOBODY has built…. An AI parking ticket fighter Here’s how I would build and scale it 👇 - Launch the app in a week (I u
- Example: [@ColinMaddenUGC](https://x.com/ColinMaddenUGC/status/2097280776421126601) · Our 1.8k-follower UGC creator pulled 12.2M views while some 400k-follower ones can’t even hit 10k… We’ve seen this happen across 100s of brands and th
- Example: [@pixclipper](https://x.com/pixclipper/status/2090016988223430845) · this app crossed $100K revenue and 100K downloads in under 50 days 🤯 their whole strategy is one ugc format on repeat: - shocked face reaction - a sna

### Live paid ads in this format (2 in [adlibrary/](adlibrary/README.md), longest-running first)

- **Muscle Mat: Dog-test visual hook (Muscle Mat, 859 days)** (859 days live): A dog flops on the mattress topper and a woman presses it; captions "what makes our campsite super comfy… 35 mm thick". DCO.
- **Muscle Mat: "FREE" baby-on-topper static (Muscle Mat)** (533 days live): A baby asleep on the topper with a "FREE" banner and a gift offer.

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| 0-3s | Text on screen over a hand holding the necklace | "Been buying gold jewellery for 15 years and NOW I find this???" |
| 3-10s | Silent demo: shower water over the chain | - |
| 10-18s | Sea dip, then the chain still bright | - |
| 18-24s | Close-up of the stack | "14K PVD. Waterproof." |
| End | Offer | - |

### Prompts

**Hook bank (Claude)**

```
Write 15 variations of "Been doing X for N years and NOW I find this???" for [audience], each with a specific number and habit.
```

**Shoot**

```
Macro clips, no voice, trending sound low.
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
- [ ] Files named `F54-<concept>-<variant>`; tracking tag `utm_content=F54-<concept>-<variant>`.
- [ ] Avoid: The number of years must be plausible for the person shown.
- [ ] Avoid: The demo has to prove the hook.
- [ ] Avoid: Keep text on screen to the hook and one benefit.

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

See [examples/README.md](examples/README.md) (13 posts). Top 5:

- @pixclipper (134L/339BM/26kV): Mise $300K/mo: 18 UGC accounts running the SAME 43s wordless video (ALDI/LIDL/German versions); store name does the targeting; 702 videos in 8 weeks, 3 carry 60 — https://x.com/pixclipper/status/2084739019187847201
- @themariaines (25L/42BM/3kV): Herbi: 70K downloads, $20K/mo in 50 days, 20M+ views; Mise copied the playbook → $100K/mo in 5 weeks. — https://x.com/themariaines/status/2090121630538412531
- @consumerxai (12L/18BM/1kV): 30 most-SAVED app TikTok hooks in 6 types (POV moment, name the viewer, disbelief, signs/lists, result first, pattern interrupt); save rate > views as signal. — https://x.com/consumerxai/status/2107471216126906682
- @wesocialgrowth (2L/8BM/838V): Herbi + Mise: 30M+ combined views with shocked reaction + app demo + "been shopping at [supermarket] for 10 years and NOW I FIND THIS". — https://x.com/wesocialgrowth/status/2087932298939544011
- @jakeackerm (1L/0BM/88V): 2.6M views in 7 days: crying face + text, then app demo; template "been (doing X) for x years and NOW I FIND THIS ???". — https://x.com/jakeackerm/status/2079949900037415215
