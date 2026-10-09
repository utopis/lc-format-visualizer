# BOT.md · generate a "In-car / "yapper" confession talking head"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 20-60s, 1080x1920, one continuous take with jump cuts), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@contentbyroxy](https://x.com/contentbyroxy/status/2100991855441666519) · A creator filming herself in the driver's seat with the sunroof open, talking fast and casually to the phone, with sunglasses on for the sign-off. It is one continuous car-talk monologue with captions.
- Example: [@hectorserrranoo](https://x.com/hectorserrranoo/status/2107526350605070475) · Wispr Flow paid UGC program: what companies get wrong.
- Example: [@hectorserrranoo](https://x.com/hectorserrranoo/status/2106136430556672384) · Panel: you're nothing without your creators (Comfrt: 10 creators = big share of revenue).
- Example: [@CEO_Vlad](https://x.com/CEO_Vlad/status/2082092962348167273) · "yapper girl in car" is such a good AI UGC format... used it this to scale my ecom brand to $200k days this format is beating every studio shot creati
- Example: [@jennamediaco](https://x.com/jennamediaco/status/2106209597526540312) · Simple in-car talking head ad scaling: car = organic, story throughout.
- Example: [@tiffanyxugc](https://x.com/tiffanyxugc/status/2097636391798854069) · #ugcexample of a yapper style script read in the car, edited by their team 🍬 I had creative freedom to take this script &amp; make it my own which mak
- Example: [@houseofjenUGC](https://x.com/houseofjenUGC/status/2087571793452118181) · Talking head in the car example! Yapping UGC as a mom ugc creator Hello@houseofjenugc.com https://t.co/4hlMiWlhlS
- Example: [@harrydelmege_](https://x.com/harrydelmege_/status/2106794963006861535) · RolyPoly yapper ads: $154.5k spend in a single day across 1,635 ads; single ads at $45.1k and $33.1k; hook rates 44-62%, hold 31-48% (Ads Manager scre

### Live paid ads in this format (7 in [adlibrary/](adlibrary/README.md), longest-running first)

- **Luxmend: Test-it-live yapper ("we're gonna see if this actually works")** (528 days live): A woman talks to her front camera for 118 s while testing a split-end trimmer on her own hair, in one take with no cuts: "we're gonna see if this split end trimmer actually works… I'm not gonna cut the video at all."
- **Kristina's Fashion Essentials: "I'll be so disappointed if this doesn't work" lash-test yapper** (382 days live): A close-up selfie: "I'm gonna be so disappointed if this does not work exactly like everyone says it does… these lashes are seriously just so stubborn". She applies the mascara live and reacts. 106 s.
- **BioRoot Labs: Ingredient-nerd yapper (turmeric percentages)** (381 days live): A creator in a branded tee explains why she picked BioRoot: "95% curcumin, around 30 times more than the store bought" and black pepper "which majority of store bought ones don't have". 125 s; the brand has 1,000 active ads.
- **HappySupp: Girlfriend-voice men's multivitamin (HappySupp)** (378 days live): A woman in a black top to camera: "Cause ain't no way he taking this without me around… this is only for you and your girl. Don't get too crazy with it. This is the men's multivitamin by HappySupp… herbal blend to support your prostate." 86 s.
- **Nothora: In-car storytime yapper (gossip hook)** (350 days live): A creator in the driver's seat tells a work-drama story ("I just got fired… because I told this woman…"), and the product drops in late. 94 s.
- **Feel Mighty: "Car chats" one-month update yapper (gifted, then hooked)** (341 days live): "Welcome to a new episode of car chats… I have been taking the mighty mushroom gummies for over a month now… initially these were sent to me as PR." 103 s.

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| 0-2s | Creator in a parked car, phone on dash mount at eye level, daylight from the windscreen | "I couldn't even wait to get inside to tell you this." |
| 2-30s | Same framing, jump cuts every 3-6s to remove pauses | Fast, personal story with one specific detail per line |
| 30-45s | She shows the product to camera (pulls necklace out of her collar) | Proof: "I've worn this in the ocean all week" |
| End | Sunglasses on / starts the car | "link's in my bio, bye" |

### Prompts

**Shoot spec**

```
iPhone front camera, 1080p 30fps, phone mount on the dash, engine off, windows closed for clean audio, face lit by daylight (park facing the sun).
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
- [ ] Files named `F14-<concept>-<variant>`; tracking tag `utm_content=F14-<concept>-<variant>`.
- [ ] Avoid: Never film while driving; parked only.
- [ ] Avoid: Over-scripted lines kill the "yapper" feel; give the creator bullet points, not a script.
- [ ] Avoid: Disclose paid partnerships (#ad / Paid partnership label).

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
5. Name every asset `F14-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F14
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

Creator in a parked car (or walking), phone propped, talking fast and personal: "I couldn't even wait to go inside to tell you." One continuous story, light jump cuts, captions. Why it works ([@jennamediaco](https://x.com/jennamediaco/status/2106209597526540312)): car looks organic, a story the whole time, feels private and unscripted.

### Production recipe

Brief 10 creators via Trybe/creator network (strategy 28) with 3 story prompts; allow improvisation; run as Partnership ads. Metric CPA; Omni new-customer.

## Reference examples

See [examples/README.md](examples/README.md) (16 posts). Top 5:

- @hectorserrranoo (210L/251BM/15kV): Wispr Flow paid UGC program: what companies get wrong. — https://x.com/hectorserrranoo/status/2107526350605070475
- @CEO_Vlad (88L/169BM/5kV): AI UGC formats tiered: S = podcast, talking head, in-car... — https://x.com/CEO_Vlad/status/2096569603761827953
- @FedotOff90 (76L/148BM/7kV): "Yappers are printing" — 299 raw talking-head yapper ads in one public swipe board (GetHookd "Yapper Ads (raw talking-head UGC) - Oct 2026"). — https://x.com/FedotOff90/status/2108198291242676622
- @LachezarVoynov (86L/102BM/10kV): $300k/mo strategy: wrappers that became top spenders = skits, carpool ads, Suno songs, AI Pixar-character podcasts; hooks must target different people. — https://x.com/LachezarVoynov/status/2097351286094021034
- @hectorserrranoo (99L/83BM/8kV): Panel: you're nothing without your creators (Comfrt: 10 creators = big share of revenue). — https://x.com/hectorserrranoo/status/2106136430556672384
