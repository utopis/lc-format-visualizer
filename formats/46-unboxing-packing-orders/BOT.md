# BOT.md · generate a "Unboxing / packing orders (ASMR)"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 20-45s, 1080x1920, ASMR), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@mannyvivianne](https://x.com/mannyvivianne/status/2101756682359480565) · "Pack orders with me": a creator in her room unpacking a shipment and trying on the pieces ("Packed some orders today"), ending with a celebratory toast. It is casual, behind the scenes and in real time.
- Example: [@hi_kikistudio](https://x.com/hi_kikistudio/status/2099776011156214179) · ASMR | Pack Orders With Me ♡ #asmr #stickers #illustration‌‌ #手帳デコ #シール
- Example: [@logies000](https://x.com/logies000/status/2067986905451344307) · Pack orders with me as a small business owner starting a clothing brand 🫡 Shop here: http://L4ESTUDIOS.com
- Example: [@Kilatyanaturals](https://x.com/Kilatyanaturals/status/2095036823839936738) · Pack orders with me! #kilatyasnaturals
- Example: [@vanillaabunnyy](https://x.com/vanillaabunnyy/status/1936279895190991018) · #pressonnails #pressonnailsbusiness pack orders with me as a press on nail business owner‼️ wholesale available for business owners #nailvendor
- Example: [@paasstah](https://x.com/paasstah/status/2092047788695494968) · The perfect fit. Biceps. Anxiety. It’s all in this episode of PACK ORDERS WITH ME
- Example: [@robertythoughts](https://x.com/robertythoughts/status/2096885424656359566) · I built a 7 figure ecom brand at 24... and most of the day it's just me, sitting by myself in my room. I feel like in ecom, it's one of the few busine

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| 0-3s | Top-down: hands open a gold-foiled box, crisp paper sound | Caption: "packing your order" |
| 3-15s | Wrapping each piece in tissue, sticker, card | No voice; real sounds amplified |
| 15-25s | Handwriting a note | "Wear it in the sea. — L" |
| 25-35s | Box closed, tape, label (blurred) | - |
| End | Text on screen | "Any 7 for $85." |

### Prompts

**Audio**

```
Clip-on mic near the table, no music or very low; boost paper and tape sounds +6 dB.
```

**Shoot**

```
Overhead arm, soft top light, 4K 30fps, clean neutral table.
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
- [ ] Files named `F46-<concept>-<variant>`; tracking tag `utm_content=F46-<concept>-<variant>`.
- [ ] Avoid: Blur names and addresses.
- [ ] Avoid: Keep hands and nails clean and consistent.
- [ ] Avoid: ASMR needs real sound; music ruins it.

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
5. Name every asset `F46-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F46
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

"Pack an order with me" (founder/team ASMR) or customer unboxing of the LC box — tactile, satisfying, shows packaging and gift readiness.

### Why it works

- ASMR + packaging = gift signal.
- Cheap volume content; a "new style" lever for stuck accounts.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0-2s | Top-down box | "Packing a 7-piece stack for Dana in Ohio" |
| 2-20s | Each piece placed | ASMR |
| 20-25s | Box closed + note | "any 7 for $85" |

### Hooks

- "Pack a 7-piece order with me"
- "Unboxing the gift I asked for"

### Production recipe

1. Top-down tripod; good mic; no customer PII on labels.

### Existing bot prompt

```
Write 10 pack-with-me captions and hooks using real order types {{ORDERS}} (no customer full names).
```

### Variants to test

- Founder vs customer

## Reference examples

See [examples/README.md](examples/README.md) (7 posts). Top 5:

- @nicktheriot_ (219L/348BM/12kV): 2026 FB creative styles tier list: S = long primary text + organic image, LTO, UGC, VSL, reaction, news; A = demo, us vs them, testimonial, close-up, founder st — https://x.com/nicktheriot_/status/2108173638033871013
- @nicktheriot_ (45L/55BM/4kV): Stuck-account order: new avatar → new style (AI UGC, animation, unboxing, reaction, native) → curiosity text hook → uncommon location → combos. — https://x.com/nicktheriot_/status/2096219973139992840
- @Ecombos_Ai (28L/26BM/2kV): 10 AI UGC styles: talking-head testimonial, product-in-hand, first-try reaction, fake podcast, street interview, comment reply, unboxing, DITL/GRWM, before/afte — https://x.com/Ecombos_Ai/status/2103180929057407425
- @rirahcreates (12L/17BM/1kV): 20 UGC types: talking head, review, unboxing, testimonial, demo, problem/solution, before/after, GRWM, DITL, voiceover, routine, how-to, FAQ, 3 reasons why, POV — https://x.com/rirahcreates/status/2089827933561016787
- @raph_guilhem (55L/105BM/7kV): 30 Meta ad formats folder tree (hooks, founder content, etc.). — https://x.com/raph_guilhem/status/2083288607062732816
