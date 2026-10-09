# BOT.md · generate a "Urgency/offer statics: low stock, back in stock, limited-time offer, BFCM"

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
5. Name every asset `F37-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F37
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

Bottom-of-funnel statics built around a real time/stock constraint: "back in stock", "only N left", "ends Sunday", "BFCM: any 7 for $85 + free gift". Clean product + offer + deadline. For retargeting and seasonal pushes.

### Why it works

- Converts warm audiences who already know the product.
- LTO S-tier in a 2026 operator tier list.
- Mirrors Omnisend/OneText calendar → consistent offer across channels.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| Static A | "Back in stock" stamp on Chelsea Herringbone | — |
| Static B | "Any 7 for $85 — ends Sunday" over stack flat-lay | — |
| Static C | Low-stock bar "87% claimed" | Only with real data |

### Hooks

- "It's back (for now)"
- "Any 7 for $85 ends Sunday"
- "BFCM early access: build your stack"
- "Last restock before the holidays"

### Production recipe

1. Pull real stock/deadline from Shopify; schedule start/stop.
2. Templates for back-in-stock, ends-X, BFCM, gift-deadline (shipping cutoff).
3. Retarget 30-day engagers + site visitors; exclude purchasers 7d.
4. Mirror in email (Omnisend) + SMS (OneText) with same UTM concept.

### Existing bot prompt

```
Given the live offer {{OFFER}}, deadline {{DATE}} and stock data {{STOCK}}, write 8 urgency static headlines (≤8 words) and 8 subheads; only use scarcity that the data supports. Add matching Omnisend subject line and OneText SMS (≤140 chars).
```

### Variants to test

- Deadline vs stock framing
- Product vs stack image

## Reference examples

See [examples/README.md](examples/README.md) (16 posts). Top 5:

- @ads4apps (412L/930BM/27kV): 39 Meta formats that convert (930 bookmarks): X reasons, IG story, us vs them, Venn, don't buy this, iPhone notes, text message, low stock, we're sorry, breakin — https://x.com/ads4apps/status/2081785032679518490
- @williamkast_ (252L/400BM/13kV): Formats by funnel: TOF founder/yapper/AI animation/natives/3 reasons/voiceless overlay; MOF comment reply/testimonial mashup/text wall; BOF urgency statics. — https://x.com/williamkast_/status/2103910235005935644
- @nicktheriot_ (219L/348BM/12kV): 2026 FB creative styles tier list: S = long primary text + organic image, LTO, UGC, VSL, reaction, news; A = demo, us vs them, testimonial, close-up, founder st — https://x.com/nicktheriot_/status/2108173638033871013
- @raph_guilhem (9L/6BM/377V): 35 static/native formats tree: Trustpilot, text msg, email screenshot, Reddit, text on skin, crossed-out, tier list, Venn, breaking news. — https://x.com/raph_guilhem/status/2090725512976970065
- @EmerieOnoh (6L/6BM/498V): Static formats printing: us vs them, whiteboard, breaking news, doodle, low stock, iPhone notes, Google search, we're sorry, Reddit, tweet screenshot, text on p — https://x.com/EmerieOnoh/status/2098426706612683154
