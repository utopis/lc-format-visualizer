# BOT.md · generate a "Zero Stars rating flip ('5 stars from you / zero stars from them')"

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

- **Main example**: [@cortex_adbrain](https://x.com/cortex_adbrain/status/2103883993603031429) · A 1-star rating flip static for an aluminium phone case (Arc Pulse): one star, the quoted complaint "It's ridiculous, it basically doesn't cover the phone at all.", then "Yep, that's the point." and the benefit.
- Example: [@akhilbuilds](https://x.com/akhilbuilds/status/1808319058200387782) · This humourous 1 star review static ad has performed very well for several brands that I designed it for. People love ads that create intrigue, adds h
- Example: [@sandiegocausa](https://x.com/sandiegocausa/status/2079314429980925993) · Saw this smart ad on my Facebook thread. The 1 star review catches attention, the negative review highlights how good the product is. The only thing I
- Example: [@helloitsdrew_](https://x.com/helloitsdrew_/status/1863574480045461667) · Instead of the usual review/testimonial static, try out an ironic 'negative' one! It's attention grabbing, and potentially entertaining to viewers!

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| Left | Review card: 5 stars from a customer | "5 stars from you." |
| Right | Review card: 0 stars, from the "enemy" | "0 stars from the sea. (It tried.)" |
| Product | Necklace between the two cards | - |
| Corner | Offer | "Any 7 for $85" |

### Prompts

**Claude**

```
Write 10 "zero stars from them" lines where "them" is the problem (the sea, your gym, tarnish, your sister who keeps borrowing it).
```

**Figma**

```
Two review cards, left 5 gold stars, right 0 grey stars; product centred.
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
- [ ] Files named `F69-<concept>-<variant>`; tracking tag `utm_content=F69-<concept>-<variant>`.
- [ ] Avoid: The 5-star review must be real.
- [ ] Avoid: Make the "zero stars" joke obviously playful.
- [ ] Avoid: Don't aim it at a competitor.

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
5. Name every asset `F69-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F69
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

A two-line rating joke: you give it five stars, while an "enemy" (the shower, the pool, tarnish, the jealous friend) gives it zero. Social proof and a benefit packed into a meme-like card.

### Why it works

- A star rating is instantly readable; the twist makes people read the second line.
- It turns the product's durability into a joke the viewer gets.
- Cheap: one image and two lines.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| Static | Necklace on wet skin; top: "5 stars from you ⭐⭐⭐⭐⭐"; bottom: "Zero stars from the shower" | Primary text: "It's been through 400 showers and refuses to turn green." |

### Hooks

- "5 stars from you. Zero stars from your shower."
- "Zero stars from tarnish"
- "Zero stars from my sister (she wanted it first)"

### Production recipe

1. Write 10 "enemy" lines: shower, pool, chlorine, tarnish, the sister who borrows it.
2. Pair each with a real product photo.
3. Rotate weekly; the format fatigues fast.

### Existing bot prompt

```
Write 10 "5 stars from you / zero stars from ___" statics for LC: enemy, photo idea, 60-word primary text. Durability claims must match the PDP.
```

### Variants to test

- Enemy type
- Joke vs proof tone

## Reference examples

See [examples/README.md](examples/README.md) (3 posts). Top 5:

- @FedotOff90 (110L/208BM/9kV): 37 formats printing (with days active): AI podcast 280d, report card, iPhone Notes, text on skin, Reddit, cross-out, fake PDP, tier list, myth vs fact, zero sta — https://x.com/FedotOff90/status/2104949773539442831
- @cortex_adbrain (0L/0BM/0V):  — https://x.com/cortex_adbrain/status/2103883993603031429
- @Yannlce (3L/2BM/1kV): Same 40-format list (adds claymation, AI podcast). — https://x.com/Yannlce/status/2085017654364958737
