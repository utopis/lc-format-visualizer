# BOT.md · generate a "Listicle save-carousel (one item per slide)"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 6-10 slides, 1080x1350 or 1080x1920), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@rsalimx](https://x.com/rsalimx/status/2108259483902513153) · Two screenshots: a recipe app's App Store page (Daily Bite, "Save Any Recipe Anywhere") and the TikTok profile that drives it ("Success Fitness"), a grid of one-meal-per-slide recipe carousels, many past 1M views. The carousel is the content; the app is the save-it-for-later tool.
- Example: [@rsalimx](https://x.com/rsalimx/status/2107517609960702306) · Running-girl ICP page; app shows on slide 4 of 5 right before last tip (can't get full list without seeing it).
- Example: [@PerezHatesAI](https://x.com/PerezHatesAI/status/2106779894785188006) · This is wild 😭 4.3M views. 250K saves. On a "weird habits" slideshow. No product demo. No feature dump. Just aesthetic slides of habits that "actually
- Example: [@_afterblossom_](https://x.com/_afterblossom_/status/2095194062756413781) · Throwing back this piece to see in the new carousel format https://t.co/rOPT5RDzKO
- Example: [@rustybrick](https://x.com/rustybrick/status/2085121962976661782) · ChatGPT Ads Product Updates including multi-product carousel format for product feed campaigns https://t.co/TWMRyCOCy2
- Example: [@glenngabe](https://x.com/glenngabe/status/2085345793343377737) · ChatGPT Ads update -&gt; ChatGPT is testing a multi-product carousel format for product feed campaigns "We’ve started testing a carousel format for pr

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| Slide 1 (cover) | Best-looking item photo, full bleed, bright | Warm headline in big rounded type: "7 ways to wear gold FOR YOU" / "gift ideas for the friend who never takes jewelry off" |
| Slides 2-8 | One item per slide, same framing and light, item centred | Item name + one useful line (price, why it works, how to use). Number in the corner (2/8) |
| One middle slide | The product, styled like every other item | Same template, so it reads as one of the list |
| Last slide | Collage of all items | "save this so you don't forget" + small handle |

### Prompts

**Canva / Figma**

```
Template: 1080x1350, photo 100% bleed, 8% black gradient top, headline 72-96px rounded sans (e.g. "Poppins Bold"), item caption 40px, slide counter top-right 28px.
```

**Claude**

```
Give me 15 save-worthy carousel topics for [audience] where [product] fits naturally as one of 6-8 items. For each: cover headline with "for you" or a direct address, the item list, and one useful line per item.
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
- [ ] Files named `F02-<concept>-<variant>`; tracking tag `utm_content=F02-<concept>-<variant>`.
- [ ] Avoid: A cover that does not promise a useful list will not get saves; test 3 covers on the same list.
- [ ] Avoid: If the product slide looks different (studio shot among phone shots) it reads as an ad.
- [ ] Avoid: Keep text above the bottom 20% so TikTok UI does not cover it.

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
5. Name every asset `F02-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F02
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

Cover slide with a big, warm "for you" headline over a hero image ("High protein dinner ideas FOR YOU", "5 weeknight dinners for your lazy ass", "dinners to make for your husband this week") then **one item per slide**, each a beautiful photo + 1-line label. Product/app line sits in bio ("Get our app with all 500+ recipes") or on the last slide ("all of this, in your pocket"). Example account: @success.fitness — 1.4M followers, 25.4M likes, posts at 16-42M views ([@rsalimx](https://x.com/rsalimx/status/2108259483902513153)).

### Why it works

People save lists on instinct (utility), share to partners/friends ("make this for me"), and return to it; saves + shares push distribution. Zero face, zero filming.

### Hooks

"[N] [things] for your [lazy ass / husband / 9-5 week]", "[season] [things] to [do]", "[Result] ideas FOR YOU (with [details])", "save this for [occasion]".

### Production recipe

Photos: LC product photography + customer UGC (with permission) + AI-styled on-body shots (see F20). Template in Canva: cover + 5-8 item slides. Agent prompt (adapted from @MaxHirsch13): *"Make a 7-slide carousel for Louise Carter: slide 1 wide candid photo of [persona] with hook '[N] waterproof stacks for [occasion]' in white serif text; slides 2-7 one stack per slide, label = piece names + price; last slide 'all pieces 14K PVD, shower-proof'."*

## Reference examples

See [examples/README.md](examples/README.md) (13 posts). Top 5:

- @MaxHirsch13 (144L/398BM/6kV): Exact agent prompt for 6-slide carousel: candid wide photo + '5 ways to get [result]' hook, slides 2-6 one tip each. — https://x.com/MaxHirsch13/status/2108340891601748034
- @rsalimx (149L/213BM/9kV): Recipe slideshows (one meal per slide) hit 40M views; app = 'all of this in your pocket'. Save-bait listicle. — https://x.com/rsalimx/status/2108259483902513153
- @rsalimx (120L/200BM/6kV): Running-girl ICP page; app shows on slide 4 of 5 right before last tip (can't get full list without seeing it). — https://x.com/rsalimx/status/2107517609960702306
- @PerezHatesAI (48L/68BM/2kV): This is wild 😭 4.3M views. 250K saves. On a "weird habits" slideshow. No product demo. No feature dump. Just aesthetic slides of habits that "actually work". An — https://x.com/PerezHatesAI/status/2106779894785188006
- @_afterblossom_ (3932L/391BM/35kV): Throwing back this piece to see in the new carousel format https://t.co/rOPT5RDzKO — https://x.com/_afterblossom_/status/2095194062756413781
