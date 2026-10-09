# BOT.md · generate a "TikTok Shop affiliate shoppable demo (real creators, sample seeding)"

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
5. Name every asset `F19-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F19
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

15-40s creator video with orange shopping cart: unboxing → put on → water test → "linked below / tap the cart". One hook per video pulled from real reviews (@maverickecom). Seed widely: 1,000 free samples/month (@NotZainAgain playbook); creators doing 4+ ads get their own ad set (@zachlduncan Trybe structure); use Trybe as a **performance** platform, not gifting (@httpsean_ca).

### Production recipe

TikTok Shop listing + open/targeted collaborations; commission 15-25%; sample requests auto-approve for creators with >X GMV; weekly creator brief with top 5 hooks; Spark-code the top 10 videos.

## Reference examples

See [examples/README.md](examples/README.md) (21 posts). Top 5:

- @maverickecom (567L/934BM/44kV): $34 product: TikTok Shop affiliates (trust) + AI affiliate pages on IG/FB to Amazon; one hook per video from reviews. — https://x.com/maverickecom/status/2106072031687315486
- @maverickecom (190L/226BM/11kV): Repurpose winning TTS content across hundreds of creator-style accounts (bulk-account; not compliant). — https://x.com/maverickecom/status/2107470108515782720
- @NotZainAgain (73L/82BM/13kV): 2026 TikTok Shop playbook incl. 1,000 free samples/mo. — https://x.com/NotZainAgain/status/2080321911918125500
- @maverickecom (57L/64BM/6kV): Affiliate made $724k GMV/30d; 3 of top 10 TTS affiliates are AI pages (claim). — https://x.com/maverickecom/status/2103161679421071603
- @maverickecom (56L/61BM/10kV): 550 AI videos/day via AI affiliate army (bulk-account; not compliant). — https://x.com/maverickecom/status/2079593540380684296
