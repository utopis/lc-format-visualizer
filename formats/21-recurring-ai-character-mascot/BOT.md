# BOT.md · generate a "Recurring (AI or illustrated) character / mascot page"

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
5. Name every asset `F21-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F21
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

One distinctive character (odd, recognisable — accent, look, catchphrase) in short repeatable bits; motion borrowed from trending formats; same character every post builds a following ([@sairahul1](https://x.com/sairahul1/status/2107172215586513360)).

## Reference examples

See [examples/README.md](examples/README.md) (8 posts). Top 5:

- @ErnestoSOFTWARE (941L/1533BM/95kV): 11.5M views one faceless account; pitches Arcads automating carousels; 3-4 accounts. — https://x.com/ErnestoSOFTWARE/status/2103534688048414959
- @sairahul1 (237L/329BM/23kV): GaryVee: make AI influencers; 'jean phil' 100M views in 1 week (recognizable odd character). — https://x.com/sairahul1/status/2107172215586513360
- @rewind02 (108L/56BM/4kV): AI influencer: treat character as a service, sell ads to brands. — https://x.com/rewind02/status/2107211233405325547
- @MuteeAutomation (43L/39BM/3kV): This channel found a crazy content loophole: Take a familiar news format → add satire → create a recurring character → keep the format consistent. The result? M — https://x.com/MuteeAutomation/status/2107022363313279044
- @BTCTanAces1 (18L/0BM/343V): Research on brand characters consistently shows measurable effects: higher recall, stronger emotional response, better long-term brand equity, and improved mark — https://x.com/BTCTanAces1/status/2082833207402057894
