# BOT.md · generate a "Interactive gesture add-on ads (TikTok tap-to-reveal, shake-to-reveal, Super Like)"

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
5. Name every asset `F66-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F66
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

TikTok interactive add-ons layered on an existing video ad: a Display Card that reveals an offer on tap, a shake-to-reveal surprise, or branded Super Like icons on double-tap.

### Why it works

- Turns a gesture viewers already make into the ad interaction.
- Good for offers/drops.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0-5s | Gift box unboxing video | — |
| 5s | Display Card: "Tap to reveal today's stack" | — |
| Reveal | Card with any 7 for $85 | — |

### Hooks

- "Tap to open the box"
- "Shake to reveal your stack"

### Production recipe

1. Add Display Card to winning TikTok video ads; test vs no card.

### Existing bot prompt

```
Write 5 Display Card / gesture concepts for LC TikTok ads with on-card copy ≤8 words.
```

### Variants to test

- Card vs no card

## Reference examples

See [examples/README.md](examples/README.md) (1 posts). Top 5:

- @_deepakss_ (10L/0BM/201V): Building "Tiktok for games" Arcadeo for this year's Shipaton. My main aim is to have a non frustrating experience when viewing an ad. This means user can skip t — https://x.com/_deepakss_/status/2087895969157246985
