# BOT.md · generate a "Advertorial-style video ('5 reasons ___ are ditching ___')"

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
5. Name every asset `F79-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F79
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

A 45-120s video built like an editorial article: headline title card, numbered reasons, B-roll, a calm narrator. It educates first, then sends viewers to a matching advertorial lander (news-mimic, listicle, comparison).

### Why it works

- Editorial framing lowers ad defences.
- The numbered structure keeps viewers watching to the end of the list.
- Pairs with lander formats that continue the article.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0-5s | Title card: "5 reasons women are ditching gold-plated jewelry" | VO reads it |
| 5-60s | Reasons 1-5 with B-roll (green mark, swim, cost per wear, gift) | calm VO |
| 60-75s | "Reason 5 is why we built LC" | CTA to listicle lander |

### Hooks

- "5 reasons women are ditching gold-plated jewelry"
- "The real reason your necklace turns green"
- "Why jewelers hate waterproof gold"

### Production recipe

1. Pick the lander first (listicle or comparison), then mirror its reasons in the video.
2. B-roll from own shoots.
3. Neutral narrator voice; no fake news branding.

### Existing bot prompt

```
Write a 75s advertorial-style video script for LC: title card, 5 numbered reasons (true, from {{PDP_FACTS}}), a close that hands off to a matching listicle lander. Also outline the lander H1/H2s.
```

### Variants to test

- Listicle vs myth-bust framing
- Narrator vs text-only

## Reference examples

See [examples/README.md](examples/README.md) (6 posts). Top 5:

- @FedotOff90 (175L/385BM/47kV): 6 lander/advertorial types (news mimic, story, listicle, quiz, authority, comparison) — 53-format lander database. — https://x.com/FedotOff90/status/2094854572623675832
- @FedotOff90 (145L/318BM/11kV): 24 landing page formats with live ad→lander pairs (breaking news, investigation, as-seen-on-TV, doctor warning…). — https://x.com/FedotOff90/status/2092382176738202057
- @funneloftheweek (0L/0BM/0V): Resilia: 12 persona Pages → one 7-min advertorial (30-50% of traffic), 3-4 copy templates × hundreds of creatives, 544 new ads/30d, OTO flow $30→$83. — https://x.com/funneloftheweek/status/2044464896104857850
- @phemeinfluence (224L/41BM/15kV): 🐶 PET UGC OPPORTUNITY 35+ (cats or dogs moms) BRAND: Chewy PAY: $2000 + Product Pet brand hiring UGC creators to film a 90s advertorial video featuring you + yo — https://x.com/phemeinfluence/status/2078934717462888585
- @k4komaaaal (16L/7BM/655V): 10 reasons why brands are ditching polished ads for founder faces on camera: 1. sushiswap, gymshark all started founder led content before ads 2. face on camera — https://x.com/k4komaaaal/status/2084289721703010738
