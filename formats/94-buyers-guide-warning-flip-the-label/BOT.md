# BOT.md · generate a "Buyer's-guide warning: 'Before you buy X, flip the label' (3-2-1 countdown, only one passes)"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 30-50s, 1080x1920), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@HenryCrochemore](https://x.com/HenryCrochemore/status/2087894849618087981) · A grotesque, stretched-face claymation character at a podcast mic reading the label of a skincare product ("WE JUST MOVED", "EVERY CREAM BEFORE", "HYDROLYZED HYALURONIC ACID", "61% OFF"). It is a buyer's guide delivered by an unforgettable character.
- Example: [@SuurajN35299](https://x.com/SuurajN35299/status/2038318041457741869) · Stop! 🛑 Before you buy that gold chain, check the clasp for these 3 stamps: GP GEP HGE If you see them, you're buying plated jewelry, not solid gold. 
- Example: [@Amiragoldgroup](https://x.com/Amiragoldgroup/status/2080124641826242894) · Thrift stores can hide incredible treasures—but never assume every piece is real. Always verify, test, and inspect before you buy. A few minutes of ch
- Example: [@OrvanyaIndia](https://x.com/OrvanyaIndia/status/2084213867505435020) · Before you buy gold as an investment or commodity/wearable next time, remember these 5 common mistakes and plan accordingly #gold #investment #jewelle
- Example: [@NatxtraSynthite](https://x.com/NatxtraSynthite/status/2078344172885700790) · Don't buy a supplement without reading the label. The real story is in the ingredients, dosage, and hidden extras—not the marketing. Read the label be
- Example: [@nicklaunches](https://x.com/nicklaunches/status/2105130548155056153) · Before you buy ANY directory ad, ask these 4. &gt; who measures the traffic, them or a third party &gt; how many ads rotate through the same spot &gt;

### Live paid ads in this format (4 in [adlibrary/](adlibrary/README.md), longest-running first)

- **British Supplements: Google-search UI static ('Which UK brand has no fillers?')** (331 days live): A Google search bar with an autocomplete question 'Which UK brand has no fillers?', a cursor clicking it, then a featured-snippet style answer box with ticks and product photos.
- **BioRoot Labs: "Relief like ibuprofen without the stomach pain" ingredient static** (179 days live): A static: "Relief Like Ibuprofen, Without the stomach pain", 3 bottles, a "45,000+ trusted" badge, and an ingredient grid (turmeric anti-inflammatory, black pepper absorption, bee propolis immune, ginger digestive, coconut oil lipid carrier, vitamin C antioxid
- **Resilia · Resilia: “Do not believe resilient oil of oregano. They said it would support…”** (2 days live): Opens: “Do not believe resilient oil of oregano. They said it would support bloating and improve digestion.”
- **Resilia · Natural Defense Report: “Do not buy resilient oil over regular. They said it was to support…”**: Opens: “Do not buy resilient oil over regular. They said it was to support bloating and improve digestion.”

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| 0-3s | Presenter at a table with 3 typical gold pieces (generic, unbranded packaging) | "Before you buy gold jewellery, flip the label." |
| 3-12s | Check 3: picks up piece 1, label close-up | "'Gold tone' means there's no gold. Fails." |
| 12-22s | Check 2: piece 2 | "'Gold plated' with no thickness listed means it wears off. Fails." |
| 22-32s | Check 1: the PVD piece | "'14K PVD over stainless steel'. Bonded, waterproof. This one passes." |
| 32-40s | Drops it in a glass of water, lifts it out | "That's the one I wear." |
| End | Offer | "Any 7 for $85." |

### Prompts

**Script (Claude)**

```
Write 3 label checks shoppers can do themselves for [category], each one true and verifiable, from weakest to the product. Max 15 words per line.
```

**Shoot**

```
Top-down + presenter angle, macro on labels, neutral packaging with competitor names removed.
```

### QA checklist (all must pass before hand-off)

- [ ] Hook lands in the first 1.5 s (video) or is readable at thumbnail size (static / slide 1).
- [ ] Removal test: delete the product from the script. If it still makes sense, rewrite so the product is the payoff.
- [ ] Matches the reference structure (same beat order and length band) before any creative twist.
- [ ] Uses only real product imagery for the product; AI is for backgrounds, characters or b-roll, and is disclosed where required.
- [ ] Every claim is on the brand's approved-claims list (PDP); no invented stats, reviews, doctors or customers.
- [ ] Captions burned in and inside the safe zone; sound-off still understandable.
- [ ] One clear CTA that matches the landing page offer.
- [ ] Three hook variants delivered for the same body (test hooks, not whole new ads).
- [ ] Files named `F94-<concept>-<variant>`; tracking tag `utm_content=F94-<concept>-<variant>`.
- [ ] Avoid: Don't name or show competitor brands; use generic packaging.
- [ ] Avoid: Every label claim must be accurate (e.g. what "gold tone" legally means).
- [ ] Avoid: Show the product passing a test it really passes.

<!-- QUICKSTART:END -->

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
