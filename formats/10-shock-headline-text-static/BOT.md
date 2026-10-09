# BOT.md · generate a "Shock-headline typographic static (story headline + product block)"

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
5. Name every asset `F10-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F10
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

White background, huge condensed black headline that is a story line, 3 short lines of body continuing the story with a twist, product pack-shot bottom right, brand + 2-line benefit + "SHOP NOW →". Example: "MY SISTER SLEPT WITH MY HUSBAND. / Eight months later, she's the one everyone calls beautiful at family dinners. / Because she drains parasites. / And I didn't even know I had them." ([@tryatria_AI](https://x.com/tryatria_AI/status/2105745816828940336)).

### Why it works

Typography-only reads in 1s, novelty of a tabloid line in a polished feed; cheap to produce → huge variant volume.

### Hooks

Family betrayal line, confession, overheard insult, "Nobody at the reunion recognised me".

### Production recipe

Figma/Canva template; Claude writes 50 headlines in LC voice; designer approves 10; resize 1:1/4:5/9:16.

## Reference examples

See [examples/README.md](examples/README.md) (2 posts). Top 5:

- @tryatria_AI (73L/98BM/4kV): Static hook 'My sister slept with my husband' vs generic benefit lines. — https://x.com/tryatria_AI/status/2105745816828940336
- @adamtaylorl (17L/9BM/3kV): Fully agree. Most brands have a winning ad they haven't made yet and the footage is already sitting on a hard drive. But there's a reason this works that most p — https://x.com/adamtaylorl/status/2103439375787003983
