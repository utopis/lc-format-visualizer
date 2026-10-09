# BOT.md · generate a "'The Cheat Code' / life-hack static (the product as the shortcut)"

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
5. Name every asset `F73-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F73
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

A static that frames the product as a hack or cheat code for a known annoyance: gifting, packing, getting ready fast. The language is "cheat code", "hack" or "the one thing that actually gets used", backed by short review quotes.

### Why it works

- "Cheat code" promises effort saved; people love shortcuts.
- Gift framing ("actually gets used") answers the gift-giver's fear.
- Review snippets supply the proof inside the copy.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| Static | Gift box open, 7 pieces fanned; headline "The gift cheat code" | Body: 3 short real review quotes + "any 7 for $85" |

### Hooks

- "The gift that actually gets worn"
- "Cheat code for getting ready in 30 seconds"
- "Travel hack: one stack, zero jewelry pouch"

### Production recipe

1. Pick 3 jobs: gifting, getting ready, travel.
2. Pull 3 short real review quotes for each.
3. Design as a plain static or a Notes screenshot.

### Existing bot prompt

```
Write 6 "cheat code" statics for LC (headline ≤7 words, 3 real review snippets from {{REVIEWS}}, offer line).
```

### Variants to test

- Gift vs routine vs travel
- With vs without quotes

## Reference examples

See [examples/README.md](examples/README.md) (13 posts). Top 5:

- @FedotOff90 (110L/208BM/9kV): 37 formats printing (with days active): AI podcast 280d, report card, iPhone Notes, text on skin, Reddit, cross-out, fake PDP, tier list, myth vs fact, zero sta — https://x.com/FedotOff90/status/2104949773539442831
- @mkwizrd (136L/186BM/66kV): AquaVoice is a fucking cheat code. Watched the Evolve podcast with @elfilosofooooo today, and bro shared so much sauce. Spoke the shit out of the Claude code to — https://x.com/mkwizrd/status/2089013712959189120
- @SEOKeval (132L/188BM/13kV): Investing in Google Ads is the ultimate SEO cheat code. It literally gives you data on what keywords convert into sales. All you have to do is rank for them, an — https://x.com/SEOKeval/status/2080403580260110750
- @doublenickk (86L/75BM/6kV): This is a f**king cheat code Someone just published a skill pack with the skills used at Anthropic, Google, OpenAI and others ComposioHQ/awesome-claude-skills.  — https://x.com/doublenickk/status/2093709535231840277
- @PerezHatesAI (48L/68BM/2kV): This is wild 😭 4.3M views. 250K saves. On a "weird habits" slideshow. No product demo. No feature dump. Just aesthetic slides of habits that "actually work". An — https://x.com/PerezHatesAI/status/2106779894785188006
