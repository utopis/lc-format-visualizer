# BOT.md · generate a "Product placement inside short-drama channels (brand written into a micro-drama that already has the audience)"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: Sponsored episode in the channel's native length (60s-3 min) + a 30s whitelisted cut), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@cesaralvarezll](https://x.com/cesaralvarezll/status/2108488444414394811) · A GoodShort clip shown in a phone frame next to the App Store overlay "App Stats: 2m downloads & $9m revenue last month" (GoodShort - Short Dramas Hub). In the drama, at a red-carpet party, a woman sneers at a birthday gift bottle of wine: "What brand is this... don't tell me it's some cheap knockoff... Are you trying to poison Dad with this no-name trash?" The clip is marked "Paid partnership". T
- Example: [@MogiOTTSolution](https://x.com/MogiOTTSolution/status/2066387745732465148) · Brands don't need more ads. They need better stories. 🎬 Lacto Calamine generated 10M organic views in 5 days through a micro-drama. 🎬 Crocs achieved 1
- Example: [@SixthTone](https://x.com/SixthTone/status/2082027321490329688) · AI-generated stars are attracting real fans. After the AI micro-drama “The Laid-Off Girl” surpassed 200 million views, its female lead launched a Douy
- Example: [@AshleyDudarenok](https://x.com/AshleyDudarenok/status/2095338838394654999) · She has NO eyes, but sold contact lenses. AI micro-drama star Fang Taozi accrued 400k followers in a month, out-charging human influencers with millio

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| Setup | Lead touches her necklace when nervous (establish the habit in the first scene) | — |
| Conflict | Antagonist line about the necklace | "That thing will be green by the wedding." |
| Proof scene | Rain / pool / tears; necklace visibly fine | — |
| Hero close-up | 1-2s macro of clasp/pendant, real product | On-screen tag: "Louise Carter · 14K PVD" |
| Sponsored end card | Paid-partnership label + shop link (whitelisted version) | "Her necklace: any 7 for $85" |

### Prompts

**Channel shortlist**

```
Search TikTok and YouTube for "micro drama", "short drama", "AI drama" with women 25-55 audiences; log avg views (last 10 posts), comment quality, audience geo, posting cadence, and whether they already do brand integrations.
```

**Outreach DM (draft only; send after approval)**

```
Draft: "Love [series]. We're Louise Carter (waterproof 14K PVD jewelry). Would you write our necklace into an upcoming episode as the lead's never-take-it-off piece? Flat fee + 30-day whitelisting + affiliate code. Can share a 1-page brief."
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
- [ ] Files named `F107-<concept>-<variant>`; tracking tag `utm_content=F107-<concept>-<variant>`.
- [ ] Avoid: Get whitelisting rights in writing before paying.
- [ ] Avoid: Approve the script for claims; creators improvise.
- [ ] Avoid: Paid-partnership label on every post.

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
5. Name every asset `F107-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F107
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

Instead of making a drama ad, the brand **buys its way into a drama that already has millions of viewers**: a short-drama channel or app (or an AI micro-drama creator) writes the product into an episode (the necklace is the heirloom, the ring is the clue, the skincare is the glow-up), then the brand whitelists that episode as a Spark/Partnership ad. The drama app gets paid twice: users for free from viral clips, and brands for placement.

**The verified example (hero).** The @cesaralvarezll post shows a **GoodShort (Short Dramas Hub)** clip next to an App Store overlay: "2m downloads & $9m revenue last month". The clip is labelled **"Paid partnership"**. At a red-carpet party, a woman mocks a birthday gift bottle of wine: "What brand is this... don't tell me it's some cheap knockoff... Are you trying to poison Dad with this no-name trash?" The sponsor's product is written in as the *underdog object*. The villain insults it, and the story is built so that it gets vindicated later. That is the template for LC: the product is not shown being praised, it is shown being *underestimated*. The dupe angle ("it's not the $90 brand... is it?") fits this perfectly.

### Why it works

- The audience is pre-built and already watching for the story; the product rides the plot.
- Placement inside entertainment avoids the 'ad' pattern women skip (frankyecom).
- Whitelisting the episode gives paid reach with the creator's handle and social proof.
- Drama characters build parasocial trust (an AI micro-drama star gained 370K followers after a 200M-view series).

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| Episode beat 1 | Lead touches her necklace when nervous (established habit) | — |
| Beat 2 | Antagonist: "That cheap thing will turn green by the wedding." | — |
| Beat 3 | Rain / pool / tears scene; necklace visibly fine | — |
| Beat 4 | Close-up of the clasp/branding for 1 s | On-screen tag: "Louise Carter, 14K PVD" |
| End card (sponsored version only) | Paid-partnership label + shop link | "Her necklace: any 7 for $85" |

### Hooks

- (The channel's own hook; don't rewrite it)
- "Episode 12: the necklace she never takes off"
- "Her mother's necklace is the only clue…"

### Production recipe

1. **Find channels:** search TikTok/YouTube for 'micro drama', 'short drama', 'AI drama' channels with women 25-55 audiences; check average views, comments and audience geo.
2. **Brief:** product role in the plot (habit, heirloom, clue), one hero close-up (1-2 s), facts allowed (PDP only), no competitor jabs.
3. **Deal:** flat fee + whitelisting rights (30-60 days) + optional affiliate code.
4. **Launch:** creator posts organically with a paid-partnership label; LC runs the episode as Spark/Partnership ads to lookalikes.
5. **Measure** with a unique code + UTM per channel.

### Existing bot prompt

```
Write a sponsorship brief for a micro-drama channel to integrate Louise Carter into one episode. Include: the plot role options (heirloom, clue, habit, glow-up), the one required close-up, allowed facts {{PDP_FACTS}}, banned claims, disclosure requirements, whitelisting terms, and 3 example scene beats in the channel's style.
```

### Variants to test

- Flat fee vs affiliate
- Organic only vs whitelisted
- Integration depth (prop vs plot point)

## Reference examples

See [examples/README.md](examples/README.md) (4 posts). Top 5:

- @Storyboard18_ (2L/1BM/164V): The @Meta -@_KukuTVOfficial Micro Drama Playbook finds the category growing rapidly, with 65% of viewers exposed to the format within the past year and audience — https://x.com/Storyboard18_/status/2105194685224702410
- @AshleyDudarenok (0L/0BM/229V): She has NO eyes, but sold contact lenses. AI micro-drama star Fang Taozi accrued 400k followers in a month, out-charging human influencers with millions of fans — https://x.com/AshleyDudarenok/status/2095338838394654999
- @MogiOTTSolution (0L/0BM/8V): Brands don't need more ads. They need better stories. 🎬 Lacto Calamine generated 10M organic views in 5 days through a micro-drama. 🎬 Crocs achieved 10M+ views  — https://x.com/MogiOTTSolution/status/2066387745732465148
- @cesaralvarezll (0L/0BM/0V):  — https://x.com/cesaralvarezll/status/2108488444414394811
