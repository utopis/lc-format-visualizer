# BOT.md · generate a "Foreign-insider story ('I lived in Seoul for 2 years and learned what Korean women actually use')"

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
5. Name every asset `F92-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F92
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

A first-person story where the narrator spent time inside another culture (Seoul office, Swiss clinic, Japanese pharmacy) and noticed that local women do one thing differently. A local colleague explains the mechanism over dinner, the narrator brings it home, and family members ask "did you get work done?" The authority comes from the place and the insider, not a doctor.

### Why it works

- An open loop ("I just learned what Korean women actually use") with no pain named, so it reaches people who are not yet problem-aware.
- The mechanism arrives as overheard dialogue from an insider, which reads as discovery.
- Proof is layered: her own results, then the insider's reaction, then three unprompted relatives.
- No discount needed: Inceptly notes the $1M/mo ad has no urgency or offer.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0:00-0:09 | Narrator to camera, suitcase or airport B-roll | "I spent the summer working with a goldsmith in Amalfi. When I came home, everyone asked if my jewelry was real gold." |
| 0:09-0:50 | The insider: a local woman who swims every day in her chains | "She never took her necklaces off. Salt water, sun, nothing. I had a drawer of green-stained pieces at home." |
| 0:50-1:40 | Mechanism as dialogue | "'You buy gold that is painted on. We buy gold that is bonded.' That's the only difference." |
| 1:40-2:20 | Proof pattern: sister, best friend, coworker ask unprompted | "My sister grabbed my wrist: 'Is that real?'" |
| 2:20-2:40 | Permission close + CTA | "If your jewelry keeps turning green, it's not you. It's the plating. Any 7 for $85." |

### Hooks

- "I spent 2 years working in [place]. When I came home, everyone asked the same question."
- "Women in [place] never take their jewelry off. Here's why."
- "The thing a [country] jeweller told me that every American woman should know."

### Production recipe

1. Only use a real trip, supplier or designer story. If there is none, use F27 founder story instead.
2. Write the three proof reactions from real customer quotes.
3. Keep the mechanism to one sentence ("painted on vs bonded").
4. Cut 60 s, 2 min and 3 min versions.

### Existing bot prompt

```
Using LC's real sourcing/design story {{TRUE_STORY}}, write a 2-minute first-person "foreign insider" script: open loop in line 1 (no pain named), insider character explains bonded PVD vs plating in one line of dialogue, 3 unprompted reactions from family, permission close ("it's not your fault, it's the plating"), CTA any 7 for $85. Flag every line that must be fact-checked.
```

### Variants to test

- Place/insider
- Spoken vs sung
- Length

## Reference examples

See [examples/README.md](examples/README.md) (7 posts). Top 5:

- @EcomSapo (0L/0BM/0V): Smooche top ad of 1,600+: "At 63 I ran into my ex at Walmart" + Seoul colleague, 5:37; Atria #1 of 721, 70d. "Resilia blueprint works for skincare." — https://x.com/EcomSapo/status/2103047669556166886
- @CSRIPPER (0L/0BM/0V): "10 minute movie ad with a Japanese/Swiss authority": Resilia, Lymphoria all run them. — https://x.com/CSRIPPER/status/2101315284753629664
- @ladprofit (0L/0BM/0V): US Under Secretary flagged scam ads using "hidden knowledge" ethnic secrets + romantic-betrayal drama; quoted re Resilia. — https://x.com/ladprofit/status/2100156940483760583
- @EcomSapo (157L/218BM/24kV): Smooche ($22M/mo skincare) uses singing ads as acquisition weapon. — https://x.com/EcomSapo/status/2105288429873528875
- @TradCathKeng (17L/0BM/446V): And now I’m getting ads for Japanese women only dating apps for foreigners… https://t.co/FV4Mr3dxTA — https://x.com/TradCathKeng/status/2082497271195709774
