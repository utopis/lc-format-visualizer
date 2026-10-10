# BOT.md · generate a "Day in the life / behind the scenes (founder or customer)"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 30-60s, 1080x1920), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@ugcAshleyRJ](https://x.com/ugcAshleyRJ/status/2067636022251290725) · A day-in-the-life POV filmed with an ultra-wide 0.5x lens: walking into an office ("Be Empowered" on the wall), working at a round table, a printed magazine spread, with captions explaining the 0.5x POV angle.
- Example: [@adamtaylorl](https://x.com/adamtaylorl/status/2100540269351350453) · 5. Day In The Life… Most brands will list a bunch of boring features. Loop just shows a guy using it for a day. Laptop, backpack, crowd at a live even
- Example: [@adamtaylorl](https://x.com/adamtaylorl/status/2090038019059314970) · 3. The Retail Vlog You're 40 seconds into a dog date before you realize Petco and the ingredients list walked in with it. Stealth education.

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| 0-3s | Founder at 6am packing orders, phone propped on shelf | "A day running a jewellery brand from my spare room." |
| 3-15s | Quick cuts: coffee, emails, quality-checking chains under a lamp | VO with time stamps on screen |
| 15-30s | Testing a necklace in the sink, then a swim at lunch | "Every new piece goes in the sea before it goes on the site." |
| 30-45s | Evening: packing the last box, handwritten note | "Order 412 today." |
| End | Product | Soft CTA |

### Prompts

**Shoot**

```
Phone on a mini tripod, 15-20 clips of 2-4s, natural light; time stamps as captions.
```

**Script (Claude)**

```
Turn this list of real tasks [paste] into a 45-second day-in-the-life with one surprising detail.
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
- [ ] Files named `F45-<concept>-<variant>`; tracking tag `utm_content=F45-<concept>-<variant>`.
- [ ] Avoid: Show the real day, not a staged one.
- [ ] Avoid: One product moment, not five.
- [ ] Avoid: Don't show customer names or addresses on labels.

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
5. Name every asset `F45-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F45
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

Vlog-style sequence of a day — founder running LC or a customer living in her jewelry (gym → shower → work → date) — with the product present in every scene. Paid version: 20-30s cut with text hook.

### Why it works

- Parasocial, native vlog grammar; product proof through continuity (same necklace all day).
- Framework that converts one message into a new Entity ID (@williamkast_).

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0-2s | 0.5x POV alarm, necklace on nightstand? No — already on | "Day in my life wearing the same necklace for 24h" |
| 2-8s | Gym | Sweat |
| 8-12s | Shower | "still on" |
| 12-20s | Work / coffee | Compliment from coworker (real) |
| 20-25s | Pool/dinner | "any 7 for $85" |

### Hooks

- "Day in the life of a jewelry founder (the unglamorous version)"
- "24 hours in the same necklace"
- "A day packing 1,000 orders"

### Production recipe

1. Film with phone 0.5x lens; 8-12 scenes; natural audio.
2. Organic first; paid cut only if organic retention ≥ average.

### Existing bot prompt

```
Turn this list of a real day's scenes {{SCENES}} into a 25s DITL script: hook text, scene captions (≤6 words), and one product moment per scene.
```

### Variants to test

- Founder vs customer
- 0.5x POV vs standard

## Reference examples

See [examples/README.md](examples/README.md) (12 posts). Top 5:

- @nicktheriot_ (219L/348BM/12kV): 2026 FB creative styles tier list: S = long primary text + organic image, LTO, UGC, VSL, reaction, news; A = demo, us vs them, testimonial, close-up, founder st — https://x.com/nicktheriot_/status/2108173638033871013
- @williamkast_ (38L/46BM/3kV): Turn 1 winning ad into 5: same message, different frameworks (DITL, 3 reasons, old me/new me, phone call). — https://x.com/williamkast_/status/2086835243474985414
- @Ecombos_Ai (28L/26BM/2kV): 10 AI UGC styles: talking-head testimonial, product-in-hand, first-try reaction, fake podcast, street interview, comment reply, unboxing, DITL/GRWM, before/afte — https://x.com/Ecombos_Ai/status/2103180929057407425
- @rirahcreates (12L/17BM/1kV): 20 UGC types: talking head, review, unboxing, testimonial, demo, problem/solution, before/after, GRWM, DITL, voiceover, routine, how-to, FAQ, 3 reasons why, POV — https://x.com/rirahcreates/status/2089827933561016787
- @ugcAshleyRJ (13L/5BM/534V): The 0.5x ultra-wide POV filming technique for demos, GRWM and day-in-the-life — immersive, native. — https://x.com/ugcAshleyRJ/status/2067636022251290725
