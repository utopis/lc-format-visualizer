# BOT.md · generate a "Attraction-proof partner reaction (primal-desire hook: 'I got one to see if it actually works on my wife/him', the partner's reaction is the proof)"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 20-30s, 1080x1920, 8-12 handheld clips of 2-3s, fixed top caption), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@FedotOff90](https://x.com/FedotOff90/status/2108201405496336460) · A 32 s phone-shot montage with a fixed top caption, "🤟 I'm actually shook 😳". Shots: a man in the kitchen and a woman on the couch, a close-up nuzzle, a dropper into a glass bottle ("this is an ancient oil blend which is designed to turn women on"), "so I got one to see if it actually works on my wife", a woman fanning herself, a couple laughing at dinner with beers ("oh my gosh babe", "this thing

### Live paid ads in this format (5 in [adlibrary/](adlibrary/README.md), longest-running first)

- **HappySupp: Girlfriend-voice men's multivitamin (HappySupp)** (378 days live): A woman in a black top to camera: "Cause ain't no way he taking this without me around… this is only for you and your girl. Don't get too crazy with it. This is the men's multivitamin by HappySupp… herbal blend to support your prostate." 86 s.
- **Penrose Skin: "Wanna pull? You need this fragrance" dupe yapper (Penrose)** (89 days live): A man to camera: "Wanna pull fine shit like this, trust me you need to get this fragrance… it literally smells like [designer], the most identical fragrance… a lot more affordable… lasts a lot longer." 28 s.
- **Penrose Skin: Nightlife street-reaction montage (Penrose)** (89 days live): Night-street clips of people reacting to a man ("Before you go, what do you think of this?", "OK, that's dangerous"), then a VO: "That reaction? It's real. And it happens every time. This is Penrose Skin, a pheromone-infused body butter…" 41 s.
- **Resilia · Arterial Health Review: “WAKE UP HARD AGAIN”** (1 days live): "WAKE UP HARD AGAIN" over an aged-garlic pouch with garlic bulbs.
- **Resilia · Arterial Health Review: “Wake Up With Morning Wood”** (1 days live): "Wake Up With Morning Wood" on a red split background with the pouch.

**Do not copy (seen in these live ads):** Implied sexual-health claims for a garlic supplement are unsupported.

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| 0-2s | Mirror selfie, she clasps the LC layered necklace. Fixed top caption: "testing if he notices 😳" | "Wore this to see if he'd say anything." |
| 2-6s | Kitchen, handheld from the counter: he walks in, stops mid-sentence, double-take | Him: "Wait… is that new?" |
| 6-12s | He touches the pendant, pulls her in; she glances at camera | Her (whisper): "He NEVER notices." |
| 12-18s | Dinner, candle light on gold, he keeps looking | Caption: "day 3 he's still talking about it" |
| 18-24s | REAL LC macro: 3-layer set on a tray, splash of water | Text: "14K PVD · waterproof · any 7 for $85" |
| 24-28s | Her wink to camera | "Go test it on yours." |

### Prompts

**Script (Claude)**

```
Write 5 partner-reaction skits (20-30 s) for Louise Carter: one private-test line, partner reaction is the proof, 1-2 real product inserts, wink CTA. 6 beats each with duration, dialogue ≤8 words, fixed top caption. Flirty, not sexual; no claims that jewelry changes attraction.
```

**Casting brief (Billo / Insense)**

```
Real couple 28-45, natural chemistry, home kitchen + one dinner location, phone-shot vertical, natural light. Deliver 12 raw clips + 3 hook takes. Usage: paid social 12 months.
```

**Edit (CapCut)**

```
Fixed top caption 10% from top; cuts every 2-3s; trending sound at -18 dB under dialogue; captions burned in; 3 hook variants on one body.
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
- [ ] Files named `F109-<concept>-<variant>`; tracking tag `utm_content=F109-<concept>-<variant>`.
- [ ] Avoid: No sexual explicitness: Meta rejects implied sexual enhancement; keep it flirty.
- [ ] Avoid: No claim that the product causes attraction or arousal (especially supplements/oils).
- [ ] Avoid: AI couples fail at touch moments; cast real people.
- [ ] Avoid: Disclose dramatizations if actors are used.

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
5. Name every asset `F109-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F109
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

A 20-40 s phone-shot skit that sells **desire, not the product**. The buyer says one sentence that frames a private test: *"So I got one to see if it actually works on my wife"* / *"this fragrance helped me pull"*. What follows is a montage of **the partner's reaction**: she leans in and sniffs his neck, laughs, grabs him, drags him off the couch. The reaction is the whole proof. A fixed top caption ("I'm actually shook 😳") keeps the stakes visible. The product shows up in 1-2 quick inserts: the dropper, the jar, the bottle. It closes on a cheeky CTA: *"grab a bottle and save your relationship."*

The female-buyer mirror version: *"wore this to see if he'd notice"*, followed by his double-take, the compliment, and him asking where it's from.

### Why it works

- **Primal motive.** Fedotoff: "Men think about getting LAID 19 TIMES a day. NATURAL desire you must use with your ads if you sell to men. Keep it simple, keep it primal." Attraction and status are older than any product category.
- **Third-party proof.** The *partner's* reaction is more believable than the buyer's own claim, which fits his "testimonials beat claims" rule: someone else is reacting.
- **A curiosity test format.** "To see if it actually works" is an experiment, and people watch experiments to the end.
- **Comment bait.** "Need this", "sending to my husband", "does it work tho?" all push distribution.
- **Penrose runs it at volume.** The compliment-magnet skits ("This fragrance helped me pull", "Do you smell that?") are 9 of the 10 ads in its 100-ad board preview, all 89 days live and still running.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0-2s | Her mirror selfie putting on the LC layered necklace; top caption "testing if he notices 😳" | "Wore this to see if he'd say anything." |
| 2-6s | Kitchen: he walks in, stops mid-sentence, double-take | (him) "Wait… is that new?" |
| 6-12s | He touches the pendant, pulls her in | (her, whisper to camera) "He NEVER notices." |
| 12-18s | Dinner out: candle light on the gold, he can't stop looking | caption: "day 3 he's still talking about it" |
| 18-24s | Real LC product insert: the 3-layer set on a tray, waterproof splash | "14K PVD, waterproof, any 7 for $85" |
| 24-28s | Her wink to camera | "Go test it on yours." |

### Hooks

- "I got one to see if it actually works on my wife."
- "This [product] helped me pull, no joke."
- "I stopped buying $400 [premium thing]… and started [cheap thing]."
- "Wore this to see if he'd notice."
- "My husband asked where I got this 3 times in one night."

### Production recipe

1. **Cast a real couple** (creator couples on Billo / Insense / TikTok Creator Marketplace) or a single creator plus a friend. AI couples look fake at the touch moments, so avoid them.
2. **Script 6 beats:** private test line → partner notices → partner escalates (touch, compliment) → caption timestamp ("day 3") → product insert → wink CTA.
3. **Shoot vertical on a phone,** natural light, 8-12 clips of 2-3 s; keep the fixed top caption.
4. **Product inserts must be real** LC macro footage.
5. **Edit:** fast cuts, trending sound at low volume, burned-in captions. Make 3 hooks × 1 body.

### Existing bot prompt

```
Write 5 'attraction-proof' partner-reaction skits (20-30 s) for Louise Carter. The buyer frames a private test in one line ('wore this to see if he'd notice' / male gifter: 'got her this to see if she'd stop stealing mine'); the partner's reaction is the proof (double-take, compliment, asks where it's from); product appears in 1-2 real inserts; wink CTA with any 7 for $85. For each: fixed top caption, 6 beats with duration, dialogue ≤8 words, casting note. Tasteful, no sexual explicitness, no claims that jewelry changes attraction.
```

### Variants to test

- Buyer gender (her test vs his gift)
- Real couple vs creator plus friend
- Caption "I'm actually shook" vs "testing if he notices"
- Length 20 s vs 35 s

## Reference examples

See [examples/README.md](examples/README.md) (1 posts). Top 5:

- @FedotOff90 (27L/27BM/4kV): Men think about getting LAID 19 TIMES a day. NATURAL fucking desire you must use with your ads if you sell to men. Keep it simple, keep it primal, and print mfe — https://x.com/FedotOff90/status/2108201405496336460
