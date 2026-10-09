# BOT.md · generate a "Text-on-skin / text-on-palm static"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 1 static 1080x1350 (or a 6s video)), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@Outscaler](https://x.com/Outscaler/status/1919120416485855259) · A collagen ad from Kollo Health (shared as an example of the 'text on skin' concept): a close-up of a woman's face with small paper-style stickers stuck on her skin — "wrinkles?" and "Kollo" — and the caption "Visible results in as little as 28 days". A second version does the same on a man's face ("it's also for blokes!"). The words sit right on the skin where the problem is.
- Example: [@S1R3NH3AD](https://x.com/S1R3NH3AD/status/1708930597014384941) · saw this ad and you will never believe what i thought she was writing on her arm

### Live paid ads in this format (1 in [adlibrary/](adlibrary/README.md), longest-running first)

- **Alicia Darling: Gym-clock POV with sticky caption ("Black leggings so I hope no one notices")** (319 days live): A POV of sneakers on a gym floor, a flip-clock "10:45" overlay, a white caption bubble: "Black leggings so I hope no one notices 😅". 4 variants ("At least no one else will smell me now"). Alicia Darling has 710 ads.

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| Main | Close-up of a wrist or collarbone with a word written in eyeliner or skin-safe marker, the necklace or bracelet sitting right next to it | Word on skin: "waterproof." |
| Variant A | Palm facing camera, the ring on a finger | On palm: "shower-proof" |
| Variant B | Collarbone with a small sticker label (like Kollo's), pointing at the necklace | Sticker: "still gold after 9 months" |
| Corner | Small logo + offer | "Any 7 for $85" |

### Prompts

**Shoot**

```
Natural window light, macro or 2x lens, skin in focus, writing in neat handwriting (not a font).
```

**Word bank (Claude)**

```
List 20 one- to three-word benefits for [product] that would look good written on skin.
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
- [ ] Files named `F33-<concept>-<variant>`; tracking tag `utm_content=F33-<concept>-<variant>`.
- [ ] Avoid: The writing must be real handwriting; fonts look fake.
- [ ] Avoid: Keep it to 1-4 words; skin is a small canvas.
- [ ] Avoid: Use skin-safe products and say so if asked.

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
5. Name every asset `F33-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F33
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

A close-up photo where the message is written (pen/eyeliner-style) directly on skin — palm, inner wrist, collarbone — next to the product. Lo-fi, intimate, impossible to read as a brand template.

### Why it works

- Pattern break: handwriting on skin stops the thumb.
- Intimate/personal — reads as a note-to-self or confession.
- For jewelry the skin shot doubles as a product-on-body shot.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| Static 1 | Inner wrist with bracelet stack; on palm: "6 months. never took it off." | Primary text: short story |
| Static 2 | Collarbone with herringbone; on shoulder: "yes I shower in it" | — |
| Static 3 | Hand with rings; on fingers (one word each): "OCEAN PROOF" | — |

### Hooks

- "never took it off"
- "yes, I shower in it"
- "$85 for 7"
- "note to self: stop buying jewelry that turns green"
- "his mom asked where it's from"

### Production recipe

1. Shoot real hands/wrists (diverse skin tones) with LC pieces in daylight; write with skin-safe eyeliner pencil.
2. Or composite handwriting in post (Procreate) — keep it believable.
3. Short message ≤6 words; long primary text tells the story.
4. 3 skin locations × 4 messages = 12 statics.

### Existing bot prompt

```
Write 20 text-on-skin messages (≤6 words, handwritten tone, lowercase) for LC waterproof 14K PVD jewelry, each paired with a body location (palm, inner wrist, collarbone, fingers) and the LC piece in frame. Then write 80-word first-person primary text for the best 5.
```

### Variants to test

- Real handwriting vs composited
- Skin location
- Message type (proof / price / identity)

## Reference examples

See [examples/README.md](examples/README.md) (6 posts). Top 5:

- @ads4apps (412L/930BM/27kV): 39 Meta formats that convert (930 bookmarks): X reasons, IG story, us vs them, Venn, don't buy this, iPhone notes, text message, low stock, we're sorry, breakin — https://x.com/ads4apps/status/2081785032679518490
- @FedotOff90 (110L/208BM/9kV): 37 formats printing (with days active): AI podcast 280d, report card, iPhone Notes, text on skin, Reddit, cross-out, fake PDP, tier list, myth vs fact, zero sta — https://x.com/FedotOff90/status/2104949773539442831
- @raph_guilhem (9L/6BM/377V): 35 static/native formats tree: Trustpilot, text msg, email screenshot, Reddit, text on skin, crossed-out, tier list, Venn, breaking news. — https://x.com/raph_guilhem/status/2090725512976970065
- @EmerieOnoh (6L/6BM/498V): Static formats printing: us vs them, whiteboard, breaking news, doodle, low stock, iPhone notes, Google search, we're sorry, Reddit, tweet screenshot, text on p — https://x.com/EmerieOnoh/status/2098426706612683154
- @Yannlce (3L/2BM/1kV): Same 40-format list (adds claymation, AI podcast). — https://x.com/Yannlce/status/2085017654364958737
