# BOT.md · generate a "In-store scan → score → reaction (scan a product on the shelf with the app, react to the score)"

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
5. Name every asset `F101-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F101
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

The creator walks into a store everyone knows (Sephora, DM, BIPA, Target), picks up a product people already own, **scans it with the app**, and the video holds on the score loading. Then a real reaction ("no way my moisturiser is a 23") and the next product. AI or creator voiceover: *"I went to BIPA to see if this product is actually worth buying…"*

The suspense is the score. Every shelf is a new video, and viewers stay because they want to know if *their* product passes.

### Why it works

- Recognisable products = instant relevance ("I own that").
- A number on screen is a mini cliffhanger; viewers wait for the reveal.
- The app's core feature IS the content (screen-recordable reveal = free ads, the same reason Cal AI / Umax spread).
- Endless supply: one store trip = weeks of content (@cicerougc).

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0-2s | Walking into a jewelry aisle / department store accessories wall (no store logo close-up) | VO: "I went to the mall to see if these 'gold' necklaces are actually gold…" |
| 2-5s | Hand picks a generic gold-tone chain; label close-up "gold tone" | Caption: "$29 'gold' necklace" |
| 5-8s | Phone screen: LC "Gold Check" quiz or a printed label checklist; score animates 0 → 18/100 | SFX: tick-tick-ding |
| 8-10s | Creator face: wince | "…18." |
| 10-16s | Same check on her LC necklace (PVD 14K, waterproof) | Score 92/100 · "this one I shower in" |
| 16-20s | End card | "How does yours score? · any 7 for $85" |

### Hooks

- "I scanned every 'gold' necklace in the mall. Only one passed."
- "Is your $30 necklace actually gold? I checked."
- "Rating my jewelry box from 0-100 (it's bad)"
- "I went to [store] to see if this is worth buying…"

### Production recipe

1. **Score tool:** LC has no scanner app, so build a 5-question "Gold Check" (tone vs plated vs PVD vs solid; water-safe; nickel-free; warranty; price per wear) in a quiz tool (F61) or a simple scoring card. The score must come from real criteria, published on the PDP/FAQ.
2. **Store run:** film in public aisles only where filming is allowed; never show a brand name or logo of a competitor product.
3. **Screen record** the quiz on the phone (iOS screen recording) and composite it in CapCut picture-in-picture.
4. **Voiceover:** creator or ElevenLabs voice (disclosed); 8-12 words max per line.
5. **Edit:** 15-20 s, score reveal at 5-8 s, LC comparison at 10-16 s.

### Existing bot prompt

```
Design a transparent 0-100 'Gold Check' scoring rubric for gold-coloured jewelry using only verifiable criteria (material label, plating type, water exposure guidance, nickel content, warranty). Then write 12 store-aisle video scripts (15-20 s) where a creator scores a generic, unbranded piece and then her Louise Carter piece. No competitor names, logos or disparaging claims; every LC score point must map to {{PDP_FACTS}}.
```

### Variants to test

- Store vs home jewelry box
- Real quiz screen vs printed score card
- AI voice vs creator voice
- Score reveal speed

## Reference examples

See [examples/README.md](examples/README.md) (3 posts). Top 5:

- @danielhangan_ (131L/233BM/20kV): $0-$10K MRR. 1 ad. $6K free TikTok credits. 0 UGC creators. the lazy app playbook: 1/ copy a proven app model (Cal AI, UMax, Pray Screen) 2/ sell to a core desi — https://x.com/danielhangan_/status/2039655379185873307
- @consumerxai (3L/1BM/293V): 121M views lost to 9.6M on the number that matters more for engagement saves -&gt; a save means "i'm going to do this later" and has high intent -&gt; calorie a — https://x.com/consumerxai/status/2107834606368293123
- @cicerougc (0L/1BM/165V): 100k+ views with a skincare app using the easiest content format I've found. The formula: 1. Go to a supermarket (BIPA, DM, Sephora, etc.) 2. Pick up a skincare — https://x.com/cicerougc/status/2075757653309919555
