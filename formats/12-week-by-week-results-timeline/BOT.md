# BOT.md · generate a "What happens if you…" week-by-week timeline (30-second funnel)"

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
5. Name every asset `F12-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F12
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

### Production recipe

Real creator 30-day diary (best) or AI animated (F05). Metric hold to 75%, CPA, Omni.

## Reference examples

See [examples/README.md](examples/README.md) (7 posts). Top 5:

- @tryatria_AI (221L/410BM/18kV): 30-second funnel: provocative hook then week-1..week-4 storyline of results. — https://x.com/tryatria_AI/status/2106069700950294836
- @MaximilianMoj (0L/0BM/0V): Resilia "$36M/month" (unverified) top 5 ads via Playhead teardowns: candida, aged garlic 4-week arteries, GLP-1, urgency (8 at once), animated explainer. — https://x.com/MaximilianMoj/status/2101002307160731848
- @Salifsibane16 (0L/0BM/0V): 3 AI song-ad story frameworks: bumping into ex (start at end), week-by-week timeline, cheating → self-improvement. — https://x.com/Salifsibane16/status/2099891350015512903
- @skytookie (249L/69BM/16kV): hey chat! as you may have seen, I've played in a few creator tournaments recently, and one thing I noticed is... there's ALWAYS a radiant or immortal popping of — https://x.com/skytookie/status/2100679695973134683
- @ZedNilm1 (43L/62BM/4kV): female beauty scare ads convert stupidly fast because they don’t educate they show the future your customer is afraid of not “get glowing skin” more like “this  — https://x.com/ZedNilm1/status/2076276174754316716
