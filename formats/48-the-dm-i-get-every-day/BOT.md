# BOT.md · generate a "'The DM / question I get every day' answer video"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 20-45s, 1080x1920 (reply-to-comment overlay)), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@MaGeAuNaturel](https://x.com/MaGeAuNaturel/status/1775569173747228909) · A skincare founder films herself on a balcony, phone held at arm's length, answering a question she says she gets asked all the time. About 27 seconds, one take, natural light, a product held up to camera partway through. The post copy says "This is a common question I get asked!" and sends people to the link in bio.
- Example: [@Aeeshatuuuu](https://x.com/Aeeshatuuuu/status/2100222367909724510) · DAY 13 One question I get asked frequently is, Do you deliver outside Kaduna? And the answer is YES,we deliver nationwide across Nigeria,and guess wha
- Example: [@nikitaavermaa](https://x.com/nikitaavermaa/status/2005526119584551309) · Address the most asked question head on - this is why going through comment sections and customer queries are so important! Great for weight loss/skin
- Example: [@antonioventre_](https://x.com/antonioventre_/status/2091592059517837677) · Customer-SERVICE call ad: record a real pre-purchase support call answering the 5-6 questions buyers actually ask.

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| 0-2s | TikTok reply sticker with the real question | "Can you really shower in it??" |
| 2-6s | Founder or stylist to camera | "I get this DM every single day, so here's the answer." |
| 6-20s | Demo: wears it under the shower, then wipes dry | "14K PVD over stainless steel. It's bonded, so there's nothing to wash off." |
| 20-30s | Shows a 9-month-old piece next to a new one | "This one is 9 months old." |
| End | Offer | "Any 7 for $85." |

### Prompts

**Question mining**

```
Export the last 200 DMs and comments; group by question; rank by frequency; film the top 5.
```

**Shoot**

```
Front camera, one take, natural light; reply sticker added in-app.
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
- [ ] Files named `F48-<concept>-<variant>`; tracking tag `utm_content=F48-<concept>-<variant>`.
- [ ] Avoid: Use real questions (screenshot them).
- [ ] Avoid: Answer the question in the first 10 seconds.
- [ ] Avoid: Don't over-claim in the answer.

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
5. Name every asset `F48-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F48
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

Founder/creator shows a real DM or recurring question (blurred sender) and answers it on camera — objection handling disguised as content.

### Why it works

- Answers the #1 objection natively.
- Feels like a reply, not an ad.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0-2s | DM screenshot (blurred) | "I get this DM every day" |
| 2-15s | Qirra answers with demo | Shower demo |
| 15-20s | CTA | — |

### Hooks

- "The DM I get every single day"
- "No, it won't turn green — here's why"

### Production recipe

1. Pull top 10 questions from inbox/comments; real DMs only, blur sender.

### Existing bot prompt

```
From {{INBOX_EXPORT}}, rank the 10 most frequent pre-purchase questions and write a 15s answer script for each using PDP wording.
```

### Variants to test

- Founder vs CS rep

## Reference examples

See [examples/README.md](examples/README.md) (4 posts). Top 5:

- @antonioventre_ (12L/13BM/995V): Customer-SERVICE call ad: record a real pre-purchase support call answering the 5-6 questions buyers actually ask. — https://x.com/antonioventre_/status/2091592059517837677
- @raph_guilhem (55L/105BM/7kV): 30 Meta ad formats folder tree (hooks, founder content, etc.). — https://x.com/raph_guilhem/status/2083288607062732816
- @adamtaylorl (36L/36BM/3kV): Dead in 2026: polished studio, "hey guys" UGC, discount statics, founder-story VSLs. Printing: ugly advertorial statics, long-form yapper, comment-reply hooks,  — https://x.com/adamtaylorl/status/2086814826177679660
- @MaGeAuNaturel (0L/0BM/0V):  — https://x.com/MaGeAuNaturel/status/1775569173747228909
