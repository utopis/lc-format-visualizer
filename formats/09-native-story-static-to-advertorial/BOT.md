# BOT.md · generate a "Native story static → advertorial (long primary text, personal-post look, illustrated comic variant)"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

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
- @antonioventre_ (241L/365BM/20kV): Story ad >1M reach: wife/work-wife anniversary drama, no product in first 40 words, revenge payoff. — https://x.com/antonioventre_/status/2107899522353381868
- @antonioventre_ (131L/233BM/18kV): Illustrated story-based ad: long primary text, ad sells next line, advertorial closes. — https://x.com/antonioventre_/status/2083619527170871298
- @tryatria_AI (73L/98BM/4kV): Static hook 'My sister slept with my husband' vs generic benefit lines. — https://x.com/tryatria_AI/status/2105745816828940336
- @dep_hart (65L/90BM/5kV): Native ads: mirror ad (ICP sees herself), news-article copy, interview-style advertorial. — https://x.com/dep_hart/status/2076056430986309814
