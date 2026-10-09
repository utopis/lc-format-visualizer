# BOT.md · generate a "AI UGC outlier-remake lab (find outliers → AI test on organic → remake winners with real creators → paid)"

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
5. Name every asset `F53-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F53
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

A production system, not a single look: research customers deeply → scrape niche videos and pick OUTLIERS (vs the creator's own average, e.g. 12×) → reverse-engineer hook/open question/sequence/payoff → build a believable AI starting frame and test one take → batch → post to 4 platforms from one scheduler → judge each platform separately → give winning concepts to real creators and put ad money behind them.

### Why it works

- Outlier-vs-own-baseline is a stronger signal than raw views (@jakecastilloooo).
- AI videos are cheap tests; real creators remake winners for trust.
- Changing one variable at a time makes results interpretable.
- Never let the model invent product details — use real footage of the product.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| Step 1 | Context pack: PDP, reviews, support tickets, surveys | Claude project |
| Step 2 | Apify TikTok/IG scrapers → outlier list (views ÷ creator median) | HTML board with select buttons |
| Step 3 | Video analyzer → hook, unanswered question, sequence, payoff | — |
| Step 4 | Starting frame from a real UGC reference: angle, skin detail, natural hands, mic | Image model |
| Step 5 | One test take (static/handheld, energy, exact dialogue) → check lip sync, hands, face drift | Seedance/Kling |
| Step 6 | Edit with REAL LC product footage; captions; review at phone size | FFmpeg/editor |
| Step 7 | Schedule to TikTok/IG/Shorts/FB | Postiz-type scheduler (drafts reviewed by a human) |
| Step 8 | Winners → real creator remake (F43) → Meta paid | Omni |

### Hooks

- Outlier-derived (examples): "I tested the internet's favorite jewelry hack…"
- "POV: you forgot you were wearing it in the ocean"
- "Things I stopped doing after 30: taking off my necklace"

### Production recipe

1. Build context pack in /lc-mkt (PDP facts, top 200 reviews, top 50 support questions).
2. Outlier research weekly: jewelry, gifting, "waterproof jewelry", GRWM niches; outlier = ≥5× creator median.
3. Analyze top 10 → pick 3 formats → 1 variable per test.
4. AI frame rules: real UGC reference, no text on face, natural hands, plausible audio source; product shots must be REAL LC footage composited (no AI-invented jewelry).
5. Post to an LC-owned test account (disclosed as AI where required); judge per platform at fixed windows.
6. Concept with signal → brief 3-5 real creators (F43) → Partnership ads.

### Existing bot prompt

```
Context: {{LC_CONTEXT_PACK}}. Here are scraped videos with views and each creator's median {{SCRAPE}}. 1) Rank by outlier ratio; 2) for top 10 give hook (first 2s), unanswered question, sequence, payoff, and why it worked; 3) propose 3 LC adaptations changing only ONE variable each; 4) write starting-frame and animation prompts (camera static/handheld, energy, exact ≤30-word dialogue, what must stay consistent). Product must be shown with real LC footage — mark insert points.
```

### Variants to test

- Model (Seedance vs Kling vs Omni)
- Hook vs character vs setting (one at a time)
- AI vs real-creator remake of same script

## Reference examples

See [examples/README.md](examples/README.md) (23 posts). Top 5:

- @jakecastilloooo (984L/3090BM/290kV): Ex-Cal AI UGC lead's full AI UGC workflow (article): customer context → outlier videos vs creator baseline → reverse-engineer → believable first frame → test ta — https://x.com/jakecastilloooo/status/2107873317369581751
- @0xDepressionn (18L/14BM/2kV): Summary of Jake Castillo's workflow: AI videos as cheap organic tests, then ad money behind winners. — https://x.com/0xDepressionn/status/2107918489587507606
- @carlynorthmedia (0L/0BM/69V): Know when to stop iterating a winner: reusing the same hook causes audience + algorithm fatigue. — https://x.com/carlynorthmedia/status/2107565970197782530
- @traqscales (0L/0BM/0V): Once app: 22.5M views from 2 AI UGC creators (one 13M, 9 >100K) — AI bride crying at her reception, "we gave every guest a camera instead of hiring more photogr — https://x.com/traqscales/status/2108113354178932920
- @ai_cult1 (0L/0BM/49V): Cal AI growth was paid, not organic: creator roster, affiliate program, MrBeast sponsorship, in-house daily ad creative ($40M in 12 months). — https://x.com/ai_cult1/status/2092368368968049118
