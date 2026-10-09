# BOT.md · generate a "Poll-sticker & product-match quiz ads (interactive A/B polls → retarget by answer)"

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
5. Name every asset `F61-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F61
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

Interactive creatives: a two-option poll sticker on a Story/Reel ad ("Herringbone or paperclip?") and/or a short product-match quiz ("Find your stack in 30s") as the destination. Answers create segments you retarget with matching creative.

### Why it works

- Low-friction participation lifts engagement and gives first-party preference data.
- Retargeting by answer = personalised follow-up creative.
- Quiz → personalised result page reduces choice paralysis for a 7-piece bundle.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| Story ad | Two pieces side by side; poll sticker "Which would you wear daily?" | — |
| Retarget A | Ad featuring the chosen piece + "you picked herringbone" | — |
| Quiz | 5 questions (style, metal, occasion, budget, recipient) → "Your 7-piece stack" | Optional email for results |

### Hooks

- "Herringbone or paperclip? Vote."
- "Gold every day or only weekends?"
- "Find your 7-piece stack in 30 seconds"

### Production recipe

1. Polls: Stories ads with poll sticker (Meta supports polls on Reels/Stories ads).
2. Engagement custom audiences by answer where available; else retarget engagers with both variants.
3. Quiz: 5-7 questions on LC site (strategy 04), result = curated 7-piece cart.

### Existing bot prompt

```
Write 10 two-option poll prompts for LC (style/metal/occasion debates) and a 6-question product-match quiz mapping answers to {{SKUS}} → a 7-piece result + copy.
```

### Variants to test

- Poll vs quiz
- Story vs Reel placement

## Reference examples

See [examples/README.md](examples/README.md) (14 posts). Top 5:

- @IgorWoorts (110L/147BM/6kV): There is NO single landing page that works best for all your ads. It all depends on the awareness stage. Unaware → listicle / quiz funnel (educate around the pr — https://x.com/IgorWoorts/status/2084623022649188607
- @codyschneider (67L/92BM/7kV): an AI agent is running facebook ads for a local business it just got the 2170 ebook downloads in august 16% of people who download the ebook turn into a future  — https://x.com/codyschneider/status/2093098436069568758
- @lorenzo_pravata (28L/21BM/3kV): We scaled an app from $0 to $50M in 10 months on Meta. The peak month did $3M, counting first purchases only. Subscription LTV came on top of that. And here's t — https://x.com/lorenzo_pravata/status/2079684588620664861
- @JamesEbringer (8L/13BM/2kV): Facebook CPCs in Africa are $0.05 right now Five cents a click Go inside TAP and look for the Africa Ads Method Set up a Facebook ad account Point a simple ad a — https://x.com/JamesEbringer/status/2081462841052151919
- @kailodee (7L/13BM/1kV): Ran ads for a client. 20 calls on the calendar in 3 days. 88% of leads qualified through the quiz funnel. We're already running out of calendar space and lookin — https://x.com/kailodee/status/2095617829051498810
