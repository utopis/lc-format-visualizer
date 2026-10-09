# BOT.md · generate a "Lo-fi promo statics (handwritten sign + 24 BFCM variants)"

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
5. Name every asset `F17-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F17
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

## Reference examples

See [examples/README.md](examples/README.md) (12 posts). Top 5:

- @adamtaylorl (57L/112BM/6kV): 25 BFCM static ads incl. The Handwritten Sign. — https://x.com/adamtaylorl/status/2106021392567198020
- @thekaipullai (373L/4BM/24kV): What's the point of all these record profits when it was the worst broadcasted sporting event anyone has ever seen. Never in my life I have seen a sporting chan — https://x.com/thekaipullai/status/2106771287096119428
- @Tonystakkz (132L/106BM/13kV): This is why Shaun for me is top 5 copywriter in 2026. He understands how copywriting in the modern world works. Abraham Lincoln said something very similar: "Gi — https://x.com/Tonystakkz/status/2099548690360721815
- @binghott (133L/57BM/20kV): We might be cooked Go to your best image ad in Ads Manager and check Meta's AI generated image options. I found a handwritten Post-It note ad in it. And it wasn — https://x.com/binghott/status/2077730930785980720
- @tryatria_AI (72L/93BM/3kV): HANDWRITTEN ADS SHOULDN’T WORK THIS WELL. BUT THEY DO. 👀 Handwritten notes. Whiteboards. Crude drawings. Marker scribbles. They look almost too simple compared  — https://x.com/tryatria_AI/status/2098414761578811635
