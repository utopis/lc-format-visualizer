# BOT.md · generate a "Split-screen "two versions of the same person" day"

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
5. Name every asset `F22-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F22
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

Left: version A of a person's day; right: version B (with product), synced timelines, captions with times.

## Reference examples

See [examples/README.md](examples/README.md) (9 posts). Top 5:

- @CEO_Vlad (88L/169BM/5kV): AI UGC formats tiered: S = podcast, talking head, in-car... — https://x.com/CEO_Vlad/status/2096569603761827953
- @thankyouecom (78L/133BM/6kV): Almost every winner in our scaling CBO this month is AI debate Here’s our method for generating these bangers 1. Not an interview Debate formats are arguments a — https://x.com/thankyouecom/status/2093386984349700402
- @Charconsults (3L/0BM/172V): Day 7/14 This one is an oldie, brief show the product in use and the pay off for using. This ad was very visual use before after/split screen pacing and brolls. — https://x.com/Charconsults/status/2081629763882430905
- @DailyYTNiches (158L/96BM/7kV): This channel hasn't even had a single flop video 👀 ~ 1.86k subscribers ~ 547,079 total views ~ $875 in the 30 days alone (assuming a $2.59 RPM) Format > Split s — https://x.com/DailyYTNiches/status/2096979805346673029
- @YouTubeAut3538 (20L/5BM/633V): This channel hasn't even had a single flop video. ~ 1.86k subs ~ 547,079 total views ~ $875 in the 30 days alone (assume $2.59 RPM) Format &gt; Split screen thu — https://x.com/YouTubeAut3538/status/2097064734474256890
