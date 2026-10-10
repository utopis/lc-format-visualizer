# BOT.md · generate a "AI UGC outlier-remake lab (find outliers → AI test on organic → remake winners with real creators → paid)"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: System: weekly loop (find outliers → AI test → real remake → paid)), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@rathikrishnav](https://x.com/rathikrishnav/status/2056472046192951468) · A split-screen test: on the left the brand's real UGC ad ('REAL AD'), on the right an AI-generated remake ('OUR AI AD') with a different AI creator copying the same moves — holding the yellow skincare jar, applying it, reacting — beat for beat for about 40 seconds. The point: a winning ad can be cloned with AI to test new faces.
- Example: [@LachezarVoynov](https://x.com/LachezarVoynov/status/1986113376230015058) · I still feel the best way to find winning ad creative concepts is scrolling on TikTok or IG Reels. Our team just turned a viral organic concept into a
- Example: [@raph_guilhem](https://x.com/raph_guilhem/status/2095453949805392267) · Seedance 2.5 is insane for AI UGC. I built a Claude skill that takes an ad that's already converting and puts a new person in it. This is perfect for 
- Example: [@SimScaler](https://x.com/SimScaler/status/2034333069167984905) · You should be PRINTING with AI UGC right now You can reverse engineer any winning ad And recreate it in minutes with your own AI creator That's the ne
- Example: [@angeldot_](https://x.com/angeldot_/status/2107913083783987306) · Cal AI scaled to 15M downloads before being acquired by MyFitnessPal now its co-founder just open-sourced the AI UGC workflow he wishes he had while b
- Example: [@ai_cult1](https://x.com/ai_cult1/status/2092368368968049118) · Cal AI growth was paid, not organic: creator roster, affiliate program, MrBeast sponsorship, in-house daily ad creative ($40M in 12 months).
- Example: [@N01ennn](https://x.com/N01ennn/status/2107887039513268301) · the person who ran UGC for Cal AI on its way to a $50M run rate just laid out how to run an AI UGC army for any app. this is pure f*cking treasure. so
- Example: [@slash1sol](https://x.com/slash1sol/status/2107878663488188775) · THE CO-FOUNDER WHO RAN GROWTH AT CAL AI JUST LEAKED THE ENTIRE AI UGC PIPELINE. ONE PERSON, ZERO CREATORS, THOUSANDS OF TEST VIDEOS Cal AI went to 15M
- Example: [@brainextends](https://x.com/brainextends/status/2094873288040497282) · i made $36,863 this month using ai agents heres the 3 step process i use : -> i created an ai agent that scans 24/7 for new trends on tiktok once it s

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| Find | Pull outlier organic posts in the niche (10x the account's median views) | Sheet: link, hook, structure, views |
| AI test | Remake 5 outliers with AI UGC (labelled) and post organically | Same hook and beats as the outlier |
| Pick | Keep the 1-2 that beat the account median | - |
| Real remake | Brief real creators to film the winners | Exact beat sheet from the AI version |
| Paid | Run the real versions as paid; retire after fatigue | - |

### Prompts

**Outlier search**

```
TikTok Creative Center / Foreplay: filter by niche, last 30 days, sort by views; keep posts at 10x the account median.
```

**AI remake (Arcads / Seedance)**

```
Split-screen check: put the original and the AI remake side by side and match every beat before posting.
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
- [ ] Files named `F53-<concept>-<variant>`; tracking tag `utm_content=F53-<concept>-<variant>`.
- [ ] Avoid: Label AI UGC.
- [ ] Avoid: Remake the structure, never copy someone's footage or exact script.
- [ ] Avoid: Kill AI tests fast; they are only for picking.

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

See [examples/README.md](examples/README.md) (27 posts). Top 5:

- @jakecastilloooo (984L/3090BM/290kV): Ex-Cal AI UGC lead's full AI UGC workflow (article): customer context → outlier videos vs creator baseline → reverse-engineer → believable first frame → test ta — https://x.com/jakecastilloooo/status/2107873317369581751
- @traqscales (22L/27BM/1kV): Once app: 22.5M views from 2 AI UGC creators (one 13M, 9 >100K) — AI bride crying at her reception, "we gave every guest a camera instead of hiring more photogr — https://x.com/traqscales/status/2108113354178932920
- @0xDepressionn (18L/14BM/2kV): Summary of Jake Castillo's workflow: AI videos as cheap organic tests, then ad money behind winners. — https://x.com/0xDepressionn/status/2107918489587507606
- @carlynorthmedia (0L/0BM/69V): Know when to stop iterating a winner: reusing the same hook causes audience + algorithm fatigue. — https://x.com/carlynorthmedia/status/2107565970197782530
- @ai_cult1 (0L/0BM/49V): Cal AI growth was paid, not organic: creator roster, affiliate program, MrBeast sponsorship, in-house daily ad creative ($40M in 12 months). — https://x.com/ai_cult1/status/2092368368968049118
