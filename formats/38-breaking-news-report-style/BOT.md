# BOT.md · generate a "Breaking-news / news-report style ad"

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
5. Name every asset `F38-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F38
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

The ad borrows news grammar: "BREAKING" lower-third, anchor-style delivery or a news-article screenshot announcing something genuinely new (launch, milestone, restock, real press). Video = creator as reporter on green screen; static = headline card.

### Why it works

- News framing triggers "what happened?" curiosity.
- S-tier in a 2026 operator tier list.
- Natural fit for launches and milestones.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0-2s | Red "BREAKING" bar, creator as anchor | "Breaking: a jewelry brand just passed 300,000 customers and…" |
| 2-12s | B-roll of pieces in water | "…the reason is you can shower in it." |
| 12-20s | Offer card | "Any 7 for $85. Back to you." |

### Hooks

- "BREAKING: the necklace that survived 6 months of ocean"
- "News: 300,000 women stopped taking their jewelry off"
- "This just in: the herringbone is back"

### Production recipe

1. Only announce real news (launch, milestone, restock, real press).
2. News lower-third template; no real network logos.
3. Creator on green screen or AI presenter (labelled).

### Existing bot prompt

```
Write 5 news-style LC ad scripts (20s) around these real events {{EVENTS}}: anchor line, 2 supporting facts, CTA. Plus 5 headline statics. Do not mimic real news outlets.
```

### Variants to test

- Anchor video vs headline static
- Serious vs playful

## Reference examples

See [examples/README.md](examples/README.md) (11 posts). Top 5:

- @ads4apps (412L/930BM/27kV): 39 Meta formats that convert (930 bookmarks): X reasons, IG story, us vs them, Venn, don't buy this, iPhone notes, text message, low stock, we're sorry, breakin — https://x.com/ads4apps/status/2081785032679518490
- @nicktheriot_ (219L/348BM/12kV): 2026 FB creative styles tier list: S = long primary text + organic image, LTO, UGC, VSL, reaction, news; A = demo, us vs them, testimonial, close-up, founder st — https://x.com/nicktheriot_/status/2108173638033871013
- @raph_guilhem (9L/6BM/377V): 35 static/native formats tree: Trustpilot, text msg, email screenshot, Reddit, text on skin, crossed-out, tier list, Venn, breaking news. — https://x.com/raph_guilhem/status/2090725512976970065
- @EmerieOnoh (6L/6BM/498V): Static formats printing: us vs them, whiteboard, breaking news, doodle, low stock, iPhone notes, Google search, we're sorry, Reddit, tweet screenshot, text on p — https://x.com/EmerieOnoh/status/2098426706612683154
- @Yannlce (3L/2BM/1kV): Same 40-format list (adds claymation, AI podcast). — https://x.com/Yannlce/status/2085017654364958737
