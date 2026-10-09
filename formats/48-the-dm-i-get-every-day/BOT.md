# BOT.md · generate a "'The DM / question I get every day' answer video"

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
5. Name every asset `F48-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F48
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

Founder/creator shows a real DM or recurring question (blurred sender) and answers it on camera — objection handling disguised as content.

### Why it works

- Answers the #1 objection natively.
- Feels like a reply, not an ad.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0-2s | DM screenshot (blurred) | "I get this DM every day" |
| 2-15s | Qirra answers with demo | Shower demo |
| 15-20s | CTA | — |

### Hooks

- "The DM I get every single day"
- "No, it won't turn green — here's why"

### Production recipe

1. Pull top 10 questions from inbox/comments; real DMs only, blur sender.

### Existing bot prompt

```
From {{INBOX_EXPORT}}, rank the 10 most frequent pre-purchase questions and write a 15s answer script for each using PDP wording.
```

### Variants to test

- Founder vs CS rep

## Reference examples

See [examples/README.md](examples/README.md) (3 posts). Top 5:

- @antonioventre_ (12L/13BM/995V): Customer-SERVICE call ad: record a real pre-purchase support call answering the 5-6 questions buyers actually ask. — https://x.com/antonioventre_/status/2091592059517837677
- @raph_guilhem (55L/105BM/7kV): 30 Meta ad formats folder tree (hooks, founder content, etc.). — https://x.com/raph_guilhem/status/2083288607062732816
- @adamtaylorl (36L/36BM/3kV): Dead in 2026: polished studio, "hey guys" UGC, discount statics, founder-story VSLs. Printing: ugly advertorial statics, long-form yapper, comment-reply hooks,  — https://x.com/adamtaylorl/status/2086814826177679660
