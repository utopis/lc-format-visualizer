# BOT.md · generate a "Us-vs-copycat screen-scroll comparison (and comparison page)"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 20-45s screen recording, 1080x1920), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@Nate_Google_](https://x.com/Nate_Google_/status/2104963469548085713) · A plain warning static: a red triangle and "IMPORTANT NOTICE: Please Check Before Purchasing", explaining that replicas use the brand's images and that you should only buy from the real site. It plays the copycat problem as a public-service notice.
- Example: [@ultimategrafiks](https://x.com/ultimategrafiks/status/2090399839309738284) · I love designing static ads because every product comes with a different story and creative challenge. CALLOUT, US vs THEM, DTC &amp; UGC, I love crea
- Example: [@EiyanDickerson](https://x.com/EiyanDickerson/status/2088266872194023737) · 4 Static Ads. 1 Angle. 1. Before &amp; After 2. Feature Callout 3. Headline Callout 4. Us vs Them A Moisturizer built for the heat☀️ https://t.co/jmYh
- Example: [@Hashir_Shaikh_](https://x.com/Hashir_Shaikh_/status/2096337779412304217) · We make 1,000+ statics every month. Around 10% are Us vs Them. Because showing the difference can be more powerful than simply talking about your prod

### Live paid ads in this format (3 in [adlibrary/](adlibrary/README.md), longest-running first)

- **Penrose Skin: "Wanna pull? You need this fragrance" dupe yapper (Penrose)** (89 days live): A man to camera: "Wanna pull fine shit like this, trust me you need to get this fragrance… it literally smells like [designer], the most identical fragrance… a lot more affordable… lasts a lot longer." 28 s.
- **Penrose Skin: Talking-jar CGI rivalry ("You copied me! That's theft!")** (89 days live): A CGI designer-cologne bottle argues with the Penrose jar: "You copied me! That's theft!" / "Can't copyright a scent, babe… And I've got your exact same scent. Plus pheromones. For $220 less." 43 s.
- **Penrose Skin: "I stopped buying $400 colognes" price-anchor demo** (89 days live): Overlay: "I stopped buying $400 colognes… and started smelling like this", a red arrow pointing at the jar, "$ave for ONLY $XX". 15 s.

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| 0-3s | Screen recording of a marketplace search for "gold necklace", copycat listings | VO: "Before you buy a gold necklace on Amazon, watch this." |
| 3-20s | Scrolls and zooms into tell-tale details (plating, "gold tone", 1-star reviews mentioning green skin) | VO explains how to tell real from cheap |
| 20-35s | Switch to the brand's product page / real product in hand | What the real one has (14K PVD, warranty) |
| End | Product + offer | "only from [brand].com" |

### Prompts

**Recording**

```
iPhone screen recording at 60fps, then crop to 9:16, add zoom-ins with CapCut keyframes on every claim, circle tool in red.
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
- [ ] Files named `F16-<concept>-<variant>`; tracking tag `utm_content=F16-<concept>-<variant>`.
- [ ] Avoid: Do not name or show a specific competitor's brand in a way that implies something false about them; blur names.
- [ ] Avoid: Every "how to tell" point must be true and checkable.
- [ ] Avoid: Static version: warning notice ("Please check before purchasing") works too, as in the featured example.

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
5. Name every asset `F16-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F16
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

Screen recording of an iPhone scrolling marketplace listings of look-alike products while a VO explains how to tell the difference (materials, plating, reviews mentioning tarnish), then cuts to the real product. ([@Nate_Google_](https://x.com/Nate_Google_/status/2104963469548085713)).

## Reference examples

See [examples/README.md](examples/README.md) (10 posts). Top 5:

- @Nate_Google_ (258L/461BM/23kV): Us-vs-copycat ads: iPhone scrolling fake Amazon listings explaining the difference - high CVR MOF. — https://x.com/Nate_Google_/status/2104963469548085713
- @adamtaylorl (36L/36BM/3kV): Dead in 2026: polished studio, "hey guys" UGC, discount statics, founder-story VSLs. Printing: ugly advertorial statics, long-form yapper, comment-reply hooks,  — https://x.com/adamtaylorl/status/2086814826177679660
- @antonioventre_ (39L/23BM/3kV): 99% of comparison ads send click to PDP; send to dedicated comparison page instead. — https://x.com/antonioventre_/status/2084404696840569332
- @alexpagepilot (11L/19BM/1kV): Top 5 dropship formats: UGC problem/solution, "TikTok made me buy it", us vs them split, founder talking head (retargets 2-3x), text-overlay slideshow. — https://x.com/alexpagepilot/status/2099438014456045990
- @piyush_jn (8L/0BM/722V): @abdushodmonov @chuckiegregory scaled Primal Queen subscription revenue from $2M to $100M+ in under 2 years. Female-focused beef organ supplements. Now in Targe — https://x.com/piyush_jn/status/2077070874084315386
