# BOT.md · generate a "Offer-architecture ads: build-your-own bundle / any-N picker / mystery box / free-plus-shipping"

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
5. Name every asset `F86-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F86
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

Ads whose creative is the offer mechanic itself: a picker grid "choose any 7" with a running counter, a mystery-box reveal, "free chain, just pay shipping" for first orders, or tiered "buy 4 get 20%". The landing page is the matching picker or offer page, not a generic PDP.

### Why it works

- The mechanic is the hook: choosing feels like play, and the flat price removes math.
- Offer-forward creative converts warm and product-aware traffic.
- A matching picker lander keeps the promise from the ad.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0-3s | Screen recording: tapping 7 pieces into a bundle builder, counter 1/7 → 7/7 | "Any 7. $85. Go." |
| 3-12s | Pieces dropping into a gift box | — |
| 12-15s | Price card | "Waterproof 14K PVD" |

### Hooks

- "Pick any 7. $85. That's it."
- "Build your stack in 20 seconds"
- "Mystery 3-piece box: guess what's inside"
- "First chain free, just pay shipping" (test only if margins allow)

### Production recipe

1. Record the real picker flow on louisecarter.com (or build one).
2. Make 3 mechanics: picker, mystery box, gift-box build.
3. Send each to the matching page with the bundle preloaded.

### Existing bot prompt

```
Write 5 offer-architecture ads for LC: picker screen-record script, mystery box reveal, gift-box build, "your stack, your rules" static, tiered offer static. Match each to a landing-page spec (preloaded cart or picker).
```

### Variants to test

- Mechanic
- Cold vs retargeting

## Reference examples

See [examples/README.md](examples/README.md) (6 posts). Top 5:

- @FedotOff90 (238L/632BM/20kV): 7,500+ winning Meta ads sorted by format across public boards (top-50 DTC, beauty, natives, listicles, shock & gross, BOFU). — https://x.com/FedotOff90/status/2093350155751924213
- @FedotOff90 (175L/385BM/47kV): 6 lander/advertorial types (news mimic, story, listicle, quiz, authority, comparison) — 53-format lander database. — https://x.com/FedotOff90/status/2094854572623675832
- @FedotOff90 (145L/318BM/11kV): 24 landing page formats with live ad→lander pairs (breaking news, investigation, as-seen-on-TV, doctor warning…). — https://x.com/FedotOff90/status/2092382176738202057
- @FedotOff90 (110L/208BM/9kV): 37 formats printing (with days active): AI podcast 280d, report card, iPhone Notes, text on skin, Reddit, cross-out, fake PDP, tier list, myth vs fact, zero sta — https://x.com/FedotOff90/status/2104949773539442831
- @FedotOff90 (35L/42BM/7kV): 335 of top BOFU ads in ONE swipe file here: https://t.co/39G7hAlLer https://t.co/rsZzZSpMFd https://t.co/CJ695Dqbfc — https://x.com/FedotOff90/status/2091884660871585977
