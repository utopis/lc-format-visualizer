# BOT.md · generate a "Unboxing / packing orders (ASMR)"

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
5. Name every asset `F46-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F46
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

"Pack an order with me" (founder/team ASMR) or customer unboxing of the LC box — tactile, satisfying, shows packaging and gift readiness.

### Why it works

- ASMR + packaging = gift signal.
- Cheap volume content; a "new style" lever for stuck accounts.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0-2s | Top-down box | "Packing a 7-piece stack for Dana in Ohio" |
| 2-20s | Each piece placed | ASMR |
| 20-25s | Box closed + note | "any 7 for $85" |

### Hooks

- "Pack a 7-piece order with me"
- "Unboxing the gift I asked for"

### Production recipe

1. Top-down tripod; good mic; no customer PII on labels.

### Existing bot prompt

```
Write 10 pack-with-me captions and hooks using real order types {{ORDERS}} (no customer full names).
```

### Variants to test

- Founder vs customer

## Reference examples

See [examples/README.md](examples/README.md) (7 posts). Top 5:

- @nicktheriot_ (219L/348BM/12kV): 2026 FB creative styles tier list: S = long primary text + organic image, LTO, UGC, VSL, reaction, news; A = demo, us vs them, testimonial, close-up, founder st — https://x.com/nicktheriot_/status/2108173638033871013
- @nicktheriot_ (45L/55BM/4kV): Stuck-account order: new avatar → new style (AI UGC, animation, unboxing, reaction, native) → curiosity text hook → uncommon location → combos. — https://x.com/nicktheriot_/status/2096219973139992840
- @Ecombos_Ai (28L/26BM/2kV): 10 AI UGC styles: talking-head testimonial, product-in-hand, first-try reaction, fake podcast, street interview, comment reply, unboxing, DITL/GRWM, before/afte — https://x.com/Ecombos_Ai/status/2103180929057407425
- @rirahcreates (12L/17BM/1kV): 20 UGC types: talking head, review, unboxing, testimonial, demo, problem/solution, before/after, GRWM, DITL, voiceover, routine, how-to, FAQ, 3 reasons why, POV — https://x.com/rirahcreates/status/2089827933561016787
- @raph_guilhem (55L/105BM/7kV): 30 Meta ad formats folder tree (hooks, founder content, etc.). — https://x.com/raph_guilhem/status/2083288607062732816
