# BOT.md · generate a "Streak calendar static (a habit grid filled with ✓ days)"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 1 static 1080x1350), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@iwo_cybulski](https://x.com/iwo_cybulski/status/1833960761489813736) · A static ad for a beef-tallow cooking fat: a split image labelled DAY 1 and DAY 30 — a frying pan on the left, a happy family at a dinner table on the right — with benefit pills under each side. It is the closest real example we found to a streak / progress-over-time static; there is no checkmark calendar grid.

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| Main | A 30- or 90-day calendar grid, each day ticked in gold marker | "90 days. Never taken off." |
| Detail | A few day boxes with tiny notes | "sea" "gym" "wedding" "shower" |
| Product | The necklace laid across the bottom of the calendar | - |
| Corner | Offer | "Any 7 for $85" |

### Prompts

**Real version**

```
Print a calendar, tick days for real as a team member wears it, photograph it at the end.
```

**Figma**

```
Calendar grid 7x13, gold ticks, handwritten notes in 4-5 cells.
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
- [ ] Files named `F68-<concept>-<variant>`; tracking tag `utm_content=F68-<concept>-<variant>`.
- [ ] Avoid: If you claim 90 days, someone should really have worn it 90 days.
- [ ] Avoid: Keep notes tiny; the grid is the visual.
- [ ] Avoid: No clean public example of this exact format was found; test it before scaling.

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
5. Name every asset `F68-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F68
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

A month-grid or habit-tracker static, filled in day by day (✓, X, or small photos), that shows a streak: "90 days, 0 times taken off". Proof of consistency becomes the visual.

### Why it works

- Calendars are a familiar personal artefact and don't read as an ad.
- A long streak says "it lasts" without making a claim.
- Easy to localise: summer, swim season, wedding month.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| Static | Paper calendar or Notes-style grid, every day ticked with gold marker; the necklace lies across the grid | Headline: "Day 90. Haven't taken it off once." |
| Variant | Grid of 30 small daily wrist/neck photos | "30 days, 30 showers, same chain" |

### Hooks

- "Day 90. Haven't taken it off once."
- "My 30-day shower test"
- "Streak: 214 days, 0 green marks"

### Production recipe

1. Run a real 30/60/90-day wear test with a staff member or customer (with consent).
2. Photograph a real calendar and keep the dates true.
3. Pair it with the F12 timeline video.

### Existing bot prompt

```
Design 4 streak-calendar statics for LC from a real wear test {{TEST_LOG}}: headline ≤8 words, grid description, 120-word primary text. Only real days and results.
```

### Variants to test

- Ticks vs photos
- 30 vs 90 days

## Reference examples

See [examples/README.md](examples/README.md) (3 posts). Top 5:

- @FedotOff90 (110L/208BM/9kV): 37 formats printing (with days active): AI podcast 280d, report card, iPhone Notes, text on skin, Reddit, cross-out, fake PDP, tier list, myth vs fact, zero sta — https://x.com/FedotOff90/status/2104949773539442831
- @iwo_cybulski (0L/0BM/0V):  — https://x.com/iwo_cybulski/status/1833960761489813736
- @monavb04 (3L/0BM/236V): Continuing to build out our open-source shadcn dashboard This time: 💬 Chat 📅 Calendar We wanted these to feel like actual apps rather than just static dashboard — https://x.com/monavb04/status/2089682216209330375
