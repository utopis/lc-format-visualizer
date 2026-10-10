# BOT.md · generate a "6-second micro-demo loop with a native headline ('omg I think I finally found…')"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 5-8s seamless loop, 1080x1920), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@fablecut](https://x.com/fablecut/status/2102944927868965360) · A 5-second AI product loop: a gold watch on black marble with light gliding across it, looping without a cut. It was made from one product photo.
- Example: [@LachezarVoynov](https://x.com/LachezarVoynov/status/1977737128290189487) · This is one of the most useful AI implementations if you run Meta ads. Animating your static ads. If you have static ads that are winning inside your 
- Example: [@adamtaylorl](https://x.com/adamtaylorl/status/2092205353744130552) · 6. The "Visual Proof" POV ad A rapid-fire, close-up demonstration of the product being applied. It's built perfectly for short attention spans and sto
- Example: [@ecomrudolfs](https://x.com/ecomrudolfs/status/2102762930886336763) · Smooche 6-second foundation clip, 12 duplicates, 225 days, "omg I think I finally found a foundation that looks like second skin".
- Example: [@pranavclickks](https://x.com/pranavclickks/status/2087497730042081339) · OMG! Claude can finally watch and analyze video ads. I connected Claude to the @hookmaster_ai MCP and gave it this 20-second Brezza S-CNG ad featuring
- Example: [@akari_w0r1d](https://x.com/akari_w0r1d/status/2102937109405311256) · I created this cozy 6-second lo-fi loop animation entirely within @adobefirefly First, I made the illustration and animation, then I used the AI Music
- Example: [@hasantoxr](https://x.com/hasantoxr/status/2099897310654378092) · Every lab claims "we're the best model" and the phrase means nothing the moment you actually make something. Best at a cinematic film look isn't best 
- Example: [@vladdubchak_x](https://x.com/vladdubchak_x/status/2080614240386240932) · Your best static ads have a ceiling. Static-only means no video slots, no autoplay spots that stop the scroll. This skill removes the ceiling: drop th
- Example: [@lifemaximised](https://x.com/lifemaximised/status/2087623547288207463) · YouTube Shorts is the most underpriced ad inventory in Google right now and 90% of ecom brands STILL aren't running a single ad there The reason is al

### Live paid ads in this format (1 in [adlibrary/](adlibrary/README.md), longest-running first)

- **Muscle Mat: Dog-test visual hook (Muscle Mat, 859 days)** (859 days live): A dog flops on the mattress topper and a woman presses it; captions "what makes our campsite super comfy… 35 mm thick". DCO.

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| 0-6s | The product doing its one job, silent: a gold chain under running shower water, water beading off, then the loop restarts on the same frame | Native headline above the video: "omg I think I finally found it" |
| Variant B | A hand dipping in the sea and lifting out, chain glinting | "necklace I don't have to take off for the beach??" |
| Variant C | A ring under a tap, then a towel rub | "6 months, still gold" |

### Prompts

**Shoot**

```
iPhone 4K 60fps, macro, shower head off-frame, dark tile background, one side light for sparkle; trim so the last frame matches the first.
```

**Seedance / Kling (if real footage is not possible)**

```
5s seamless loop, macro of a thin gold chain under running water, droplets beading, dark tiles, side light
```

**Headline bank (Claude)**

```
Write 20 lowercase "found it" headlines a real person might post, under 10 words, no brand name.
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
- [ ] Files named `F98-<concept>-<variant>`; tracking tag `utm_content=F98-<concept>-<variant>`.
- [ ] Avoid: The loop must be seamless or it looks like an ad.
- [ ] Avoid: No logo or text inside the video; the headline does the talking.
- [ ] Avoid: Use real footage of the real product wherever possible.

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
5. Name every asset `F98-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F98
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

A silent 5-8 second clip of the product doing its one job (foundation blending to skin tone; a chain under a shower) with a casual, first-person headline written like a friend's caption. No story, no VO. It runs as the short, cheap counterweight to the brand's 3-10 minute films.

### Why it works

- The whole ad fits inside the time people actually watch.
- One visible proof plus one native line works muted.
- Easy to duplicate across placements and ad sets (Smooche runs 12 copies).
- It balances an account that is otherwise long-form.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0:00-0:06 | Hand runs the LC necklace under a showerhead, macro, water beading, still gold | Text: "omg I think I finally found gold I can shower in" |
| end card | Optional 1 s product + price | "Any 7 for $85" |

### Hooks

- "omg I think I finally found gold I can shower in"
- "ok this is the necklace that survived the ocean"
- "6 months, every shower, still this color"

### Production recipe

1. Shoot 10 macro clips of the single proof (shower, pool, sweat, saltwater).
2. Write 10 native one-line headlines in a friend's voice.
3. Launch 5 clip × headline pairs; duplicate the winner into 3 ad sets.

### Existing bot prompt

```
Write 10 casual first-person headlines (≤12 words, lowercase ok) for a 6-second clip of an LC necklace under a shower. They should sound like a friend's caption, not ad copy. No claims beyond "waterproof, 14K PVD".
```

### Variants to test

- Clip
- Headline voice

## Reference examples

See [examples/README.md](examples/README.md) (10 posts). Top 5:

- @ecomrudolfs (0L/0BM/0V): Smooche 6-second foundation clip, 12 duplicates, 225 days, "omg I think I finally found a foundation that looks like second skin". — https://x.com/ecomrudolfs/status/2102762930886336763
- @fablecut (0L/0BM/0V):  — https://x.com/fablecut/status/2102944927868965360
- @adamtaylorl (0L/0BM/0V):  — https://x.com/adamtaylorl/status/2092205353744130552
- @LachezarVoynov (0L/0BM/0V):  — https://x.com/LachezarVoynov/status/1977737128290189487
- @vladdubchak_x (222L/317BM/29kV): Your best static ads have a ceiling. Static-only means no video slots, no autoplay spots that stop the scroll. This skill removes the ceiling: drop the static – — https://x.com/vladdubchak_x/status/2080614240386240932
