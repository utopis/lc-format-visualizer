# BOT.md · generate a "Green-screen reaction over a proven winner + reply-to-comment overlay"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 20-45s, 1080x1920), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@claireonvideo](https://x.com/claireonvideo/status/2098103517680402637) · A creator in front of a green screen of news articles (Hollywood box office, Warner Bros) reacting and explaining, then the green screen switches to the product (the "Dailies" newsletter signup page). It is UGC commentary with the background as the visual.
- Example: [@evodawson](https://x.com/evodawson/status/2103985895443398988) · Your UGC isn't converting because your creators have no credibility. Borrow the founder's. Have them green screen and react to a video from the founde
- Example: [@generatedbyann](https://x.com/generatedbyann/status/2061823394270843156) · I started noticing an uptick of this video format across ads and socials. The green screen explainer style mixed with rotating visuals/photos in the b
- Example: [@jsocialstoryugc](https://x.com/jsocialstoryugc/status/2053877587928092845) · UGC example using green screen format! This style continues to perform SO well for brands: ⚫️ Great pacing ⚫️ Gives audience a good visual reference T
- Example: [@naturallyshan](https://x.com/naturallyshan/status/2064745463513768389) · Don’t be afraid to use green screen in your concepts for beauty brands!📈👇 The green screen format is high converting because it gets people interested
- Example: [@jennamediaco](https://x.com/jennamediaco/status/2074943138205176288) · Want to make UGC videos that actually convert? 💸 Here is the exact strategy behind one of my winning videos: 📱 The "Scroll" Hook: Use a TikTok feed gr
- Example: [@ugcwithvan](https://x.com/ugcwithvan/status/1999270533557285146) · Split screen videos WORK >> This brand had a winning video that consisted of a similar structure with green screen visuals but wanted to test differen
- Example: [@TheJeremyHaynes](https://x.com/TheJeremyHaynes/status/2092620077946614206) · Ranking every ad creative format worst->best (video).
- Example: [@sincerelydawnUG](https://x.com/sincerelydawnUG/status/2078944255465439652) · Here’s a recent ad where the brand requested green screen ads while the product ships! Portfolio: https://t.co/8dOkKM0Yrz Email: sincerelydawn.ugc@gma

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| 0-2s | Creator in the lower half, green-screen background: a screenshot of a viral comment or the brand's own top post | Reads the comment: "someone asked if it really survives the ocean..." |
| 2-20s | Background switches to proof (a video of the product in water) | Creator explains, points at the background |
| 20-35s | Background: product page | Offer |
| Comment-reply variant | TikTok/IG "reply to comment" sticker on the first frame | Answers the real comment |

### Prompts

**CapCut**

```
Effects > Green screen (or TikTok "Green Screen" effect), creator cut-out at 55% height bottom-left, background image scaled to fill, add a subtle drop shadow under the creator.
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
- [ ] Files named `F18-<concept>-<variant>`; tracking tag `utm_content=F18-<concept>-<variant>`.
- [ ] Avoid: Only react to content you own or have permission to use.
- [ ] Avoid: Real comments only; do not invent a comment to reply to.

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
5. Name every asset `F18-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F18
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

Creator in front of a green-screen background showing **LC's own winning ad/post** (or a screenshot of a viral comment), reacting/explaining. Comment-reply: TikTok/IG comment bubble sticker ("does this actually survive the ocean??") + answer video.

## Reference examples

See [examples/README.md](examples/README.md) (11 posts). Top 5:

- @adamtaylorl (139L/203BM/13kV): Tier list of ecom formats: F = AI UGC, street interviews, read scripts; B = founder, testimonial compilations, listicle statics... — https://x.com/adamtaylorl/status/2097641383355879452
- @CEO_Vlad (88L/169BM/5kV): AI UGC formats tiered: S = podcast, talking head, in-car... — https://x.com/CEO_Vlad/status/2096569603761827953
- @adamtaylorl (36L/36BM/3kV): Dead in 2026: polished studio, "hey guys" UGC, discount statics, founder-story VSLs. Printing: ugly advertorial statics, long-form yapper, comment-reply hooks,  — https://x.com/adamtaylorl/status/2086814826177679660
- @Ecombos_Ai (28L/26BM/2kV): 10 AI UGC styles: talking-head testimonial, product-in-hand, first-try reaction, fake podcast, street interview, comment reply, unboxing, DITL/GRWM, before/afte — https://x.com/Ecombos_Ai/status/2103180929057407425
- @williamkast_ (12L/14BM/967V): 15 formats to repackage winners into (scaled to $30k/day on 3-4 angles): founder, yapper, AI animation, voiceless overlay, carousel, reply ad, text wall, review — https://x.com/williamkast_/status/2083616523134841035
