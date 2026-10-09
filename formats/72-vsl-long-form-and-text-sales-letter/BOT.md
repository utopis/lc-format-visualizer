# BOT.md · generate a "VSL: long-form video sales letter (2-25 min) and its text twin (TSL)"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 2-6 min first cut (up to 25 min), plus a matching text sales letter page), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@FedotOff90](https://x.com/FedotOff90/status/2095237367925731363) · A long-form VSL of about 4 to 5 minutes: a woman telling her story to camera ("Over 40"), with cutaways to an orange being peeled, a woman in bed, a red-light device on skin and close-ups of skin. It is slow, story-led and sells late.
- Example: [@FedotOff90](https://x.com/FedotOff90/status/2087245595249721445) · 97-day VSL; VSLs spent millions profitably; full VSL Machine SOP.

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| 0:00-0:30 Hook | Narrator to camera or story B-roll | Personal problem in one sentence: "My mother's gold chain turned her neck green the day of my wedding." |
| 0:30-2:00 Story + villain | B-roll of the problem, archive-style photos | Why the usual fixes fail ("plating is a coat of paint, it wears off") |
| 2:00-3:30 Mechanism | Diagram / macro of the material | How PVD bonding works in plain words |
| 3:30-4:30 Proof | Real customer clips, review screenshots, water test | Specific, verifiable proof only |
| 4:30-5:30 Offer + guarantee | Product grid, offer card | Bundle, price, guarantee terms, shipping |
| 5:30-6:00 CTA | Narrator | One clear action, repeated once |

### Prompts

**Claude (outline)**

```
Outline a 6-minute VSL for [product] with sections hook, story, villain, mechanism, proof, offer, guarantee, CTA. Give each a timing, the exact spoken lines and the B-roll list. Every claim must come from this product page: [paste].
```

**Text twin (TSL)**

```
Turn the VSL script into a long-form landing page with the same headlines as H2s, pull quotes from real reviews and the offer box repeated 3 times.
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
- [ ] Files named `F72-<concept>-<variant>`; tracking tag `utm_content=F72-<concept>-<variant>`.
- [ ] Avoid: Long form makes weak claims more visible, not less; substantiate everything.
- [ ] Avoid: Test a 2-minute cut against the long version before shooting a 20-minute one.
- [ ] Avoid: Most viewers drop before the offer; put a mini-offer at 60-90s too.

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
5. Name every asset `F72-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F72
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

A single video that takes cold viewers through problem → villain → mechanism → authority → proof → offer → guarantee. Lengths run from 2 minutes to 25 minutes, and "extra long" (double normal length) is a test in itself. The text sales letter (TSL) is the same skeleton as a long page with an order form at the bottom.

### Why it works

- Educates and closes in one sitting, with no retargeting needed.
- Long watch time trains the algorithm on high-intent viewers.
- One winning VSL can absorb very large budgets (Fedotoff: "spent millions profitably").

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0-15s | Hook: the green neck mark / the necklace in the shower | "If you've ever taken your necklace off before a shower, watch this." |
| 15-60s | Villain: plating that wears off | "The coating on most gold jewelry is thinner than a hair." |
| 1-2 min | Mechanism: PVD bonding, 14K | founder explains |
| 2-3 min | Proof stack: reviews, wear tests | real numbers |
| 3-4 min | Offer + guarantee | "Any 7 for $85, [real guarantee]" |

### Hooks

- "The coating on your jewelry is thinner than a hair"
- "Why your gold turns green (and what jewelers don't say)"
- "I tested 12 waterproof necklaces for 30 days"

### Production recipe

1. Write a 7-beat script (≈450 words for 3 min).
2. Shoot the founder plus B-roll, or use an AI narrator with real product footage (disclosed).
3. Send it to a dedicated lander, not the PDP: the page continues the video.
4. Test 3 hooks on the same body.

### Existing bot prompt

```
Write a 3-minute LC VSL on the 7-beat skeleton (hook, villain, mechanism, authority, proof, offer, guarantee) using only {{PDP_FACTS}} and {{REAL_PROOF}}. Then condense it into a 900-word text sales letter with the same beats.
```

### Variants to test

- Length 2 vs 4 vs 8 min
- Founder vs narrator
- VSL vs TSL

## Reference examples

See [examples/README.md](examples/README.md) (7 posts). Top 5:

- @FedotOff90 (83L/152BM/17kV): 97-day VSL; VSLs spent millions profitably; full VSL Machine SOP. — https://x.com/FedotOff90/status/2087245595249721445
- @FedotOff90 (49L/103BM/8kV): "VSLs… most scalable ad format by far" — 300 VSLs with 30+ day runtime. — https://x.com/FedotOff90/status/2095237367925731363
- @FedotOff90 (110L/208BM/9kV): 37 formats printing (with days active): AI podcast 280d, report card, iPhone Notes, text on skin, Reddit, cross-out, fake PDP, tier list, myth vs fact, zero sta — https://x.com/FedotOff90/status/2104949773539442831
- @EricSchechter (66L/46BM/3kV): Don’t overcomplicate testing offers, especially in the beginning. Some of our biggest affiliates on Meta right now are doing hundreds to 1,000+ orders a day run — https://x.com/EricSchechter/status/2100245791776428230
- @williamkast_ (28L/34BM/3kV): 5 formats to test: founder talking head, voiceless B-roll text overlay, yapper (uncut), AI educational, camouflage static + long copy. — https://x.com/williamkast_/status/2078179704050246125
