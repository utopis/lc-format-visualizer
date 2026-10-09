# BOT.md · generate a "6-second micro-demo loop with a native headline ('omg I think I finally found…')"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

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

See [examples/README.md](examples/README.md) (7 posts). Top 5:

- @ecomrudolfs (0L/0BM/0V): Smooche 6-second foundation clip, 12 duplicates, 225 days, "omg I think I finally found a foundation that looks like second skin". — https://x.com/ecomrudolfs/status/2102762930886336763
- @vladdubchak_x (222L/317BM/29kV): Your best static ads have a ceiling. Static-only means no video slots, no autoplay spots that stop the scroll. This skill removes the ceiling: drop the static – — https://x.com/vladdubchak_x/status/2080614240386240932
- @lifemaximised (8L/12BM/929V): YouTube Shorts is the most underpriced ad inventory in Google right now and 90% of ecom brands STILL aren't running a single ad there The reason is always the s — https://x.com/lifemaximised/status/2087623547288207463
- @hasantoxr (9L/5BM/10kV): Every lab claims "we're the best model" and the phrase means nothing the moment you actually make something. Best at a cinematic film look isn't best at a 6-sec — https://x.com/hasantoxr/status/2099897310654378092
- @akari_w0r1d (23L/2BM/545V): I created this cozy 6-second lo-fi loop animation entirely within @adobefirefly First, I made the illustration and animation, then I used the AI Music Generator — https://x.com/akari_w0r1d/status/2102937109405311256
