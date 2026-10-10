# BOT.md · generate a "Persona aesthetic slideshow account with one recurring caption template"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: Daily 4-6 slide TikTok photo-mode slideshows from one aesthetic account), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@yurahulei](https://x.com/yurahulei/status/2108224536902815967) · Three TikTok profiles of AI persona pages, each a consistent aesthetic girl (beach, sunset, bikini photos) posting templated captioned slideshows at scale.
- Example: [@rsalimx](https://x.com/rsalimx/status/2108629140480168133) · nah bro 😭 this is a fitness account with nothing in the bio 😭💔 every post is the exact same mirror selfie she’s prolly pulling 20m+ views a month and 
- Example: [@onlinedopamine](https://x.com/onlinedopamine/status/2082813772373098530) · these are the types of outsized organic views you get on new accounts when you nail &gt; understanding of your target audience (= pinterest aesthetic 
- Example: [@g_buildz_apps](https://x.com/g_buildz_apps/status/2096288782517457130) · I started this account last month Over 1M+ views just on slideshows This brought me 10,000 downloads btw One slideshow account. https://t.co/plkjEqnwZ
- Example: [@yassratti](https://x.com/yassratti/status/2100554319070212573) · bro is doing $9k a month with a single tiktok slideshow account 😭 that's wild as fuck and it's your wake up call build an app that fits a format explo
- Example: [@onlinedopamine](https://x.com/onlinedopamine/status/2077706055656558799) · this slideshow account is literally leaving money on the table, it's almost infuriating the account owner is going viral on basically every second pos

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| Cover slide | Aesthetic photo in the persona's world (morning coffee, beach bag, mirror selfie with the stack) | Same caption template every post: "things that just make sense: ___" |
| Slides 2-5 | One "thing that makes sense" per slide; the product is one of them, never the first | e.g. "a necklace you never take off" |
| Last slide | A soft pointer | "my stack is in my bio" |
| Audio | Trending soft sound at low volume | - |

### Prompts

**Caption template**

```
Pick ONE template ("things that just make sense", "soft life essentials", "signs you're the friend with good taste") and reuse it on every post for 30 days.
```

**Image sourcing**

```
Shoot a library of 100 aesthetic photos in one day (same light, same palette), then mix and match; label any AI images as AI.
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
- [ ] Files named `F85-<concept>-<variant>`; tracking tag `utm_content=F85-<concept>-<variant>`.
- [ ] Avoid: AI persona accounts must be labelled as AI.
- [ ] Avoid: One template, many posts; changing it weekly resets the account.
- [ ] Avoid: The product must be one tip among several; if every slide sells, it reads as an ad.

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
5. Name every asset `F85-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F85
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

A themed "persona" account (e.g. an aesthetic travel girl) posts photo slideshows of aspirational moments with the same short meme caption on the cover every time. The bio carries the CTA. The repeated caption becomes a recognisable series; volume finds the outliers.

### Why it works

- One proven caption × endless images = cheap volume testing.
- Aspirational photos are inherently shareable.
- The bio CTA avoids an in-post sales pitch.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| Cover | Beach sunset, wearer in profile, necklace catching light | Caption: "she never takes her jewelry off" |
| Slides 2-5 | Ocean, shower, dinner, airport, same chain | — |
| Bio | "waterproof 14K stacks · louisecarter.com" | — |

### Hooks

- "she never takes her jewelry off"
- "she wears it in the ocean"
- "her jewelry has been to 9 countries"

### Production recipe

1. ONE (or a few) clearly LC-affiliated accounts; no account farms, no bought/warmed accounts.
2. Use only LC-owned, creator-licensed or customer-consented photos (not Pinterest scrapes).
3. Pick 1 caption template; post daily for 30 days; keep the outliers.

### Existing bot prompt

```
Write 20 one-line cover captions in the "she never takes her jewelry off" family for an LC aesthetic slideshow account, plus a 5-slide image brief per caption using only owned/licensed photos.
```

### Variants to test

- Caption template
- Travel vs everyday imagery

## Reference examples

See [examples/README.md](examples/README.md) (9 posts). Top 5:

- @yurahulei (0L/0BM/0V): AI agent posting 1000s of TikTok slideshows: rented US iPhones (Minionix), warmed accounts, 100K Pinterest image DB; screenshots: persona accounts, same caption — https://x.com/yurahulei/status/2108224536902815967
- @rsalimx (0L/0BM/0V):  — https://x.com/rsalimx/status/2108629140480168133
- @rsalimx (76L/122BM/8kV): Claim slideshows convert harder than videos; it's about finding the right format. — https://x.com/rsalimx/status/2090094780864713021
- @onlinedopamine (46L/73BM/5kV): this slideshow account is literally leaving money on the table, it's almost infuriating the account owner is going viral on basically every second post what's m — https://x.com/onlinedopamine/status/2077706055656558799
- @yassratti (60L/54BM/5kV): bro is doing $9k a month with a single tiktok slideshow account 😭 that's wild as fuck and it's your wake up call build an app that fits a format exploit that fo — https://x.com/yassratti/status/2100554319070212573
