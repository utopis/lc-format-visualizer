# BOT.md · generate a "Diagram statics: Venn, report card, comparison chart, us-vs-them grid"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 1 static 1080x1350 per diagram), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@Hashir_Shaikh_](https://x.com/Hashir_Shaikh_/status/2096337779412304217) · Four diagram-style statics: a this-vs-that comparison with the product against a rival, a red X versus a green check table, and a "NO WONDER EVERY STEP HURTS" anatomy visual. Each one makes the argument with a simple chart instead of a lifestyle photo.
- Example: [@EiyanDickerson](https://x.com/EiyanDickerson/status/2088266872194023737) · 4 Static Ads. 1 Angle. 1. Before & After 2. Feature Callout 3. Headline Callout 4. Us vs Them A Moisturizer built for the heat☀️
- Example: [@adamtaylorl](https://x.com/adamtaylorl/status/2002000462955090352) · The "Us vs. Them" static is the easiest high-performing ad you can make today. Here is the layout: Left side: "Other Brands" ➡️Image: Generic/competit
- Example: [@adamtaylorl](https://x.com/adamtaylorl/status/2006349117052891625) · The "Us vs. Them" framework is still the highest-performing static ad format. But most brands do it wrong. Don't just list features. Contrast emotions
- Example: [@iwo_cybulski](https://x.com/iwo_cybulski/status/2014511962734940211) · Static ad for Nutravantix 🐄 Us vs them, vitamins vs real supplement. Want high-converting ads like this? DM me "ads" 🔥
- Example: [@gginwanderland](https://x.com/gginwanderland/status/2107842978173862243) · Winner static breakdown pt.2: the us vs them layout save this post ;)
- Example: [@aaazavyalov](https://x.com/aaazavyalov/status/2020886502788501660) · This is a new static ad concept I’m seeing only a few DTC brands test so far… Us vs Us. - Same product. - Two angles. - Side-by-side. It works because
- Example: [@ultimategrafiks](https://x.com/ultimategrafiks/status/2090399839309738284) · I love designing static ads because every product comes with a different story and creative challenge. CALLOUT, US vs THEM, DTC &amp; UGC, I love crea

### Live paid ads in this format (5 in [adlibrary/](adlibrary/README.md), longest-running first)

- **Frøya Organics: "What will be gone by 2025" checklist static (Frøya Organics)** (609 days live): A black static: "What will be gone by 2025" with yellow check-boxes: Dark circles GONE, Crows feet GONE, Wrinkles GONE, Age spots GONE, Dull skin GONE, Turkey neck GONE; 4 jars on the strip below.
- **Raising Toddlers with Bec: Vintage anatomy diagram static ("2 years in diapers vs 4 years")** (278 days live): A vintage medical-illustration-style diagram comparing two toddlers' brain-bladder connection ("active connection" versus "signal suppression"). Raising Toddlers with Bec.
- **FurryWell Philippines: Report-card rating static (FurryWell "A+ / 9.7")** (188 days live): An "Overall Guide A+ / Total Rating 9.7/10" card with bars (Ingredient quality 9.7, Flavour 10, Scent 10, Value 9) and a SHOP NOW button.
- **Smooche · Cosmetic Times: “REVERSE MENOPAUSE SKIN CHANGES: TRY KOREAN PEPTIDES”** (19 days live): "REVERSE MENOPAUSE SKIN CHANGES: TRY KOREAN PEPTIDES", an ingredient-callout diagram around the bottle.
- **Smooche · Cosmetic Times: “Botox in a bottle”** (17 days live): "Botox in a bottle" with 4 benefit callouts (blurs, flattens, fades, plumps).

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| Venn | Two circles: "Looks like real gold" and "You can shower in it"; product in the overlap | - |
| Report card | School report card layout grading cheap plated vs PVD | Water: F vs A · Sweat: D vs A · Price: B vs A |
| Comparison chart | Three columns: plated, solid gold, PVD; rows: price, waterproof, lasts | Ticks and crosses |
| Us vs them grid | Two-column table with photos at the top | "Them: $20, 3 weeks. Us: $12 a piece, years." |

### Prompts

**Figma**

```
Grid 1080x1350, 2-3 columns, 5 rows max, bold row labels, gold ticks; product photo at the top of the winning column.
```

**Claude**

```
Build a comparison table for [product] vs 2 alternatives using only facts from [paste sources]; mark anything unverified.
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
- [ ] Files named `F35-<concept>-<variant>`; tracking tag `utm_content=F35-<concept>-<variant>`.
- [ ] Avoid: Comparisons must be fair and provable; keep your sources.
- [ ] Avoid: Don't name competitors unless you can back every cell.
- [ ] Avoid: Five rows maximum or nobody reads it.

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
5. Name every asset `F35-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F35
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

Information-graphic statics: a Venn diagram where LC sits in the overlap, a school report card grading LC vs "typical gold-plated", a check/cross comparison chart, or an us-vs-them split. Quick logical proof at a glance.

### Why it works

- Visual logic is processed instantly; the overlap/grade is the punchline.
- Report card and Venn are novel UIs in feed (pattern break).
- Good for MOF shoppers comparing options.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| Venn | 3 circles: "looks like real gold" / "shower-proof" / "under $15 a piece" → center: LC stack photo | — |
| Report card | "Louise Carter — Report Card": Waterproof A+, Price A, Compliments A+, Taking it off F (never) | Primary text: teacher comment joke |
| Chart | LC vs plated vs solid 14K: price, waterproof, tarnish, gift box | — |

### Hooks

- "The jewelry Venn diagram nobody could solve"
- "Report card after 6 months of wearing it every day"
- "Plated vs solid vs PVD — honest chart"

### Production recipe

1. Figma templates: Venn, report card, 3-column chart, split us/them.
2. Comparison rows only with verifiable facts; competitor = generic category ("typical gold-plated").
3. AI image tools can render the template; check text accuracy.

### Existing bot prompt

```
Produce on-image copy for: 1 Venn (3 desirable traits, LC center), 1 report card (5 subjects, grades, a funny teacher comment), 1 comparison chart (LC vs gold-plated vs solid 14K; 5 rows from {{PDP_FACTS}} and public generic facts). Flag any row that needs substantiation.
```

### Variants to test

- Diagram type
- Funny vs factual tone

## Reference examples

See [examples/README.md](examples/README.md) (13 posts). Top 5:

- @ads4apps (412L/930BM/27kV): 39 Meta formats that convert (930 bookmarks): X reasons, IG story, us vs them, Venn, don't buy this, iPhone notes, text message, low stock, we're sorry, breakin — https://x.com/ads4apps/status/2081785032679518490
- @FedotOff90 (110L/208BM/9kV): 37 formats printing (with days active): AI podcast 280d, report card, iPhone Notes, text on skin, Reddit, cross-out, fake PDP, tier list, myth vs fact, zero sta — https://x.com/FedotOff90/status/2104949773539442831
- @raph_guilhem (9L/6BM/377V): 35 static/native formats tree: Trustpilot, text msg, email screenshot, Reddit, text on skin, crossed-out, tier list, Venn, breaking news. — https://x.com/raph_guilhem/status/2090725512976970065
- @_evancarroll (4L/2BM/239V): 15 AI static frameworks: 3 core benefits, bold claim, us vs them, comparison chart, old vs new, 5-star, stat, press screenshot, notes app, sticky notes, meme, l — https://x.com/_evancarroll/status/2084775630152114293
- @Yannlce (3L/2BM/1kV): Same 40-format list (adds claymation, AI podcast). — https://x.com/Yannlce/status/2085017654364958737
