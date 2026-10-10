# BOT.md · generate a "Persona-swap script cloning (one winning script, re-told by 6-10 different narrators and settings)"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: One locked script x 6-10 narrators, 20-40s each), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@SparkifyAI](https://x.com/SparkifyAI/status/2078068798314422644) · An AI-cloned UGC creator in an orange gym set talking excitedly to camera in a home gym. It is the same script performed by an AI persona instead of a real creator.
- Example: [@adamtaylorl](https://x.com/adamtaylorl/status/2105251325575315867) · 2. The breed callout "If your Shih Tzu is itching constantly" – then "over 50 times a day." One breed, one number, and every owner of that breed stops
- Example: [@adamtaylorl](https://x.com/adamtaylorl/status/2100540267476496805) · 1. The Niche Hook… Most brands write one ad for everyone. Loop writes one ad for a specific person. A neurodivergent creator in her car explaining exa
- Example: [@mikefutia](https://x.com/mikefutia/status/2080734489529971056) · I just cracked the code on cloning UGC ads with AI 🤯 One ad that's already converting → 20 different creators delivering the exact same script. New fa
- Example: [@lorenzo_pravata](https://x.com/lorenzo_pravata/status/2079246318191403496) · Resilia ~8,000 ads, "$10-15M/month" (unverified); mostly AI avatars/doctors/claymation; gap = real authority reshoots + long unaware VSL.
- Example: [@edwardlavinel_](https://x.com/edwardlavinel_/status/2082467046034702738) · Shit. Analyzed 800+ active ads from creatine gummy. one pattern doing all the work. want the beats? Here is the breakdown: - uses a magazine cutout ae
- Example: [@oliverxmedia](https://x.com/oliverxmedia/status/2075560773657694682) · I genuinely had to do a double take the first time I watched this. If nobody told me it was AI-generated, I would've assumed it was filmed by a real c
- Example: [@wabilaura](https://x.com/wabilaura/status/2082918789470208150) · Ladies in the algo. Dr turner from féline skinscience is printing. 800+ active ads and the winner is the same hook every time. why is nobody copying i
- Example: [@wabilaura](https://x.com/wabilaura/status/2083215336971858040) · Ladies in the algo. Dr turner from féline skinscience is printing. 800+ active ads and the winner is the same hook every time. why is nobody copying i

### Live paid ads in this format (6 in [adlibrary/](adlibrary/README.md), longest-running first)

- **Prime Prometics: Older-man talking head (Prime Prometics persona ad)** (331 days live): A white-haired man in a black shirt talks and laughs to camera, holding the product tube, with captions ("…called PrimeLash", "but I'm going to try", "My wife would", "The girls."). 153 s. Prime Prometics has 2,702 active ads.
- **Smooche · Smooche: “My ex has been locked in A woman he left me for Young enough to be her…”** (21 days live): Opens: “My ex has been locked in A woman he left me for Young enough to be her daughter On the first date, I've been on in 22 years And the only reason I didn't fall apart On both of them So, the day before,…” The same script appears in 2 ads across 2 pages (C
- **Smooche · Cosmetic Times: “I'm going to be a high loronic acid, a peptide serum, a night cream…”** (4 days live): Opens: “I'm going to be a high loronic acid, a peptide serum, a night cream, and none of it moved the needle. I was doing all of that because I had a trip booked.” The same script appears in 2 ads across 2 pages (Cosmetic Times, Vascular Wellness Report).
- **Resilia · Arterial Health Review: “I'm the founder of Resilia and I owe all of you an apology. I told you…”** (1 days live): Opens: “I'm the founder of Resilia and I owe all of you an apology. I told you the last sale was the best price you'd ever get, and then we overproduced.” The same script appears in 2 ads across 2 pages (Arterial Health Review, Vascular Wellness Report).
- **Resilia · Midlife Wellness Journal: “One night my husband asked me to keep my shirt on 22 years of marriage…”**: Opens: “One night my husband asked me to keep my shirt on 22 years of marriage and that's what we've come, too He has no idea what that night cost him. We met when we were six Mary 22 years and for two…” The same script appears in 3 ads across 2 pages (Midlife
- **Resilia · Ancient Remedy Co: “This is what happens to your swollen prostate that's been killing your…”**: Opens: “This is what happens to your swollen prostate that's been killing your wood and the nerves that make everything work downstairs. It's finally being reached.” The same script appears in 2 ads across 2 pages (Ancient Remedy Co, Jennifer Williams - Gut He

**Do not copy (seen in these live ads):** The pages pose as independent reviews and publications. Running the same script from fake independent pages is deceptive. Use real creators who disclose the partnership.

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| Lock the script | Take a winning script (e.g. from F14 or F06) and freeze it word for word | - |
| Narrator 1-3 | Real creators of different ages (20s, 40s, 60s), each in their own setting (car, kitchen, beach) | Exactly the same words |
| Narrator 4-6 | Different ethnicities and styles; one man buying a gift | Same words, his own delivery |
| Narrator 7-10 | AI avatars (labelled) to fill gaps fast | Same words |
| Test | Launch all versions in one ad set with Dynamic Creative off | Naming F97-narratorNN |

### Prompts

**Arcads / HeyGen**

```
Upload the locked script, pick 4 avatars that differ in age and setting, export 9:16 and 4:5, burn captions in the same style as the real versions.
```

**Creator brief**

```
Say the script exactly; film in your own space; 3 takes; natural light; phone at eye level.
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
- [ ] Files named `F97-<concept>-<variant>`; tracking tag `utm_content=F97-<concept>-<variant>`.
- [ ] Avoid: Label AI avatars.
- [ ] Avoid: Don't change the script while testing narrators, or you won't know what moved results.
- [ ] Avoid: Match caption style across versions so only the narrator differs.

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

See [examples/README.md](examples/README.md) (30 posts). Top 5:

- @grok (0L/0BM/0V): Pod strategy: creatives labelled Pod1…Pod26, hosted unlisted on YouTube to build view counts (Pod26 420K views in 3 weeks). — https://x.com/grok/status/2105957466420703499
- @Best_OFPages (0L/0BM/0V): Claim: Smooche (Ooak Brands) runs only AI ads at ~$1M/day (unverified). — https://x.com/Best_OFPages/status/2105176364748054721
- @thevslguy (0L/0BM/0V): Resilia and Lymphoria run the same ad with their own mechanism at the end. — https://x.com/thevslguy/status/2089344767293567232
- @lorenzo_pravata (0L/0BM/0V): Resilia ~8,000 ads, "$10-15M/month" (unverified); mostly AI avatars/doctors/claymation; gap = real authority reshoots + long unaware VSL. — https://x.com/lorenzo_pravata/status/2079246318191403496
- @funneloftheweek (0L/0BM/0V): Resilia: 12 persona Pages → one 7-min advertorial (30-50% of traffic), 3-4 copy templates × hundreds of creatives, 544 new ads/30d, OTO flow $30→$83. — https://x.com/funneloftheweek/status/2044464896104857850
