# BOT.md · generate a "Emotional + relatable TikTok slideshow (share-bait story slides)"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 5-8 slides, 1080x1920), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@?](https://x.com/?/status/2099496707209994736) · An emotional relatable slideshow: "I'm 24 years old and I'm moving back into my childhood bedroom after losing my job..." over a photo of a young woman, with the story continuing across the slides.
- Example: [@simonecanciello](https://x.com/simonecanciello/status/2092704268734099547) · this $100k/month relationship app is going viral with this format. 6.7M views and 578k likes. hook + demo, relatable for women. people are searching f
- Example: [@consumerxai](https://x.com/consumerxai/status/2092629155036987751) · ‼️Tiktok Outlier Alert ‼️ 📉 585K Views, 133K Likes, 322 Comments, 28K Shares, 11K Saves 🧐What this is: > A silent travel-footage slideshow you can use
- Example: [@tellenne_](https://x.com/tellenne_/status/2106759383656849698) · A skincare app promoting across 20 US TikTok accounts (no ads, $0.21 CPM). I analyzed 30 of its carousels in TokPortal: • 786,527 total views • 3,152 
- Example: [@g_buildz_apps](https://x.com/g_buildz_apps/status/2108234459241935255) · "Post emotional slideshows on TikTok" — one slideshow: 13.3K views, 2,881 likes, 802 shares, 313 saves (TikTok Studio screenshot).
- Example: [@Dkevs_](https://x.com/Dkevs_/status/2100425887636472312) · $200K MRR app via TikTok slideshows; don't overcomplicate with clippers.
- Example: [@BrunoF566](https://x.com/BrunoF566/status/2095543004626890752) · TikTok slideshows are being used completely wrong. Most people treat them like a lottery ticket. Post the same recycled hooks, hope one goes viral, th

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| Slide 1 | Relatable photo of a woman (AI or licensed) | "I'm 24 and I just moved back into my childhood bedroom" |
| Slides 2-5 | Story continues, one line per slide | Emotional, specific details |
| Slide 6 | Turn: the small thing that helped (the product as a gift) | One line |
| Slide 7 | Hopeful close | "send this to someone who needs it" |

### Prompts

**Claude**

```
Write 10 six-slide TikTok slideshow stories, one line per slide, first person, relatable life moments for women 20-35, product appears as one small comfort in slide 5 or 6.
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
- [ ] Files named `F56-<concept>-<variant>`; tracking tag `utm_content=F56-<concept>-<variant>`.
- [ ] Avoid: Stories presented as true must be true or clearly fiction.
- [ ] Avoid: Share-bait endings work; buy-now endings do not.

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
5. Name every asset `F56-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F56
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

A 4-8 slide photo-mode story built around a relatable emotional moment (a mother, a breakup, a friend's birthday at 5am), told in short first-person lines over candid photos; the product appears naturally in one slide as part of the moment. Optimised for shares and saves rather than clicks.

### Why it works

- Emotion + relatability drives shares (802 shares on 13.3K views ≈ 6% share rate).
- "Put them in the moment" POV openers are among the most-saved hook types.
- Cheap; tests emotional angles before paying for video.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| Slide 1 | Candid photo: mom's hands; text "my mom never bought herself jewelry" | — |
| Slide 2 | "she always said 'it'll just turn green anyway'" | — |
| Slide 3 | "so for her 60th I got her one she can wear in the garden, the shower, everywhere" | — |
| Slide 4 | Close-up LC necklace on her | — |
| Slide 5 | "she hasn't taken it off in 4 months" | — |
| Slide 6 | "call your mom" (no hard CTA; product tag/comment pin) | — |

### Hooks

- "It's 5am on her birthday…"
- "my mom never bought herself jewelry"
- "POV: your best friend remembers the necklace you pointed at 8 months ago"
- "things my grandma told me about jewelry"

### Production recipe

1. Write stories from real customer reviews/notes (with permission) or as the brand's/founder's own story.
2. Candid, warm photos (not studio); 6-8 words per slide.
3. Post 1/day on an owned page; pin a comment with the product.

### Existing bot prompt

```
From these real customer stories {{REVIEWS}}, write 8 emotional 6-slide slideshow scripts (≤12 words per slide, first person, the LC piece appears once naturally). Never invent a story and present it as a real customer's.
```

### Variants to test

- Opener type (POV / name the viewer / moment)
- Slide count

## Reference examples

See [examples/README.md](examples/README.md) (15 posts). Top 5:

- @consumerxai (12L/18BM/1kV): 30 most-SAVED app TikTok hooks in 6 types (POV moment, name the viewer, disbelief, signs/lists, result first, pattern interrupt); save rate > views as signal. — https://x.com/consumerxai/status/2107471216126906682
- @g_buildz_apps (7L/5BM/390V): "Post emotional slideshows on TikTok" — one slideshow: 13.3K views, 2,881 likes, 802 shares, 313 saves (TikTok Studio screenshot). — https://x.com/g_buildz_apps/status/2108234459241935255
- @g_buildz_apps (0L/1BM/172V): Emotional slideshows do better every time and convert better (claim). — https://x.com/g_buildz_apps/status/2094812455847309758
- @simonecanciello (47L/77BM/15kV): this $100k/month relationship app is going viral with this format. 6.7M views and 578k likes. hook + demo, relatable for women. people are searching for “long d — https://x.com/simonecanciello/status/2092704268734099547
- @consumerxai (7L/11BM/1kV): Outlier: silent travel-footage slideshow with long-distance text hook → widget demo, 585K views/28K shares. — https://x.com/consumerxai/status/2092629155036987751
