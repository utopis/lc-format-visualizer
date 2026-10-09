# BOT.md · generate a "Street / resort interview & "overheard question" ("what are you wearing?")"

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
5. Name every asset `F07-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F07
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

**Variant 1 — Interview**: handheld mic, stranger on the street/resort: "Are you really 56?" → "I lost 18 pounds in one month… it was cortisol" ([@tryatria_AI](https://x.com/tryatria_AI/status/2095860430099058905)). Question does the hooking; answer is social proof.
**Variant 2 — Overheard question (stronger)**: the product is discovered by a third party asking. GroundingWell: hotel guests calling the front desk asking what mattress they use — "Quick question, what kind of mattress you guys use?… I think you just saved me three grand… half the calls I get now are about the sheets" (transcript; [@adamtaylorl](https://x.com/adamtaylorl/status/2094742062755422423)). They don't even sell mattresses.

Shot list (20-30s, V2): 0-2s stranger approaches / phone rings "Sorry—where is your necklace from?" · 2-10s owner answers casually, fiddles with it · 10-20s reveal detail ("I swim in it") + close-up · 20-25s asker: "okay I'm ordering one" · end card.

### Why it works

Curiosity + third-party validation; viewer becomes the person asking. Resolves "is it real gold?" doubt via an honest answer on camera.

### Production recipe

Real: hire 2 creators, film in a café/beach, scripted-but-natural (disclose as ad). AI: Seedance/Veo two-character scene — only for dramatized skits, not presented as real people.

## Reference examples

See [examples/README.md](examples/README.md) (16 posts). Top 5:

- @adamtaylorl (362L/466BM/26kV): GroundingWell 550+ ads: hotel guests asking what mattress they use (overheard-question angle). — https://x.com/adamtaylorl/status/2094742062755422423
- @adamtaylorl (139L/203BM/13kV): Tier list of ecom formats: F = AI UGC, street interviews, read scripts; B = founder, testimonial compilations, listicle statics... — https://x.com/adamtaylorl/status/2097641383355879452
- @lorenzo_pravata (150L/196BM/10kV): "Ads that don't look like ads": podcast clips, street interviews, skits with studio actors; pet brand $29K→$150K/mo spend in 60 days, CPA $188→$124. — https://x.com/lorenzo_pravata/status/2104536224488738839
- @ZedNilm1 (116L/185BM/17kV): Resilia AI street interviews with 90+ year olds - believable, near-zero ad feel. — https://x.com/ZedNilm1/status/2101280447154036917
- @tryatria_AI (83L/150BM/9kV): AI resort 'random interview' ('Are you really 56?') hook format. — https://x.com/tryatria_AI/status/2095860430099058905
