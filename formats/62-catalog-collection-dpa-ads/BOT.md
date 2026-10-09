# BOT.md · generate a "Catalog / collection / dynamic product ads (Advantage+ catalog, catalog video, collection + Instant Experience lookbook)"

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
5. Name every asset `F62-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F62
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

Let Meta pick the product per person: Advantage+ catalog ads (dynamic product ads) with catalog video and branded frames; collection ads with a lifestyle hero video over 3-4 product tiles opening an Instant Storefront/Lookbook; creator Partnership ads paired with the catalog.

### Why it works

- Shows the exact piece someone viewed (abandoned cart / browse retargeting).
- Catalog video/lifestyle frames beat plain packshots.
- Lookbook keeps browsing inside the app (fast load).

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| Hero | 15s lifestyle video: stack on wet skin | — |
| Tiles | 4 bestsellers from catalog with price | — |
| Instant Experience | Lookbook: "Beach stack", "Office stack", "Bridesmaid stack" → PDPs | — |
| DPA frame | Catalog image + branded frame "14K PVD · waterproof · any 7 for $85" | — |

### Hooks

- Hero line: "Shower-proof gold. Pick your 7."
- DPA frame: "Still thinking about it? It's waterproof."
- Lookbook: "Shop the stack"

### Production recipe

1. Clean Shopify→Meta catalog feed (titles with "14K PVD waterproof", lifestyle images, video where possible).
2. Product sets: bestsellers, necklaces, huggies, gift sets, bundle-eligible.
3. Branded catalog frames (price/offer must match).
4. Pair top creator Partnership ads with catalog (F43).

### Existing bot prompt

```
Audit this catalog feed sample {{FEED}}: rewrite titles/descriptions for search + clarity (≤65 chars titles), propose 5 product sets, 3 catalog frame overlays, and a collection-ad hero script.
```

### Variants to test

- Packshot vs lifestyle catalog image
- Frame vs no frame
- Collection vs carousel

## Reference examples

See [examples/README.md](examples/README.md) (4 posts). Top 5:

- @danpantelo (0L/0BM/0V):  — https://x.com/danpantelo/status/1640330448818544640
- @torovictorioso (17L/2BM/4kV): $SNAP today introduces the .. The "Commerce Power Pack" Bundle: Packaging some existing e-commerce performance tools together into a dedicated, end-to-end perfo — https://x.com/torovictorioso/status/2098135439458877901
- @_reachsumit (9L/6BM/388V): SMART: LLM-Augmented Hybrid Retrieval for Dynamic Product Ads Snap routes users between keyword BM25 retargeting and LLM-driven prospecting queries, cutting LLM — https://x.com/_reachsumit/status/2081996559710130535
- @wearetheselect (4L/1BM/1kV): most y'all just run all products dpa ads don't forget to test into new product sets: best sellers, new drops, shirts, bottoms, hats, socks, etc you can go super — https://x.com/wearetheselect/status/2076807089280668077
