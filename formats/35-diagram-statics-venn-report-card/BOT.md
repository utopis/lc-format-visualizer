# BOT.md · generate a "Diagram statics: Venn, report card, comparison chart, us-vs-them grid"

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
