# BOT.md · generate a "Result reveal → expert stitch ('Y'all, this is my dad… after listening to this man. Just listen.')"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 30-60s, 1080x1920 (TikTok Stitch or duet)), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@CalixAVelarde](https://x.com/CalixAVelarde/status/2083448214431351004) · A girl in a car talking to camera with bold yellow word-by-word captions ("EUROPE THIS SUMMER", "DOING HIP THRUST"): a result-reveal story told AI-UGC style.
- Example: [@HoIyJosee](https://x.com/HoIyJosee/status/1668712653726859268) · This is my Mom after taking Lady Gaga’s advice and getting the Nurtec® ODT (rimegepant) 75 mg shot… what’s going on?!!’ @ladygaga @pfizer
- Example: [@adamtaylorl](https://x.com/adamtaylorl/status/2102759897708249588) · 4. The expert told me The expert delivers the claim, so the product never has to sell itself. This one has been live for 12 months. Tell the story of 
- Example: [@EvoBradley](https://x.com/EvoBradley/status/2082416231353590174) · The #1 most viral format in entire ugc industry. Here are a few hits from past few days… Let me break it down for you; &gt; Stitch format: inherits tr

### Live paid ads in this format (2 in [adlibrary/](adlibrary/README.md), longest-running first)

- **BioRoot Labs: Podcast-plus-doctor stitched explainer (turmeric)** (345 days live): A woman on a podcast mic, turmeric close-ups, then a doctor with "Doctor-Formulated" and a "What do you think?" overlay. 129 s DCO with 32 media.
- **Smriti Kochar: Nutritionist 3-product stack explainer (Hinglish)** (301 days live): Smriti Kochar (nutritionist) talks to camera, cut with gym b-roll and belly close-up: 'Major pain point for men and women is belly fat…' then presents 3 products (digestion, gallbladder, cortisol) as a routine, 'try all three for a month'.

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| 0-3s | A creator holds up her mum's hand wearing the ring | "Y'all, this is my mom's ring after six months of pool laps." |
| 3-10s | Close-up of the ring, still bright | "She swims every day. Still gold." |
| 10-35s | Stitch: the source clip (founder or care expert explaining PVD) | Founder: "PVD is a bonded layer, not a coat of paint..." |
| 35-45s | Back to the creator | "So yeah. I got one too." |
| End | Product + offer | - |

### Prompts

**TikTok**

```
Use Stitch on your own (or licensed) founder explainer; keep the reveal under 10s and the stitch under 25s.
```

**Brief to creator**

```
Show a real person you know who has worn the product for 3+ months; no scripts beyond the first line.
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
- [ ] Files named `F96-<concept>-<variant>`; tracking tag `utm_content=F96-<concept>-<variant>`.
- [ ] Avoid: Results must be real and on a real person, with consent.
- [ ] Avoid: The "expert" must be real and accurately described.
- [ ] Avoid: Don't stitch other people's videos without permission.

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
5. Name every asset `F96-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F96
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

Two layers in one vertical video: a relatable person shows a result on someone close (their dad, themselves on Day 1 vs Day 42) and credits "this woman/this man", then the video hands over to an expert clip that explains the mechanism. The personal result earns attention; the expert carries the explanation.

### Why it works

- Third-person proof ("my dad") feels less like bragging and more like a recommendation.
- "Just listen" sets up the expert as a discovery, not an ad.
- Stitch/duet grammar is native to TikTok and Reels.
- The expert clip can be reused under many result intros.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0:00-0:08 | Daughter holds up a photo of mom's green-stained wrist, then mom now wearing an LC stack in the pool | "Y'all, this is my mom's wrist last summer. This is her now. Just listen to this woman." |
| 0:08-0:45 | Stitched clip: LC jeweller or founder at the bench | "Most gold jewelry is plated: a layer thinner than a hair over brass. We bond 14K PVD to steel…" |
| 0:45-0:55 | Back to daughter + CTA | "She hasn't taken it off in a year. Link's below." |

### Hooks

- "Y'all, this is my mom's wrist last summer. Just listen."
- "Day 1 vs day 365 of never taking it off."
- "I didn't believe this woman until I tried it."

### Production recipe

1. Film 1 expert clip (founder or jeweller) explaining PVD in 30-40 s.
2. Collect real customer result intros (with consent) and stitch each onto the expert clip.
3. Keep the result honest: time worn, what she did (showers, pool).

### Existing bot prompt

```
Write 5 result-reveal intros (≤8 s each) from real LC customer stories {{STORIES}} and one 35-second expert explanation of bonded 14K PVD for the stitch. No exaggerated results.
```

### Variants to test

- Third-person vs self
- Expert = founder vs jeweller

## Reference examples

See [examples/README.md](examples/README.md) (5 posts). Top 5:

- @CalixAVelarde (4L/1BM/461V): this girl-in-car ai ugc format is actually insane this entire clip is ONE generation i didn't stitch anything together. dropped the script in and it came back t — https://x.com/CalixAVelarde/status/2083448214431351004
- @adamtaylorl (0L/0BM/0V):  — https://x.com/adamtaylorl/status/2102759897708249588
- @valentinszabadi (49L/58BM/3kV): How to iterate a winning creative as a strategist? Easy. - Change the talent - Change the format - UGC, VSL, Stitch, Street Interview, Podcast, AI slop, Pixar,  — https://x.com/valentinszabadi/status/2079614879309185498
- @EvoBradley (18L/31BM/1kV): The #1 most viral format in entire ugc industry. Here are a few hits from past few days… Let me break it down for you; &gt; Stitch format: inherits trust and re — https://x.com/EvoBradley/status/2082416231353590174
- @nicktheriot_ (29L/23BM/3kV): Begging every brand owner to stop this mistake: Sitting on 50 pieces of B-roll footage… And launching zero variations of it. Do THIS instead: ⦁ Find one hook →  — https://x.com/nicktheriot_/status/2085544771150352632
