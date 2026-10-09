# BOT.md · generate a "Native story static → advertorial (long primary text, personal-post look, illustrated comic variant)"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 1 image + 150-600 words of primary text), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@antonioventre_](https://x.com/antonioventre_/status/2083619527170871298) · A Facebook-native illustrated comic. The caption opens with a story hook ("Mom left for a business trip, leaving me alone with my stepfather Johan..." then See more) over two cartoon panels. It reads like a story post; the long primary text leads to an advertorial.
- Example: [@antonioventre_](https://x.com/antonioventre_/status/2078512377616589256) · Before/after photos are best native ad image: change creates curiosity; long copy tells story.
- Example: [@blvckledge](https://x.com/blvckledge/status/2083175922048647671) · Advertorials outperform PDP for Google Shopping traffic.
- Example: [@EcomTable](https://x.com/EcomTable/status/2100980324633063694) · Ad-spy filters: top 10-25%, image, active, 14+ day run, 2,500+ char copy -> find long-copy native winners.
- Example: [@antonioventre_](https://x.com/antonioventre_/status/2107899522353381868) · Story ad >1M reach: wife/work-wife anniversary drama, no product in first 40 words, revenge payoff.
- Example: [@tryatria_AI](https://x.com/tryatria_AI/status/2105745816828940336) · Static hook 'My sister slept with my husband' vs generic benefit lines.
- Example: [@antonioventre_](https://x.com/antonioventre_/status/2106778634006442013) · The structure I use for story ads, in video and in long primary text: 1 - Hook: the problem, not the product 2 - Problem: make it specific enough that
- Example: [@HenryCrochemore](https://x.com/HenryCrochemore/status/2081681278861021254) · spoke with an operator running paid social for a fast-growing skincare brand they connected gethookd api + mcp to turn one winning angle into hundreds
- Example: [@antonioventre_](https://x.com/antonioventre_/status/2078183710604591539) · The native ad funnel, start to finish. 1. The ad. A native image and a long story in the primary text. Built for an unaware or problem-aware person. 2

### Live paid ads in this format (2 in [adlibrary/](adlibrary/README.md), longest-running first)

- **Smooche · Aging Queens Magazine: “Designed for women 60+ or you don't pay”** (6 days live): "Designed for women 60+ or you don't pay": a 60%-off image from the "Aging Queens Magazine" page, under first-person copy "I thought foundation was over for me at 52".
- **Resilia · Daily Wellness: “Three Octobers, a small pouch arrived in her mailbox”**: "Three Octobers, a small pouch arrived in her mailbox…": a ~600-word story (Sophie, a dental hygienist…) under a dim, phone-style kitchen photo.

**Do not copy (seen in these live ads):** Fictional narrators posted from pages like "Daily Wellness" and "Cosmetic Times".

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| Image | Lo-fi illustration or real-looking phone photo of the story moment (two people, a table, a wedding) | No text on the image, or one short speech bubble |
| Primary text line 1 | - | A story hook that gets the "See more" tap: "My husband's 'work wife' came to Barbados with us..." |
| Primary text body | - | First-person story in short paragraphs, real details, the product enters as part of what happened |
| Close | - | Link to an advertorial that continues the story, not to the product page |
| Page name | - | A persona or editorial page, labelled as sponsored |

### Prompts

**Illustration (Midjourney)**

```
simple flat comic illustration, two panels, a woman at a dinner table looking at her husband laughing with a coworker, muted colours, Facebook comic style --ar 4:5
```

**Story (Claude)**

```
Write a 400-word first-person Facebook post from a 42-year-old woman. Hook in the first 12 words. Story: [situation]. [Product] appears naturally at the turning point. Short paragraphs, no hashtags, ends by pointing to the full story.
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
- [ ] Files named `F09-<concept>-<variant>`; tracking tag `utm_content=F09-<concept>-<variant>`.
- [ ] Avoid: The first line decides everything; write 20 and test 5.
- [ ] Avoid: Fiction must not be presented as a real customer testimonial; keep claims inside the advertorial truthful.
- [ ] Avoid: Facebook flags sensational personal-attribute language ("are you fat?"); write about the character, not the reader.

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
5. Name every asset `F09-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F09
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

Looks like a friend's Facebook post, not an ad: a person's name as page ("Claire Parker · Sponsored"), first line is a story ("My husband's 'work wife' came to Barbados with us. Our anniversary. His idea. 'Don't make this weird,' he said…"), a candid phone photo, **nothing about the product in the first 40 words**, then a long story (300-2,500 chars) where the product lands as the thing she used ([@antonioventre_](https://x.com/antonioventre_/status/2107899522353381868)). Click → advertorial (first-person or news-interview style) → PDP/bundle.
Illustrated variant: 2-4 comic panels with a cliffhanger caption; "the ad sells the next line of the story; the advertorial does the closing" ([@antonioventre_](https://x.com/antonioventre_/status/2083619527170871298)).
Mirror ad: the ICP "must be shocked and see herself"; news-article style copy; advertorial = interview where ICP describes her discovery ([@dep_hart](https://x.com/dep_hart/status/2076056430986309814)).

Structure: photo (candid / before-after / comic) · line 1 conflict · 3-6 short paragraphs of story · turning point (product, specific) · result · soft CTA "here's the one I got" · link.

### Why it works

Native look avoids ad-blindness; curiosity loop forces "See more" (a click that trains delivery); long copy pre-sells so advertorial CVR is high. Facebook skew older = gifting buyers.

### Production recipe

Claude writes 10 stories from review themes (gift moments, beach trip, wedding, divorce glow-up, mom/daughter); photo = real customer UGC (permission) or staged phone photo with LC piece visible; advertorial on Shopify page template (or Replo/Zipify): headline story, 3 reasons, real reviews, offer block (7 for $85), guarantee.

## Reference examples

See [examples/README.md](examples/README.md) (27 posts). Top 5:

- @EcomTable (285L/418BM/21kV): Ad-spy filters: top 10-25%, image, active, 14+ day run, 2,500+ char copy -> find long-copy native winners. — https://x.com/EcomTable/status/2100980324633063694
- @antonioventre_ (270L/389BM/20kV): Story ad >1M reach: wife/work-wife anniversary drama, no product in first 40 words, revenge payoff. — https://x.com/antonioventre_/status/2107899522353381868
- @antonioventre_ (131L/233BM/18kV): Illustrated story-based ad: long primary text, ad sells next line, advertorial closes. — https://x.com/antonioventre_/status/2083619527170871298
- @tryatria_AI (73L/98BM/4kV): Static hook 'My sister slept with my husband' vs generic benefit lines. — https://x.com/tryatria_AI/status/2105745816828940336
- @dep_hart (65L/90BM/5kV): Native ads: mirror ad (ICP sees herself), news-article copy, interview-style advertorial. — https://x.com/dep_hart/status/2076056430986309814
