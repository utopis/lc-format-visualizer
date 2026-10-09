# BOT.md · generate a "Podcast-style ad (two mics, conversation clip)"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 30-90s clip, 1080x1920 (podcast set framed for vertical)), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@tryatria_AI](https://x.com/tryatria_AI/status/2097763972325745046) · Podcast-studio cuts: men at mics delivering lines with big captions ("I used to be you", "I couldn't"), cutaways to the Heights supplement tub ("I started taking") and an ingredients card, then several different hosts. It looks like clipped podcast content, not an ad.
- Example: [@HenryCrochemore](https://x.com/HenryCrochemore/status/2089291503919087933) · ai podcast ads might be one of the easiest ways to make ugc feel native again instead of generating another creator holding a product put them behind 
- Example: [@sixugc](https://x.com/sixugc/status/2088316130070790246) · genuinely confused why apps still don't get it they need to scale with content not ads found one tiktok account posting podcast style talking head cli
- Example: [@CEO_Vlad](https://x.com/CEO_Vlad/status/2081473127985582384) · take AI podcast ads like this and go run them in latin america... barely anyone is running the podcast format in spanish, so the feed there hasn't see
- Example: [@itsLORDROY](https://x.com/itsLORDROY/status/2079061186008760542) · Podcast ads are entering a new era. The most impressive part isn't that this is AI generated. It's that this entire podcast ad was made inside Claude 
- Example: [@adreads_ai](https://x.com/adreads_ai/status/2083709698059206725) · Podcast ads data for August 1 320 new podcast ad reads across 183 sponsors and 56 shows 187 announcer read, 123 host read Most active sponsors: @Shane

### Live paid ads in this format (6 in [adlibrary/](adlibrary/README.md), longest-running first)

- **Cellular Performance Institute: Celebrity-style podcast set clip (stem cells)** (731 days live): A Rogan-style podcast studio with headphones and mics; a guest talks about "mesenchymal stem cells… from a woman's umbilical cord". 47 s with captions.
- **BioRoot Labs: Podcast-plus-doctor stitched explainer (turmeric)** (345 days live): A woman on a podcast mic, turmeric close-ups, then a doctor with "Doctor-Formulated" and a "What do you think?" overlay. 129 s DCO with 32 media.
- **Pure Rhythm: "Content may go offline" podcast clip (weight loss)** (326 days live): "If you want to go from size L to size S, you need to hear this… three essential ingredients that the industry does everything to hide from you… share this with your friend because this content may go offline at any moment." 117 s.
- **Pure Rhythm: Menopause reframe podcast (hair / energy)** (326 days live): "When your period stops, your brain literally cuts off the signal to your ovaries… that's the moment you need to say, no, I'm not going to waste away at 50. I still have 30 years ahead." 101 s.
- **Pure Rhythm: Tough-love podcast rant ("women over 40 who still don't know this")** (324 days live): "I can't believe… woman over 40 who still doesn't know this… waking up wrecked, bloated, drained… I'm not angry. I'm just tired of watching people suffer because no one tells them the truth. Magnesium is the foundation…" 84 s.
- **Dr. Lisa Downing: "Men's health researcher" podcast (prostate DHT)** (267 days live): "As a men's health researcher, I study why the prostate swells… This is what most men over 40 get wrong about nighttime urination… Block DHT at the source… 3,000 mg cold-pressed pumpkin seed oil with saw palmetto." 54 s. Dr. Lisa Downing page, 1,357 ads.

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| 0-3s | Mid-conversation, guest at mic, warm studio (two SM7B-style mics, bookshelf, lamp) | Starts on a strong opinion: "Most gold jewelry is a scam, honestly." |
| 3-15s | Host reaction shot | Host asks the viewer's question: "Wait, what do you mean?" |
| 15-45s | Guest explains, cutaways to product B-roll / diagram | The mechanism in plain words (plating vs PVD bond) |
| 45-60s | Both laugh / agree | Product named once, naturally |
| End | Caption card | "Full episode" or offer |

### Prompts

**Real shoot**

```
2 cameras (wide + guest close-up) at 4K 30fps, 2 dynamic mics, warm practical lights at 3200K, record 20 minutes of real conversation and cut 10 clips.
```

**AI version (Veo 3 / HeyGen podcast)**

```
two people at podcast microphones in a cozy studio, warm lamp light, natural conversation, guest speaking "[line]", 8s, vertical framing
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
- [ ] Files named `F13-<concept>-<variant>`; tracking tag `utm_content=F13-<concept>-<variant>`.
- [ ] Avoid: Clips that start at the beginning of a thought are boring; start mid-sentence.
- [ ] Avoid: A fake podcast with fake "experts" is deceptive; use a real person or label AI and avoid credentials.
- [ ] Avoid: Burn in captions; 80% watch muted.

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
5. Name every asset `F13-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F13
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

Two people at podcast mics, warm studio, captions; clip starts mid-conversation with a strong opinion; host asks the question the viewer has; guest explains; product mentioned naturally. "They're not trying to make a podcast ad feel like an ad" ([@tryatria_AI](https://x.com/tryatria_AI/status/2097763972325745046)). "Best format for anything that needs explaining" ([@CEO_Vlad](https://x.com/CEO_Vlad/status/2096569603761827953)).

### Production recipe

Real: rent a podcast studio 2h → 15 clips. Metric: hold, CPA, Omni. Founder face also feeds organic (strategy 31).

## Reference examples

See [examples/README.md](examples/README.md) (13 posts). Top 5:

- @lorenzo_pravata (150L/196BM/10kV): "Ads that don't look like ads": podcast clips, street interviews, skits with studio actors; pet brand $29K→$150K/mo spend in 60 days, CPA $188→$124. — https://x.com/lorenzo_pravata/status/2104536224488738839
- @CEO_Vlad (88L/169BM/5kV): AI UGC formats tiered: S = podcast, talking head, in-car... — https://x.com/CEO_Vlad/status/2096569603761827953
- @LachezarVoynov (86L/102BM/10kV): $300k/mo strategy: wrappers that became top spenders = skits, carpool ads, Suno songs, AI Pixar-character podcasts; hooks must target different people. — https://x.com/LachezarVoynov/status/2097351286094021034
- @tryatria_AI (62L/74BM/3kV): Heights podcast ads: don't feel like ads, underrated performance format. — https://x.com/tryatria_AI/status/2097763972325745046
- @sixugc (6L/3BM/233V): genuinely confused why apps still don't get it they need to scale with content not ads found one tiktok account posting podcast style talking head clips single  — https://x.com/sixugc/status/2088316130070790246
