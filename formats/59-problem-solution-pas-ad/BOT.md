# BOT.md · generate a "Problem → agitation → solution → proof (4-part PAS ad, video or static)"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 20-40s video or a 4-panel static), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@ayomikunszn](https://x.com/ayomikunszn/status/2078116608069800131) · A 4-image static concept for a weekender bag: the product on its own with feature icons, a man carrying it ("GO FURTHER"), the bag open ("ROOM FOR EVERYTHING") and a 5-star review card.
- Example: [@Jordan_Created](https://x.com/Jordan_Created/status/2017403665741742102) · Here is a UGC Example breaking down the PAS framework. To take this 1 step further: - Hook - Problem - Agitate - Solution - CTA Adding in "Agitate" he
- Example: [@alice_ercolani](https://x.com/alice_ercolani/status/2048553690215444873) · Sleepway's ads use a classic marketing formula: Problem → Agitate → Solution. This ad starts with a doctor and a stark warning: "DON'T SLEEP THIS WAY!
- Example: [@rayyanmru](https://x.com/rayyanmru/status/1930403658061000934) · 🚨 Ad Breakdown: Pet Lab Co’s UGC that prints money This ad preys on a hidden fear every dog owner has and it works like crazy. Bad breath? Tartar? Tha
- Example: [@TobyWalleruk](https://x.com/TobyWalleruk/status/1734535147591012689) · Why this ad works ✅ Has an intriguing HOOK ✅ Handles objections & answers FAQ’s ✅ Transitions throughout every 2 seconds ✅ Uses the Problem-Agitate-So

### Live paid ads in this format (2 in [adlibrary/](adlibrary/README.md), longest-running first)

- **Deborah Hayes: "Spa treatments for belly fat don't work" two-layer explainer** (286 days live): "Spa treatments for belly fat don't work. And there's a scientific reason why… I did six spa sessions… $1,200… Your belly fat has two types of fat… these only work on surface fat." UGC plus a medical-paper insert plus CGI. 126 s.
- **BioRoot Labs: "Relief like ibuprofen without the stomach pain" ingredient static** (179 days live): A static: "Relief Like Ibuprofen, Without the stomach pain", 3 bottles, a "45,000+ trusted" badge, and an ingredient grid (turmeric anti-inflammatory, black pepper absorption, bee propolis immune, ginger digestive, coconut oil lipid carrier, vitamin C antioxid

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| Problem (0-5s) | Green mark on a finger | "Your gold ring turned your finger green." |
| Agitation (5-12s) | Money down the drain: a drawer of tarnished pieces | "Again. That's the fourth one this year." |
| Solution (12-22s) | PVD ring under a tap | "14K PVD over stainless steel doesn't wear off." |
| Proof (22-32s) | Review screenshots, 9-month-old piece | "4.8 stars from 4,812 reviews." |
| End | Offer | "Any 7 for $85." |

### Prompts

**Claude**

```
Write 5 PAS scripts for [product]: one line each for problem, agitation, solution, proof, CTA. Proof must be real.
```

**Static version**

```
4 panels in a 2x2 grid, one word header each: PROBLEM / WHY / FIX / PROOF.
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
- [ ] Files named `F59-<concept>-<variant>`; tracking tag `utm_content=F59-<concept>-<variant>`.
- [ ] Avoid: Don't over-agitate; it reads as fear-mongering.
- [ ] Avoid: Proof must be specific and real.
- [ ] Avoid: Keep each beat to one line.

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
5. Name every asset `F59-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F59
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

The classic direct-response structure: name one specific pain so the right person thinks "that's me", agitate it (consequences, failed fixes), introduce the product as THE fix for that pain, close with specific proof and one CTA. One problem per ad — five benefits = five ads.

### Why it works

- Meets the viewer where they already are emotionally.
- Specific proof ("4.8★ from 12,000 reviews") beats generic.
- Scales cleanly: one ad per pain point.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0-5s | Close-up green ring mark on finger | "If your rings leave a green line, this is for you." |
| 5-20s | Taking jewelry off before every shower/pool; tangled tray | "I tried clear nail polish, 'hypoallergenic' plating… still green in a week." |
| 20-40s | LC piece in shower and pool | "This is what finally let me stop taking it off: 14K PVD, bonded not plated." |
| 40-60s | Real review count + any 7 for $85 | "[real rating/count]. Any 7 for $85." |

### Hooks

- "If your rings leave a green line, this is for you"
- "Tired of taking your necklace off every night?"
- "Still buying gifts she never wears?"

### Production recipe

1. List LC pain points from reviews; one ad per pain.
2. Cover-the-product test: first 15s must stand alone as a portrait of the problem.
3. Proof must be real and specific (review count/rating from the actual platform).

### Existing bot prompt

```
For each LC pain point in {{PAINS}}, write a 45-60s PAS script with the 4 timed phases; proof only from {{REAL_PROOF}}. Also a static version: headline (pain) / body (agitation) / product visual / CTA.
```

### Variants to test

- Pain point
- Video vs static
- Creator vs founder

## Reference examples

See [examples/README.md](examples/README.md) (3 posts). Top 5:

- @alexpagepilot (11L/19BM/1kV): Top 5 dropship formats: UGC problem/solution, "TikTok made me buy it", us vs them split, founder talking head (retargets 2-3x), text-overlay slideshow. — https://x.com/alexpagepilot/status/2099438014456045990
- @ayomikunszn (26L/5BM/1kV): Created these Weekender Bag ad concepts after studying what's working for leading DTC travel brands on Meta. Each creative focuses on a different conversion ang — https://x.com/ayomikunszn/status/2078116608069800131
- @mattgittleson (0L/0BM/0V):  — https://x.com/mattgittleson/status/2107530746923823444
