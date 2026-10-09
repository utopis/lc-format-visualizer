# BOT.md · generate a "GRWM / 'stack with me'"

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
5. Name every asset `F47-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F47
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

Creator gets ready (outfit → makeup → jewelry) or builds a stack piece by piece while talking; the jewelry is the payoff of the routine.

### Why it works

- GRWM is a default watch habit; jewelry as the "finishing touch" is natural.
- "Stack with me" demonstrates the bundle offer visually.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0-2s | Mirror, bare neck | "GRWM for a wedding — jewelry edition" |
| 2-15s | Layering 1→7 pieces | Chatty VO |
| 15-20s | Full look | "any 7 for $85" |

### Hooks

- "Building a 7-piece stack with me"
- "GRWM: jewelry I never take off"
- "Stack check"

### Production recipe

1. Creator briefs for swarm (F43).
2. Shoot mirror + close-ups.

### Existing bot prompt

```
Write 6 GRWM/stack-with-me scripts (25s) for occasions {{OCCASIONS}}; each builds a 7-piece stack from {{SKUS}}.
```

### Variants to test

- Occasion
- Creator age 25-35 vs 40-55

## Reference examples

See [examples/README.md](examples/README.md) (8 posts). Top 5:

- @Ecombos_Ai (28L/26BM/2kV): 10 AI UGC styles: talking-head testimonial, product-in-hand, first-try reaction, fake podcast, street interview, comment reply, unboxing, DITL/GRWM, before/afte — https://x.com/Ecombos_Ai/status/2103180929057407425
- @rirahcreates (12L/17BM/1kV): 20 UGC types: talking head, review, unboxing, testimonial, demo, problem/solution, before/after, GRWM, DITL, voiceover, routine, how-to, FAQ, 3 reasons why, POV — https://x.com/rirahcreates/status/2089827933561016787
- @ugcAshleyRJ (13L/5BM/534V): The 0.5x ultra-wide POV filming technique for demos, GRWM and day-in-the-life — immersive, native. — https://x.com/ugcAshleyRJ/status/2067636022251290725
- @0xJeyx (15L/3BM/889V): Generate the same product as every format at once (street quiz, review, GRWM, DITL) and let the feed pick — example: "$50 street quiz" video. — https://x.com/0xJeyx/status/2063387846803673406
- @wayne_forge (2L/1BM/118V): TWO AI TWINS "GET READY" IN THE SAME CLOSET — AND THE PAGE BEHIND THEM CLEARS $11,400 A MONTH. Same face, same hair, same dressing room. One in a pink textured  — https://x.com/wayne_forge/status/2087161700298473607
