# BOT.md · generate a "Testimonial mashup (real customer clip montage)"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 20-40s, 1080x1920), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@ashvinmelwani](https://x.com/ashvinmelwani/status/2105710765151752218) · A mashup of raw customer testimonials: different people on Zoom-style calls, at desks and in kitchens, each saying one line, cut together fast and ending on the brand card ("synthesis tutoring").
- Example: [@hellonecole](https://x.com/hellonecole/status/1714802268971655219) · I love a customer testimonial mashup! Meet the hormone support and period relief vitamin that's changing lives @MyHappyFlo Http://myhappyflo.co
- Example: [@_ibbibhai](https://x.com/_ibbibhai/status/1958891605307404424) · The “testimonial mashup” ad is killing it for My DTC clients! #DTCbrands #UGCads #UGC #admanagement #ads #Winningads #MetaAds #SnapchatAds
- Example: [@domaco1968](https://x.com/domaco1968/status/1949766307567620333) · If you’re in a “saturated” niche and your ads are tanking, you’ve gotta try this testimonial mashup format. So I planned this creative for a supplemen

### Live paid ads in this format (1 in [adlibrary/](adlibrary/README.md), longest-running first)

- **Blossom Essentials Skin: Short AI-UGC "only balm I'll ever buy" (Blossom Essentials, 3 variants)** (213 days live): Three 24-33 s UGC cuts: "This is the only skin balm I will ever spend money on… I've tried everything, from prescription to specialist." Different women, same script skeleton.

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| 0-3s | Strongest single customer line, selfie video | "I've worn it in the sea every day for a year." |
| 3-10s | Customers 2-4, 2s each: shower, gym, wedding | One line each: "Never taken it off." "Still gold." "My sister stole mine." |
| 10-20s | Customers 5-8: review screenshots and unboxings | Short on-screen quotes |
| 20-30s | Stack shot + review count | "4,812 reviews. 4.8 stars." |
| End | Offer | "Any 7 for $85." |

### Prompts

**Collect**

```
Email recent buyers: "Send us a 10-second selfie video answering: what surprised you most? We'll send $20 store credit." Include a release form link.
```

**Edit**

```
Cut each clip to its single best line; captions in the same style; order from strongest to weakest; music at -22 dB.
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
- [ ] Files named `F40-<concept>-<variant>`; tracking tag `utm_content=F40-<concept>-<variant>`.
- [ ] Avoid: Real customers only, with signed consent.
- [ ] Avoid: Don't script customers; ask one question and use their words.
- [ ] Avoid: Review counts on screen must be current.

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
5. Name every asset `F40-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F40
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

A fast montage of 6-12 real customers each saying one line (selfie video, review screenshot, unboxing) stitched into a 20-40s ad. Volume of real voices = proof.

### Why it works

- Social proof at scale; MOF retargeting staple (@williamkast_).
- Many faces → broad identification across age/skin tone.
- Uses content LC can collect via post-purchase flows.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0-3s | Rapid 3 faces | "I shower in it" / "6 months" / "still gold" |
| 3-25s | 8 more one-liners with name/city captions | Real audio |
| 25-30s | Review count + offer | "300,000+ customers" |

### Hooks

- "We asked customers one question: do you ever take it off?"
- "300,000 people can't be wrong (here are 12)"

### Production recipe

1. Omnisend post-purchase flow (day 30): "Send us a 10s selfie video answering X → $15 credit" with usage-rights consent.
2. Same question for everyone → clean edit.
3. Disclose incentive where required ("customers received store credit").

### Existing bot prompt

```
From these customer clip transcripts {{CLIPS}} pick 10 one-liners (≤8 words) that together cover: waterproof, compliments, gift, value, longevity. Order for a 30s montage with an opening 3-clip hook.
```

### Variants to test

- Question asked
- Length 15 vs 30s

## Reference examples

See [examples/README.md](examples/README.md) (5 posts). Top 5:

- @williamkast_ (252L/400BM/13kV): Formats by funnel: TOF founder/yapper/AI animation/natives/3 reasons/voiceless overlay; MOF comment reply/testimonial mashup/text wall; BOF urgency statics. — https://x.com/williamkast_/status/2103910235005935644
- @zackpaid (9L/20BM/2kV): 11 AI formats (agency pitch): native UGC, founder, claymation, Pixar 3D, jingle, screen recording, before/after, testimonial compilation, cinematic demo, mini-d — https://x.com/zackpaid/status/2085621175292670183
- @williamkast_ (12L/14BM/967V): 15 formats to repackage winners into (scaled to $30k/day on 3-4 angles): founder, yapper, AI animation, voiceless overlay, carousel, reply ad, text wall, review — https://x.com/williamkast_/status/2083616523134841035
- @nicktheriot_ (219L/348BM/12kV): 2026 FB creative styles tier list: S = long primary text + organic image, LTO, UGC, VSL, reaction, news; A = demo, us vs them, testimonial, close-up, founder st — https://x.com/nicktheriot_/status/2108173638033871013
- @ashvinmelwani (31L/7BM/12kV): One ad format that will always crush is a mashup of raw customer testimonials. The fastest way to get this content for us was to post in our 117K+ member Facebo — https://x.com/ashvinmelwani/status/2105710765151752218
