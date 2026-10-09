# BOT.md · generate a "Buyer's-guide warning: 'Before you buy X, flip the label' (3-2-1 countdown, only one passes)"

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
5. Name every asset `F94-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F94
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

An educational warning video aimed at people already shopping the category: "Before you buy X, watch this." The presenter picks up typical products, flips them over, reads the small print, and counts down 3 reasons (3, 2, 1) why only one option meets the standard. It is a buyer's guide where the standard is defined so only the brand passes.

### Why it works

- It catches product-aware shoppers comparing options (and Amazon look-alikes) at the moment of choice.
- "Flip it over and read the small print" is a demonstrable, repeatable proof the viewer can do at home.
- The countdown structure keeps people watching to #1.
- Defining the standard ("bonded, not painted") makes cheaper alternatives disqualify themselves.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0:00-0:04 | Hands hold 3 generic gold necklaces on cards | "Warning: before you buy waterproof gold jewelry, flip the card over." |
| 0:04-0:20 | #3: card reads "gold tone" / "gold plated" | "Three: 'gold tone' means paint over brass. That's what turns green." |
| 0:20-0:35 | #2: "18K gold-plated, 0.5 micron" | "Two: plating thinner than a hair wears off in weeks of showers." |
| 0:35-0:50 | #1: LC card "14K PVD bonded, stainless base" | "One: PVD is bonded, not painted. That's why you can swim in it." |
| 0:50-1:00 | Shower demo + offer | "Any 7 for $85, waterproof. Link below." |

### Hooks

- "Before you buy 'waterproof' gold jewelry, flip the card over."
- "Warning: most 'gold' necklaces under $50 say this in the small print."
- "Three things to check before you buy gold jewelry online."

### Production recipe

1. List the 3-4 label terms a buyer meets (gold tone, gold plated, gold filled, vermeil, PVD) and what each truly means.
2. Buy 3 generic unbranded pieces as props; never show a competitor brand name.
3. Shoot hands-only (cheap, scalable) plus one presenter version.
4. End with a real shower or ocean demo.

### Existing bot prompt

```
Write a 60-second "before you buy, flip the label" countdown for LC: 3 label terms shoppers see (from {{LABEL_FACTS}}), what each means in one sentence, #1 = LC 14K PVD bonded. All statements must be factually accurate and generic (no brand names). End with a demo line and the offer.
```

### Variants to test

- Hands vs presenter
- Countdown vs checklist
- Warning hook vs question hook

## Reference examples

See [examples/README.md](examples/README.md) (5 posts). Top 5:

- @MaximilianMoj (0L/0BM/0V): Resilia "$36M/month" (unverified) top 5 ads via Playhead teardowns: candida, aged garlic 4-week arteries, GLP-1, urgency (8 at once), animated explainer. — https://x.com/MaximilianMoj/status/2101002307160731848
- @lorenzo_pravata (0L/0BM/0V): Resilia 6,000 ads, parasite cause-relocation angle, "That's parasites" roll-call, carvacrol gate; 10+ subpages to avoid bans. — https://x.com/lorenzo_pravata/status/2065407167515984348
- @HenryCrochemore (6L/10BM/1kV): Worth breaking this one down. brand: thriving through midlife. hook: "spring sale | up to 63% off . today only". specific: sounds too good to be true? try it be — https://x.com/HenryCrochemore/status/2087894849618087981
- @nicklaunches (23L/4BM/977V): Before you buy ANY directory ad, ask these 4. &gt; who measures the traffic, them or a third party &gt; how many ads rotate through the same spot &gt; is it on  — https://x.com/nicklaunches/status/2105130548155056153
- @kevalb26 (7L/3BM/760V): BlackRock is buying Shapoorji bonds. Retail platforms are already using this as a marketing hook. Before you buy “the bond BlackRock bought” read this. 🧵 — https://x.com/kevalb26/status/2075939546467119410
