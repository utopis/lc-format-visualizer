# BOT.md · generate a "Reaction hook + fast demo (Cal AI / app-UGC 'hook and demo')"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 8-15s, 1080x1920), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@carlynorthmedia](https://x.com/carlynorthmedia/status/2077482959620190437) · A woman covers her mouth in shock (the reaction hook, captioned), then a fast screen demo of a face-search app ("you can search ANYONE's face"), and she reacts again. The whole thing is 11 seconds.
- Example: [@consumerxai](https://x.com/consumerxai/status/2096916156389240853) · Outlier: aesthetic desk-setup hook + split-screen app demo, 558K views/4.4K saves.
- Example: [@leonclipping](https://x.com/leonclipping/status/2107903429490135362) · Musa app: ONE format (4-sec shocked reaction to a body fact → mascot explains) = 522M views, 930 videos >100K, 100+ creators.
- Example: [@simonecanciello](https://x.com/simonecanciello/status/2092704268734099547) · this $100k/month relationship app is going viral with this format. 6.7M views and 578k likes. hook + demo, relatable for women. people are searching f
- Example: [@nicholasnlawton](https://x.com/nicholasnlawton/status/2104924114712469774) · Looking at the current state of tech UGC on TikTok today and remembering a time in early 2025 where you could lob up a hook and demo and drive 100k ne
- Example: [@danclipping](https://x.com/danclipping/status/2079987510680150282) · This app raked 7.1M views 387K like with the usual WTH reaction hook And they have hundreds of videos in this format with millions of views Works ever
- Example: [@getnoise](https://x.com/getnoise/status/2087608814551904327) · Viral Hook + Demo format from Cantina 📝 ”Use ChatGPT to make money online” - but actually, you’re using their service to do it. No one thinks twice ab
- Example: [@tellenne_](https://x.com/tellenne_/status/2104591914511045111) · Instagram account with 11.6M views in the US [Real anonymized @tokportal data] CPM: $0.014 | B2B SaaS | UGC (non-AI) hook + demo format This account a
- Example: [@consumerxai](https://x.com/consumerxai/status/2102862107205398992) · ‼️Tiktok Outlier Alert ‼️ 📉 370K Views, 23K Likes, 207 Comments, 1.6K Shares, 2.9K Saves 🧐What this is: > A genuine reaction hook you can use to promo

### Live paid ads in this format (5 in [adlibrary/](adlibrary/README.md), longest-running first)

- **Muscle Mat: "I transform your bed today" demo (Muscle Mat)** (819 days live): A man sits on a hard bed, rolls out the topper, sits again and smiles; end card "SALE ON NOW · swipe up to save". 27 s.
- **Luxmend: Test-it-live yapper ("we're gonna see if this actually works")** (528 days live): A woman talks to her front camera for 118 s while testing a split-end trimmer on her own hair, in one take with no cuts: "we're gonna see if this split end trimmer actually works… I'm not gonna cut the video at all."
- **Kristina's Fashion Essentials: "I'll be so disappointed if this doesn't work" lash-test yapper** (382 days live): A close-up selfie: "I'm gonna be so disappointed if this does not work exactly like everyone says it does… these lashes are seriously just so stubborn". She applies the mascara live and reacts. 106 s.
- **Smooche · Smooche: “Apparently all the Gen XONES are going crazy for that foundation…”** (10 days live): Opens: “Apparently all the Gen XONES are going crazy for that foundation because it looks really there. And it matches perfectly only.”
- **Smooche · Smooche: “on this color changing foundation that you're seeing everywhere right…”** (10 days live): Opens: “on this color changing foundation that you're seeing everywhere right now. New one says that it's supposed to...”

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| 0-2s | Shocked reaction: hand over mouth, eyes wide, phone selfie | Text hook: "3 years of green fingers and I finally found this" |
| 2-8s | Hard cut to sped-up demo (2x): product under the shower, rubbing, still gold | Text: "showered in it for 30 days" |
| 8-12s | Back to reaction, or product close-up | "[brand]" + "link in bio" |

### Prompts

**Edit**

```
CapCut: speed 2x on the demo, hard cut on a sound hit, captions in TikTok default font, white with black outline.
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
- [ ] Files named `F28-<concept>-<variant>`; tracking tag `utm_content=F28-<concept>-<variant>`.
- [ ] Avoid: The reaction must be under 2s; longer and people scroll.
- [ ] Avoid: Demo must show the real product doing the real thing.

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
5. Name every asset `F28-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F28
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

1-4 second shocked/emotional reaction with a curiosity text hook ("3 years of X and I finally found this") → hard cut to a sped-up demo of the product doing the thing → on-screen text explains the steps → optional reaction-return. 7-15 seconds. The app-marketing workhorse behind Cal AI/Umax-style growth; for LC the "demo" is a physical reveal.

### Why it works

- The face sells before the script: surprise is contagious and creates an open loop ("what is she looking at?").
- Whole product shown in ~10 seconds, so completion and rewatch rates are high (@carlynorthmedia).
- One locked format + many creators = volume: Musa runs the same hook across 100+ creators (@leonclipping).
- Reaction discovery ranked the highest-converting app hook across 500+ UGC videos (@lucaspatiri_).

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0-2s | Creator close-up, hand over mouth / wide eyes; big caption hook | No VO or a gasp; trending sound low |
| 2-3s | Hard cut (match the gesture) to hands + product | Whoosh SFX |
| 3-9s | Sped-up demo: dunk necklace in a glass of water → wipe → still gold; or build a 7-piece stack in 5s | Captions per step ("put it in water", "scrub it", "still gold??") |
| 9-11s | Return to face: second reaction or "where has this been" caption | — |
| 11-12s | Product name + "any 7 for $85" sticker (paid) / nothing (organic) | — |

### Hooks

- "3 years of green necks and I finally found this"
- "I'm sorry WHAT is this jewelry made of"
- "POV: you find out you never have to take your jewelry off again"
- "Why did nobody tell me you can shower in gold-tone jewelry"
- "My boyfriend said it would turn green in a week. It's been 6 months."
- "I was today years old when I found out what PVD means"
- "That friend who never takes her jewelry off" (identity hook)

### Production recipe

1. Lock ONE template: hook caption style, cut point, demo action, caption font (TikTok Classic white w/ black stroke), 7-12s length.
2. Brief 10 creators (strategy 28): film 5 reactions each in different outfits/locations + 1 demo clip set we supply (LC can shoot the demo B-roll once and share it).
3. Demo library (shoot once): water dunk, sink scrub, ocean dip, sweat/gym, 6-month-old vs new, 7-piece stack build, gift-box open.
4. Assemble in CapCut template; swap hook text per post; post 1-3/day across LC TikTok + creators' own accounts.
5. Paid: take top 10% by 3s-hold into Spark/Partnership ads.

### Existing bot prompt

```
Generate 40 reaction-hook captions for Louise Carter (waterproof 14K PVD jewelry; any 7 for $85). Mix 8 hook types: discovery ("3 years of X and I finally found…"), POV, identity ("that friend who…"), disbelief, stat in first 0.5s, boyfriend/mom doubt, "I was today years old", confession. ≤10 words each, lowercase TikTok voice, no claims beyond: shower-proof/waterproof as on PDP, won't turn skin green, 14K PVD. Pair each with one demo clip from: water dunk, sink scrub, ocean dip, 6-month comparison, stack build, gift open.
```

### Variants to test

- Reaction length 1s vs 3s
- Demo: water vs stack vs comparison
- Caption hook type (8 types)
- Creator age 22-30 vs 35-50

## Reference examples

See [examples/README.md](examples/README.md) (25 posts). Top 5:

- @nicktheriot_ (219L/348BM/12kV): 2026 FB creative styles tier list: S = long primary text + organic image, LTO, UGC, VSL, reaction, news; A = demo, us vs them, testimonial, close-up, founder st — https://x.com/nicktheriot_/status/2108173638033871013
- @jesseabed_ (148L/324BM/18kV): Sideshift creator pay: hook-and-demo creators ~$400 base + view milestones for 40-60 videos; talking head/skit ~$400 for 20-30; 25% upfront. — https://x.com/jesseabed_/status/2102818749384421524
- @alexolim_ (55L/192BM/9kV): Glam AI / Cal AI / Umax used the same 5 UGC content patterns to $1M MRR (image + thread). — https://x.com/alexolim_/status/2086830919587942456
- @lucaspatiri_ (53L/122BM/4kV): 9 hooks in 80% of top app UGC (500+ videos/30 apps): POV, reaction discovery (highest-converting), "that friend who…", before/after, guilty confession, stat in  — https://x.com/lucaspatiri_/status/2076336849111449657
- @cesaralvarezll (74L/108BM/9kV): UGC reaction + app demo works for almost any product (Arcads pitch). — https://x.com/cesaralvarezll/status/2069747240634032364
