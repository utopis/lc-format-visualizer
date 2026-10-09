# BOT.md · generate a "TikTok Shop affiliate shoppable demo (real creators, sample seeding)"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 15-40s, 1080x1920, TikTok Shop product link), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@maverickecom](https://x.com/maverickecom/status/2103161679421071603) · A TikTok Shop affiliate explainer: the creator's profile and GMV dashboard ($100K+ in 30 days), then the creator talking to camera, then a grid of the many accounts posting the same shoppable product videos.
- Example: [@maverickecom](https://x.com/maverickecom/status/2079593540380684296) · 550 AI videos/day via AI affiliate army (bulk-account; not compliant).
- Example: [@maverickecom](https://x.com/maverickecom/status/2107470108515782720) · Repurpose winning TTS content across hundreds of creator-style accounts (bulk-account; not compliant).
- Example: [@maverickecom](https://x.com/maverickecom/status/2103191756153962752) · Hormozi loves affiliate marketing. In ecom the proper method for affiliate marketing is scaling an affiliate army. Here’s what that actually means — a
- Example: [@maverickecom](https://x.com/maverickecom/status/2103878538851950958) · GPT Astra + Fastmoss + Manus + Omni Flow = AI Content Factory We built a fully automated system that repurposes, localizes, and launches winning TikTo
- Example: [@maverickecom](https://x.com/maverickecom/status/2078105645757178124) · 4 years and over $1M GMV into TikTok Shop, here's what I've been surprised to learn. 1. Products must be new, in season, or niche. Videos must be inte

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| 0-2s | Hook: product in hand to camera, or the water test already happening | Hook pulled from a real review: "I wore this in the pool for a week" |
| 2-10s | Unboxing: box, packaging, clasp close-up | "it comes like this, gift-ready" |
| 10-25s | Put it on, water test under the tap, rub it | "no green, no fading" |
| 25-35s | Point down at the orange cart | "it's linked below, tap the cart" |

### Prompts

**Creator brief**

```
Film vertical 1080p, 15-40s. Start with the water test or a real review line. Show the price and the cart in the last 5s. Use TikTok Shop product link. No medical or "never tarnishes forever" claims.
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
- [ ] Files named `F19-<concept>-<variant>`; tracking tag `utm_content=F19-<concept>-<variant>`.
- [ ] Avoid: Seed samples to many small creators instead of a few big ones; most affiliate GMV comes from volume.
- [ ] Avoid: Creators must use the Shop disclosure; no unverified claims.
- [ ] Avoid: Demo the one thing the reviews praise; long feature lists do not convert on Shop.

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
5. Name every asset `F19-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F19
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

15-40s creator video with orange shopping cart: unboxing → put on → water test → "linked below / tap the cart". One hook per video pulled from real reviews (@maverickecom). Seed widely: 1,000 free samples/month (@NotZainAgain playbook); creators doing 4+ ads get their own ad set (@zachlduncan Trybe structure); use Trybe as a **performance** platform, not gifting (@httpsean_ca).

### Production recipe

TikTok Shop listing + open/targeted collaborations; commission 15-25%; sample requests auto-approve for creators with >X GMV; weekly creator brief with top 5 hooks; Spark-code the top 10 videos.

## Reference examples

See [examples/README.md](examples/README.md) (21 posts). Top 5:

- @maverickecom (567L/934BM/44kV): $34 product: TikTok Shop affiliates (trust) + AI affiliate pages on IG/FB to Amazon; one hook per video from reviews. — https://x.com/maverickecom/status/2106072031687315486
- @maverickecom (190L/226BM/11kV): Repurpose winning TTS content across hundreds of creator-style accounts (bulk-account; not compliant). — https://x.com/maverickecom/status/2107470108515782720
- @NotZainAgain (73L/82BM/13kV): 2026 TikTok Shop playbook incl. 1,000 free samples/mo. — https://x.com/NotZainAgain/status/2080321911918125500
- @maverickecom (57L/64BM/6kV): Affiliate made $724k GMV/30d; 3 of top 10 TTS affiliates are AI pages (claim). — https://x.com/maverickecom/status/2103161679421071603
- @maverickecom (56L/61BM/10kV): 550 AI videos/day via AI affiliate army (bulk-account; not compliant). — https://x.com/maverickecom/status/2079593540380684296
