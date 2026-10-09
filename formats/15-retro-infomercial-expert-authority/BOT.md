# BOT.md · generate a "Retro TV infomercial / expert authority (1987 daytime-TV look, "professor interview")"

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
5. Name every asset `F15-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F15
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

VHS grain, 4:3 framing, serious host in a pink blazer, studio set, big claims overlay ("550,000+ women"), phone number style lower-third. "It doesn't look like a polished DTC ad" ([@tryatria_AI](https://x.com/tryatria_AI/status/2105329322496016777)).

## Reference examples

See [examples/README.md](examples/README.md) (5 posts). Top 5:

- @tryatria_AI (118L/211BM/8kV): Retro 1987-TV dermatologist ad: un-polished authority format stands out. — https://x.com/tryatria_AI/status/2105329322496016777
- @CEO_Vlad (78L/117BM/7kV): AI pharmacist ad format: $5, 4 minutes (authority-figure risk). — https://x.com/CEO_Vlad/status/2088597593949692087
- @antonioventre_ (47L/49BM/3kV): Supplement 3.17x ROAS: 1 CBO/product, 1 ad set/persona; creatives = Suno AI ads, professor interview... — https://x.com/antonioventre_/status/2108228200421576872
- @HenryCrochemore (5L/1BM/394V): this static is weird enough to make you stop poo-pourri took a product nobody wants to think about and wrapped it in a polished retro ad the contrast is what ma — https://x.com/HenryCrochemore/status/2092191032645431595
- @TomReichertWA (3L/0BM/90V): @CocaCola Quick jump to tick tock to dub in music to my Grok made clip now I made you a retro ad in a minute 😎 @nikitabier @X @elonmusk Hot weather grate soft d — https://x.com/TomReichertWA/status/2085467482224247014
