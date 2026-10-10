# BOT.md · generate a "Emotional life-moment story with the product as the hidden mechanism (crying-bride 'we gave every guest a camera')"

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

- **Main example**: [@stat_biz](https://x.com/stat_biz/status/2100293137709269251) · A real wedding moment (a crying bride, a flower) as the hook, then a phone showing the app (Once camera) collecting guests' photos, ending on a QR code and the app name. The emotion comes first and the mechanism is revealed after.
- Example: [@ByMorola](https://x.com/ByMorola/status/1752970187198865515) · We love reviews. We customized a bracelet for a client and frame 1 was her reaction. Customized bracelet- N11000 Adjustable customized bracelets for w
- Example: [@Strawaubreyyy](https://x.com/Strawaubreyyy/status/2006263964175622457) · Napaiyak ko sya nung Shady brunch 🥹 I gave her a locket necklace na may picture ng mom nya so she can carry it with her everywhere she goes🥹 & I told 
- Example: [@eva_jiang47397](https://x.com/eva_jiang47397/status/1824386160946274779) · I bought my American mother-in-law a Chinese bracelet on Independence Day, and she was shocked.but she liked the necklace I gave her very much and hop
- Example: [@sammgrowth](https://x.com/sammgrowth/status/2080991187133943894) · i should never be sharing this but fuck it a wedding app is running the craziest ai ugc play of 2026 and nobody has clocked it 11.8M views on one tikt
- Example: [@adamtaylorl](https://x.com/adamtaylorl/status/2090038014353277073) · 1. The Emotional Redemption ad "We thought it was time to say goodbye for good" The discovery moment is a Reddit thread on screen.
- Example: [@Pavol_Repisky](https://x.com/Pavol_Repisky/status/2078415656895082582) · Disposable-camera app $20K/mo in 83 days; best TikTok 10M views/900K likes = AI bride crying at "her" wedding.

### Live paid ads in this format (3 in [adlibrary/](adlibrary/README.md), longest-running first)

- **Aucier: AI story ad: sister's autistic son's meltdowns (sensory product)** (447 days live): "My autistic son's meltdowns were destroying our family until I found this…" A first-person family story told over AI-generated scenes. 108 s.
- **Pure Rhythm: Menopause reframe podcast (hair / energy)** (326 days live): "When your period stops, your brain literally cuts off the signal to your ovaries… that's the moment you need to say, no, I'm not going to waste away at 50. I still have 30 years ahead." 101 s.
- **Mariella Gut Health Expert: "Gross embarrassing story time" gut yapper (Mariella Gut Health Expert)** (320 days live): A creator on a couch: "Alright, gross embarrassing story time! A few months ago I started noticing that my smells were… terrible… I was feeling bloated, icky… I consulted a few physicians, they said something was wrong with my gut health…" 105 s.

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| 0-5s | Wedding morning, bride's mum crying quietly | Caption: "We gave her mum's old necklace a second life." |
| 5-20s | Flashback photos of the mum wearing a necklace; it had turned green | Soft VO from the daughter |
| 20-35s | Gift moment: a small box, the new necklace | "So she can wear it every day now. Even in the sea." |
| 35-45s | Mum wearing it at the reception, dancing | - |
| End | Brand card, soft offer | - |

### Prompts

**Casting**

```
Use a real customer story (with consent) or label it as a dramatisation.
```

**Shoot**

```
Warm grade, handheld, natural sound; music swells only at the gift moment.
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
- [ ] Files named `F55-<concept>-<variant>`; tracking tag `utm_content=F55-<concept>-<variant>`.
- [ ] Avoid: Label dramatisations.
- [ ] Avoid: Don't exploit grief; keep it warm, not sad.
- [ ] Avoid: The product must be the hidden mechanism, not the hero of every shot.

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
5. Name every asset `F55-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F55
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

A peak-emotion moment (bride in tears at her reception, mom at a birthday, best friend at a graduation) + an on-screen line that reveals an unusual choice — "We gave every guest a camera instead of hiring more photographers…" / "Everyone says no phones at weddings… but I did the opposite" — then the product is shown as the mechanism behind the moment (QR on the place card → app). The ad is the story; the product is how it happened.

### Why it works

- Emotion first, product second: viewers watch a wedding, not an ad (@traqscales: "doesn't need to look like an ad").
- The contrarian line ("instead of", "I did the opposite") creates curiosity about the mechanism.
- Weddings/milestones are universally shareable; brides and bridesmaids save and send.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0-3s | Real bride, tearful smile, at reception (consented footage); caption "We gave every bridesmaid a necklace instead of matching dresses…" | Ambient music |
| 3-8s | Close-up: bridesmaids' hands, each wearing a different LC piece | — |
| 8-14s | Flashback: the gift boxes on the place settings, handwritten notes | — |
| 14-20s | Group jumps in the pool after the reception — necklaces still on | Caption: "…they swam in them that night" |
| 20-25s | "24 hours later" text from a bridesmaid (real, consented) | — |

### Hooks

- "We gave every bridesmaid a necklace instead of matching dresses…"
- "Everyone said skip the favors… I did the opposite"
- "My mom cried when she opened this (she's never cried at a gift)"
- "I proposed with a $12 ring on purpose…" (only if real story)
- "We swam at the reception. Nobody took their jewelry off."

### Production recipe

1. Source REAL moments: ask LC customers who bought bridesmaid/wedding/anniversary gifts for consented footage (Omnisend post-purchase flow; offer store credit, disclose).
2. Script only the on-screen line; the footage is real.
3. If testing AI versions (F53 lab), label as AI and never present the AI person as a real customer/bride; use only for angle discovery, then remake with real people.
4. Cut 20-30s; caption-driven; trending emotional audio (licensed for paid).

### Existing bot prompt

```
From these customer wedding/milestone stories {{STORIES}}, write 10 on-screen opener lines in the pattern "[We/I] [did unusual thing with LC] instead of [expected thing]…" and a 6-shot sequence for each using only footage the customer can supply. Flag anything that would require staging.
```

### Variants to test

- Occasion (wedding/birthday/anniversary/graduation)
- Bride POV vs guest POV
- Real vs AI-labelled test

## Reference examples

See [examples/README.md](examples/README.md) (8 posts). Top 5:

- @traqscales (22L/27BM/1kV): Once app: 22.5M views from 2 AI UGC creators (one 13M, 9 >100K) — AI bride crying at her reception, "we gave every guest a camera instead of hiring more photogr — https://x.com/traqscales/status/2108113354178932920
- @stat_biz (6L/1BM/582V): Crying-face hooks go viral; Once's bride is clearly AI ("getting married" for 6+ months) — authenticity caveat. — https://x.com/stat_biz/status/2100293137709269251
- @Pavol_Repisky (0L/0BM/130V): Disposable-camera app $20K/mo in 83 days; best TikTok 10M views/900K likes = AI bride crying at "her" wedding. — https://x.com/Pavol_Repisky/status/2078415656895082582
- @sammgrowth (173L/231BM/22kV): i should never be sharing this but fuck it a wedding app is running the craziest ai ugc play of 2026 and nobody has clocked it 11.8M views on one tiktok. the ac — https://x.com/sammgrowth/status/2080991187133943894
- @mattgittleson (0L/0BM/0V):  — https://x.com/mattgittleson/status/2107530746923823444
