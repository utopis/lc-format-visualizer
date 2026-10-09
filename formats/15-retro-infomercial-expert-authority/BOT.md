# BOT.md · generate a "Retro TV infomercial / expert authority (1987 daytime-TV look, "professor interview")"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 30-60s, 1080x1920 with a 4:3 picture inside, VHS look), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@tryatria_AI](https://x.com/tryatria_AI/status/2105329322496016777) · A retro late-80s TV infomercial: a big-haired presenter in a pink suit, a "70% WATER" starburst, a dermatology close-up, the product bottle (Magic serum) on a set, and a collage of archive-looking footage. The lo-fi era styling is the hook.
- Example: [@CEO_Vlad](https://x.com/CEO_Vlad/status/2088597593949692087) · AI pharmacist ad format: $5, 4 minutes (authority-figure risk).
- Example: [@TomReichertWA](https://x.com/TomReichertWA/status/2085467482224247014) · @CocaCola Quick jump to tick tock to dub in music to my Grok made clip now I made you a retro ad in a minute 😎 @nikitabier @X @elonmusk Hot weather gr
- Example: [@HenryCrochemore](https://x.com/HenryCrochemore/status/2092191032645431595) · this static is weird enough to make you stop poo-pourri took a product nobody wants to think about and wrapped it in a polished retro ad the contrast 

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| 0-3s | 4:3 frame, VHS grain, presenter in a power blazer on a pastel studio set | "Ladies, are you STILL taking off your jewelry to shower?" |
| 3-15s | Demo on a turntable, chunky 80s graphics ("WATERPROOF!" starburst) | Exaggerated infomercial delivery |
| 15-30s | Fake-retro "testimonial" lower-thirds (clearly comedic), product close-ups | Real facts, retro delivery |
| End | "CALL NOW" parody card that becomes a modern URL | Offer + AI label |

### Prompts

**Veo 3 / Kling**

```
1987 daytime television infomercial, VHS footage, 4:3, a woman presenter with big hair in a pink blazer on a pastel studio set holding a gold necklace, enthusiastic, scan lines, color bleed, 8s
```

**Post**

```
CapCut: add "VHS" effect, 4:3 crop inside 9:16, date stamp, mono audio with slight hiss.
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
- [ ] Files named `F15-<concept>-<variant>`; tracking tag `utm_content=F15-<concept>-<variant>`.
- [ ] Avoid: A fake "doctor" or fake credentials is not OK even as parody.
- [ ] Avoid: The retro look must not hide the real product; show it clean in the last 5s.

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
5. Name every asset `F15-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F15
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

VHS grain, 4:3 framing, serious host in a pink blazer, studio set, big claims overlay ("550,000+ women"), phone number style lower-third. "It doesn't look like a polished DTC ad" ([@tryatria_AI](https://x.com/tryatria_AI/status/2105329322496016777)).

## Reference examples

See [examples/README.md](examples/README.md) (5 posts). Top 5:

- @tryatria_AI (118L/211BM/8kV): Retro 1987-TV dermatologist ad: un-polished authority format stands out. — https://x.com/tryatria_AI/status/2105329322496016777
- @CEO_Vlad (78L/117BM/7kV): AI pharmacist ad format: $5, 4 minutes (authority-figure risk). — https://x.com/CEO_Vlad/status/2088597593949692087
- @antonioventre_ (47L/49BM/3kV): Supplement 3.17x ROAS: 1 CBO/product, 1 ad set/persona; creatives = Suno AI ads, professor interview... — https://x.com/antonioventre_/status/2108228200421576872
- @HenryCrochemore (5L/1BM/394V): this static is weird enough to make you stop poo-pourri took a product nobody wants to think about and wrapped it in a polished retro ad the contrast is what ma — https://x.com/HenryCrochemore/status/2092191032645431595
- @TomReichertWA (3L/0BM/90V): @CocaCola Quick jump to tick tock to dub in music to my Grok made clip now I made you a retro ad in a minute 😎 @nikitabier @X @elonmusk Hot weather grate soft d — https://x.com/TomReichertWA/status/2085467482224247014
