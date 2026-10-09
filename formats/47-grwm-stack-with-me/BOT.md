# BOT.md · generate a "GRWM / 'stack with me'"

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

- **Main example**: [@ugcAshleyRJ](https://x.com/ugcAshleyRJ/status/2067636022251290725) · The same 0.5x ultra-wide POV technique used as a get-ready / stack-with-me sequence: a wide shot of the creator, close-ups of the items laid out, the final look.
- Example: [@wayne_forge](https://x.com/wayne_forge/status/2087161700298473607) · TWO AI TWINS "GET READY" IN THE SAME CLOSET — AND THE PAGE BEHIND THEM CLEARS $11,400 A MONTH. Same face, same hair, same dressing room. One in a pink
- Example: [@Atlas8a](https://x.com/Atlas8a/status/2080302219199385799) · A 26-YEAR-OLD IN TEXAS BUILT A TRY-ON HAUL INFLUENCER WHO DOESN'T EXIST. ONE VIDEO HIT 5.8 MILLION VIEWS 👗 Try-on hauls used to be a job. Buy the clot
- Example: [@moneytokwitbuki](https://x.com/moneytokwitbuki/status/2084621955752145291) · Brand Study: rhode rhode's primary target audience is Gen Z and Millennials. Before the official product launch, the founder built anticipation by con

### Live paid ads in this format (1 in [adlibrary/](adlibrary/README.md), longest-running first)

- **Smriti Kochar: Nutritionist 3-product stack explainer (Hinglish)** (301 days live): Smriti Kochar (nutritionist) talks to camera, cut with gym b-roll and belly close-up: 'Major pain point for men and women is belly fat…' then presents 3 products (digestion, gallbladder, cortisol) as a routine, 'try all three for a month'.

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| 0-3s | Creator at a mirror, bare neck and wrist | "Stack with me for a beach day." |
| 3-20s | One piece at a time: chain, pendant, second chain, bracelets, ring | Name each piece as it goes on |
| 20-35s | Turn to camera, full stack | "All waterproof, so I don't take it off for the sea." |
| 35-45s | Quick beach clip wearing it | - |
| End | Product list on screen | "7 pieces, $85." |

### Prompts

**Shoot**

```
Mirror or front camera at chest height, ring light at 45°, one take per piece.
```

**Script**

```
Write 5 "stack with me" themes (beach, wedding guest, office, gym, date) with 7 pieces each from the catalogue.
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
- [ ] Files named `F47-<concept>-<variant>`; tracking tag `utm_content=F47-<concept>-<variant>`.
- [ ] Avoid: Name pieces so viewers can find them.
- [ ] Avoid: Show the full stack long enough to screenshot.
- [ ] Avoid: Keep it under 60s.

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
5. Name every asset `F47-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F47
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

Creator gets ready (outfit → makeup → jewelry) or builds a stack piece by piece while talking; the jewelry is the payoff of the routine.

### Why it works

- GRWM is a default watch habit; jewelry as the "finishing touch" is natural.
- "Stack with me" demonstrates the bundle offer visually.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0-2s | Mirror, bare neck | "GRWM for a wedding — jewelry edition" |
| 2-15s | Layering 1→7 pieces | Chatty VO |
| 15-20s | Full look | "any 7 for $85" |

### Hooks

- "Building a 7-piece stack with me"
- "GRWM: jewelry I never take off"
- "Stack check"

### Production recipe

1. Creator briefs for swarm (F43).
2. Shoot mirror + close-ups.

### Existing bot prompt

```
Write 6 GRWM/stack-with-me scripts (25s) for occasions {{OCCASIONS}}; each builds a 7-piece stack from {{SKUS}}.
```

### Variants to test

- Occasion
- Creator age 25-35 vs 40-55

## Reference examples

See [examples/README.md](examples/README.md) (8 posts). Top 5:

- @Ecombos_Ai (28L/26BM/2kV): 10 AI UGC styles: talking-head testimonial, product-in-hand, first-try reaction, fake podcast, street interview, comment reply, unboxing, DITL/GRWM, before/afte — https://x.com/Ecombos_Ai/status/2103180929057407425
- @rirahcreates (12L/17BM/1kV): 20 UGC types: talking head, review, unboxing, testimonial, demo, problem/solution, before/after, GRWM, DITL, voiceover, routine, how-to, FAQ, 3 reasons why, POV — https://x.com/rirahcreates/status/2089827933561016787
- @ugcAshleyRJ (13L/5BM/534V): The 0.5x ultra-wide POV filming technique for demos, GRWM and day-in-the-life — immersive, native. — https://x.com/ugcAshleyRJ/status/2067636022251290725
- @0xJeyx (15L/3BM/889V): Generate the same product as every format at once (street quiz, review, GRWM, DITL) and let the feed pick — example: "$50 street quiz" video. — https://x.com/0xJeyx/status/2063387846803673406
- @wayne_forge (2L/1BM/118V): TWO AI TWINS "GET READY" IN THE SAME CLOSET — AND THE PAGE BEHIND THEM CLEARS $11,400 A MONTH. Same face, same hair, same dressing room. One in a pink textured  — https://x.com/wayne_forge/status/2087161700298473607
