# BOT.md · generate a "Styling carousel — 'how to wear it / how it stacks' (jewelry-native carousel)"

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
5. Name every asset `F57-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F57
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

A 5-8 card carousel that answers "how will I actually wear this?": one piece styled 5 ways, or how several pieces build one look. Each card evolves the story (hook → looks → proof → CTA) instead of repeating one message.

### Why it works

- Answers the #1 jewelry pre-purchase question (wearability).
- Each swipe is a re-engagement opportunity; carousel copy should build like a short story.
- Shows the bundle (any 7) as outfits, raising AOV.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| Card 1 | Hook: "1 necklace, 5 ways" over Chelsea Herringbone on skin | — |
| Card 2 | Alone, white tee | "the everyday" |
| Card 3 | Layered with a fine chain | "the layer" |
| Card 4 | With a blazer | "the office" |
| Card 5 | Wet, at the beach | "the beach (yes, waterproof)" |
| Card 6 | Full 7-piece stack | "or build all 7 for $85 →" |

### Hooks

- "1 necklace, 5 ways"
- "How to stack 7 pieces without looking like a jewelry store"
- "Wedding guest → beach → office: same stack"
- "The 3-piece rule for layering necklaces"

### Production recipe

1. Shoot one model/creator in 5 outfits (or use real customer photos with permission).
2. 4:5, ≤10 words per card, consistent type; card 1 = hook, last card = offer.
3. Variants: "1 piece 5 ways", "7-piece stack build", "occasion stack" (wedding/office/beach), FAQ carousel (sizes, waterproof, care).

### Existing bot prompt

```
Write 5 styling-carousel scripts (6 cards each, ≤10 words per card) for LC pieces {{SKUS}}: card 1 hook, cards 2-5 looks/occasions, card 6 offer (any 7 for $85). Also suggest the photo for each card.
```

### Variants to test

- Single piece vs stack
- Model vs real customers
- Occasion vs styling-rule framing

## Reference examples

See [examples/README.md](examples/README.md) (2 posts). Top 5:

- @ChristyGodswil (73L/31BM/12kV): Fashion brands don’t just need beautiful clothes. They need content that helps people imagine themselves wearing them. Instead of posting another product photo, — https://x.com/ChristyGodswil/status/2080225401406672901
- @happy_place247 (51L/28BM/1kV): As a fashion vendor, you could simply put your outfits on a mannequin, or you could show potential customers what those same pieces actually look like on a pers — https://x.com/happy_place247/status/2087866038750736389
