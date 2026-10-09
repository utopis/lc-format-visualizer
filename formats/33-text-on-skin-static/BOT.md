# BOT.md · generate a "Text-on-skin / text-on-palm static"

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
5. Name every asset `F33-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F33
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

A close-up photo where the message is written (pen/eyeliner-style) directly on skin — palm, inner wrist, collarbone — next to the product. Lo-fi, intimate, impossible to read as a brand template.

### Why it works

- Pattern break: handwriting on skin stops the thumb.
- Intimate/personal — reads as a note-to-self or confession.
- For jewelry the skin shot doubles as a product-on-body shot.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| Static 1 | Inner wrist with bracelet stack; on palm: "6 months. never took it off." | Primary text: short story |
| Static 2 | Collarbone with herringbone; on shoulder: "yes I shower in it" | — |
| Static 3 | Hand with rings; on fingers (one word each): "OCEAN PROOF" | — |

### Hooks

- "never took it off"
- "yes, I shower in it"
- "$85 for 7"
- "note to self: stop buying jewelry that turns green"
- "his mom asked where it's from"

### Production recipe

1. Shoot real hands/wrists (diverse skin tones) with LC pieces in daylight; write with skin-safe eyeliner pencil.
2. Or composite handwriting in post (Procreate) — keep it believable.
3. Short message ≤6 words; long primary text tells the story.
4. 3 skin locations × 4 messages = 12 statics.

### Existing bot prompt

```
Write 20 text-on-skin messages (≤6 words, handwritten tone, lowercase) for LC waterproof 14K PVD jewelry, each paired with a body location (palm, inner wrist, collarbone, fingers) and the LC piece in frame. Then write 80-word first-person primary text for the best 5.
```

### Variants to test

- Real handwriting vs composited
- Skin location
- Message type (proof / price / identity)

## Reference examples

See [examples/README.md](examples/README.md) (6 posts). Top 5:

- @ads4apps (412L/930BM/27kV): 39 Meta formats that convert (930 bookmarks): X reasons, IG story, us vs them, Venn, don't buy this, iPhone notes, text message, low stock, we're sorry, breakin — https://x.com/ads4apps/status/2081785032679518490
- @FedotOff90 (110L/208BM/9kV): 37 formats printing (with days active): AI podcast 280d, report card, iPhone Notes, text on skin, Reddit, cross-out, fake PDP, tier list, myth vs fact, zero sta — https://x.com/FedotOff90/status/2104949773539442831
- @raph_guilhem (9L/6BM/377V): 35 static/native formats tree: Trustpilot, text msg, email screenshot, Reddit, text on skin, crossed-out, tier list, Venn, breaking news. — https://x.com/raph_guilhem/status/2090725512976970065
- @EmerieOnoh (6L/6BM/498V): Static formats printing: us vs them, whiteboard, breaking news, doodle, low stock, iPhone notes, Google search, we're sorry, Reddit, tweet screenshot, text on p — https://x.com/EmerieOnoh/status/2098426706612683154
- @Yannlce (3L/2BM/1kV): Same 40-format list (adds claymation, AI podcast). — https://x.com/Yannlce/status/2085017654364958737
