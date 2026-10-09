# BOT.md · generate a "Persona aesthetic slideshow account with one recurring caption template"

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

See [examples/README.md](examples/README.md) (8 posts). Top 5:

- @yurahulei (0L/0BM/0V): AI agent posting 1000s of TikTok slideshows: rented US iPhones (Minionix), warmed accounts, 100K Pinterest image DB; screenshots: persona accounts, same caption — https://x.com/yurahulei/status/2108224536902815967
- @rsalimx (76L/122BM/8kV): Claim slideshows convert harder than videos; it's about finding the right format. — https://x.com/rsalimx/status/2090094780864713021
- @onlinedopamine (46L/73BM/5kV): this slideshow account is literally leaving money on the table, it's almost infuriating the account owner is going viral on basically every second post what's m — https://x.com/onlinedopamine/status/2077706055656558799
- @yassratti (60L/54BM/5kV): bro is doing $9k a month with a single tiktok slideshow account 😭 that's wild as fuck and it's your wake up call build an app that fits a format exploit that fo — https://x.com/yassratti/status/2100554319070212573
- @chesny (121L/17BM/14kV): You swiped through that slideshow 3 times today. Nobody filmed it. Nobody edited it. Watch until 0:25. That's where it breaks down the hook. Find a slideshow ac — https://x.com/chesny/status/2098080607125561633
