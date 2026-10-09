# BOT.md · generate a "'Ugly ad': an unusual or weird visual + long copy (native image)"

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
5. Name every asset `F84-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F84
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

A deliberately odd, low-polish photo (product in a weird place, strange crop, unexpected object) paired with long, story-driven primary text. Steal the visual idea and keep your own copy.

### Why it works

- Weirdness beats beauty for stopping the scroll.
- A low-polish look reads as organic.
- Long copy does the selling once the visual earns the pause.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| Static | Necklace frozen inside an ice cube / in a glass of seawater / on a lemon | Primary: 300-word first-person story |

### Hooks

- "I left my necklace in a glass of seawater for 30 days"
- "Why is there a necklace in my ice tray?"

### Production recipe

1. Brainstorm 10 weird but true scenes (real tests: ice, saltwater, lemon juice).
2. Shoot on phone, flash on.
3. Pair with F09 long-copy natives.

### Existing bot prompt

```
List 10 weird-but-true visual scenes for LC that also prove durability, then write a 250-word native primary text for the top 3.
```

### Variants to test

- Weird level
- Proof vs pure oddity

## Reference examples

See [examples/README.md](examples/README.md) (8 posts). Top 5:

- @FedotOff90 (68L/98BM/6kV): 777 native images + long-form copy swipe board. — https://x.com/FedotOff90/status/2104253649346068682
- @FedotOff90 (41L/53BM/5kV): "The ugly ads print" — weird visuals stop the scroll, long copy sells; 122-ad Native Unusual Visuals board. — https://x.com/FedotOff90/status/2107184145541853536
- @alexgoughcooper (61L/60BM/9kV): This video did 32M views and is a masterclass in ugly ads. Why? Because it’s authentic. You keep trying to make ‘UGC’ or ‘ugly ads’ that are fully scripted. But — https://x.com/alexgoughcooper/status/2092657905002529270
- @Simon__Rob (51L/79BM/5kV): this is how your Meta ad account should be built if you're a brand: - ugly static ads and yapping videos stop cold traffic - testimonials and stats convince war — https://x.com/Simon__Rob/status/2089448804676239424
- @dileshumale (10L/3BM/775V): Animate those ugly static ads. Thank me later. — https://x.com/dileshumale/status/2105897021328757090
