# BOT.md · generate a "Customer thank-you / shout-out turned into an ad"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: Static 1080x1350 or a 15-25s video), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@LorelDiamonds](https://x.com/LorelDiamonds/status/2099906094990508266) · A fine-jewellery brand's thank-you post: a customer's hand wearing her ring next to flowers and the note she sent about what the piece means to her. The caption: "The loveliest part of creating jewellery is hearing what it means to the person wearing it. Thank you to our customer for sharing their experience."
- Example: [@E_S_Collectible](https://x.com/E_S_Collectible/status/2082178074108637387) · Huge shoutout to our customer @GamecockCards for creating these two incredible custom 3D cards! The detail and depth look amazing in person. Please ch
- Example: [@Nate_Google_](https://x.com/Nate_Google_/status/2090789562121359452) · this is a PRIME EXAMPLE of why native style creative wins 600k views on this article post in 5 hours nobody scrolls past a handwritten note on a cup. 
- Example: [@envyofyibo](https://x.com/envyofyibo/status/2095707442294448570) · Lanqin Lozenges Weibo "Lanqin Lozenges's Monkey Lily suddenly disappeared last night!! We found a handwritten note on his workstation. 🔍 It said he wa

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| 0-3s / image | The customer's own photo or clip (wearing the piece), with permission | Text: "Thank you, Maria." |
| 3-12s | Her words, quoted verbatim on screen or read by the founder | "I wore it every day of my mum's last summer. It's the one thing I never take off now." |
| 12-18s | Founder to camera, a short genuine reply | "This is why we make it waterproof." |
| End | Product in the photo + soft CTA | "The Mae Necklace. Any 7 for $85." |

### Prompts

**Consent ask**

```
DM: "Your message made our week. Would you be OK with us sharing your photo and words in a thank-you post and ads? We'll credit you however you like."
```

**Copy (Claude)**

```
Write a 40-word thank-you caption that quotes the customer verbatim and adds one sentence from the founder; no sales language until the last line.
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
- [ ] Files named `F89-<concept>-<variant>`; tracking tag `utm_content=F89-<concept>-<variant>`.
- [ ] Avoid: Explicit consent from the customer is required for ads.
- [ ] Avoid: Never polish or rewrite her words.
- [ ] Avoid: Don't use grief or sensitive stories without the customer's clear OK.

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
5. Name every asset `F89-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F89
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

The brand publicly thanks one real customer (a note, video or photo) for their story or photo: "Thank you, Maria, for wearing your stack through a whole summer of sea swims." Gratitude makes the proof feel human and specific.

### Why it works

- Gratitude is disarming; the ad doesn't ask for anything.
- One named story is more believable than an average.
- Customers love being featured, which encourages more submissions.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| Static | Handwritten thank-you card next to the customer's photo (with consent) | "Thank you, Maria" |
| Video 20s | Founder reads the customer's message, then thanks her | — |

### Hooks

- "Thank you, Maria."
- "A note to the customer who wore it up Kilimanjaro"

### Production recipe

1. Pick 3 customer stories with written consent.
2. The founder writes and reads the thank-you.
3. Run to warm audiences first.

### Existing bot prompt

```
Write 3 customer thank-you ads for LC (card text ≤50 words + 20s founder VO) from {{STORIES}} with consent.
```

### Variants to test

- Card vs video

## Reference examples

See [examples/README.md](examples/README.md) (3 posts). Top 5:

- @LorelDiamonds (0L/0BM/0V):  — https://x.com/LorelDiamonds/status/2099906094990508266
- @Nate_Google_ (211L/267BM/23kV): this is a PRIME EXAMPLE of why native style creative wins 600k views on this article post in 5 hours nobody scrolls past a handwritten note on a cup. everybody  — https://x.com/Nate_Google_/status/2090789562121359452
- @envyofyibo (44L/3BM/2kV): Lanqin Lozenges Weibo "Lanqin Lozenges's Monkey Lily suddenly disappeared last night!! We found a handwritten note on his workstation. 🔍 It said he was going to — https://x.com/envyofyibo/status/2095707442294448570
