# BOT.md · generate a "Short AI revenge-drama ad (25-60 s: betrayal open, fast cuts, twist, product is how she gets even)"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 25-30s (plus a 45-60s cut), 1080x1920, 12-16 shots of 1.5-2.5s), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@0xROAS](https://x.com/0xROAS/status/2107188290264740348) · A 25-second AI drama (Seedance 2.5). A woman calls up the stairs: "Dad, tea's on the table, it's getting cold." Dad struggles on the stairs: "40 years I've done these stairs... I'm all right." Close-ups: "You're not all right, Dad. It's been like this since Christmas. Why didn't you say something?" "Didn't want to be the old bloke who can't do the stairs." She kneels beside him on the stairs, with
- Example: [@david_attisaas](https://x.com/david_attisaas/status/2108195582607081720) · I'm running short drama ads for a few apps right now, and every one of them started as a copy of something a dropshipper ran first. I went looking aft
- Example: [@ViralOps_](https://x.com/ViralOps_/status/2108255353016406383) · Koriderm is absolutely CRUSHING with these DRAMA ads rn. they're literally making mini movies just to sell skincare products 😭 and i think this could 
- Example: [@zedmadeit](https://x.com/zedmadeit/status/2102176819709673703) · heres how to make ai drama ads for your brand ai dramas are the new trend and theyre great for engagement but you want the right kind the kind that ac
- Example: [@JUSTCHAEL_](https://x.com/JUSTCHAEL_/status/2098373776828256595) · Enjoy this short drama ad I created for Outlash, featuring their Curt Purse. @outlashbrand AI can create story-driven ads, not just pretty visuals. If
- Example: [@frankyecom](https://x.com/frankyecom/status/2106833649970684195) · Women want shows: characters, drama, payoff; build entertainment first, slot product in.

### Live paid ads in this format (5 in [adlibrary/](adlibrary/README.md), longest-running first)

- **Smooche · Smooche: “I'm about to walk into brunch to meet my girlfriend that I was with to…”** (41 days live): Opens: “I'm about to walk into brunch to meet my girlfriend that I was with to figure out who tried to draw a ying yang on my forehead and guess what? I just saw my ex- boyfriend of 15 years and it's perfect…”
- **Smooche · Smooche: “Okay, this is a good one. Emergency because I just pulled up to the…”** (37 days live): Opens: “Okay, this is a good one. Emergency because I just pulled up to the gym.”
- **Smooche · Cosmetic Times: “I thought menopause ruined my face. My ex has been used it as his…”** (36 days live): Opens: “I thought menopause ruined my face. My ex has been used it as his excuse to leave me.”
- **Smooche · Cosmetic Times: “My ex has been filed for divorce eight months after my menopause…”** (36 days live): Opens: “My ex has been filed for divorce eight months after my menopause started. He told our daughter he couldn't be attracted to someone whose face looked that ruined and ugly.”
- **Smooche · Cosmetic Times: “My ex has been told me I'd aged 10 years in six months. And for a…”** (36 days live): Opens: “My ex has been told me I'd aged 10 years in six months. And for a while, I actually believed him.”

**Do not copy (seen in these live ads):** These are AI-acted first-person stories posted from fake narrator pages. Label fiction as fiction.

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| 0-2s | Engagement party, medium close-up. SIL flicks the bride's necklace with one finger. | SIL: "Cute. Did it come with the cake?" + crowd laugh |
| 2-4s | Bride's face, push-in; party sound drops out | Low bass sting |
| 4-6s | Title card over black | "3 weeks later" |
| 6-9s | Pool: SIL climbs out; close-up of her wrist, bracelet dull/green-tinged | — |
| 9-13s | Bride swims, surfaces, necklace bright gold in sunlight (REAL LC footage for the macro) | Music lifts |
| 13-18s | Bachelorette brunch; SIL hides her wrist under the table | Friend: "Wait, is that the same necklace?" |
| 18-21s | Bride, casual | "Mine? I shower in it." |
| 21-25s | Hands-only LC box, 14K PVD card | Text: "14K PVD · waterproof · any 7 for $85" |
| 25-28s | SIL alone, typing "louise carter" into search | Beat; cut to black |

### Prompts

**Story (Claude)**

```
Write a 28-second revenge drama for Louise Carter. 0-2s humiliation tied to jewelry; escalate with cuts every 1.5-2.5s; twist = water/sweat ruins the antagonist's piece, LC survives; real product beat at 21-25s; payoff at 25-28s. Give 14 shots: duration, camera, action, dialogue ≤8 words, on-screen text.
```

**Character lock (image model)**

```
Photoreal, 9:16, "woman, 32, warm brown hair in a low bun, soft satin green dress, natural makeup, engagement party in a garden with string lights, shallow depth of field, Canon R5 50mm f/1.8 look". Save as reference; reuse the same seed/reference for every shot.
```

**Shot prompt (Seedance 2.5 / Kling / Veo)**

```
"[Reference: Character A] stands at a garden party at dusk, a second woman flicks her necklace dismissively, guests laugh in soft focus, handheld, 2 seconds, natural skin texture, no text." Generate 3 takes per shot, keep the one with stable hands and face.
```

**Voice + lip-sync**

```
ElevenLabs voices per character; lines ≤8 words; lip-sync only close-ups (Arcads / HeyGen); everything else plays under music.
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
- [ ] Files named `F105-<concept>-<variant>`; tracking tag `utm_content=F105-<concept>-<variant>`.
- [ ] Avoid: Never AI-generate the jewelry close-ups: shoot the real product.
- [ ] Avoid: Product beat must land before ~70% of runtime or most viewers never see it.
- [ ] Avoid: Keep the antagonist petty, not cruel; abuse/violence gets ads rejected.
- [ ] Avoid: Label AI content per platform rules.

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
5. Name every asset `F105-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F105
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

The short cousin of F91. A 25-60 second AI-generated (or acted) mini-movie built like a ReelShort clip: **0-3 s betrayal or humiliation** ("my sister-in-law laughed at my jewelry in front of everyone"), **fast cuts every 1-2 s**, a **twist**, and the **product is the reason she wins**. No narrator selling; the product is a plot device. It ends on the satisfying payoff, not a cliffhanger (that is F106).

### Why it works

- Micro-drama viewers (ReelShort, DramaBox) are already trained on betrayal → twist → revenge; boomers and women 35+ binge it and rarely notice it is AI (@david_attisaas).
- It is entertainment first, so CPMs drop and people stay (frankyecom: "stop interrupting the show, make the ad the show").
- 25 s keeps the product inside the retention window; F91 long melodramas lose 90-95% before the product (@TheIvanKreimer).
- Revenge gives the product an emotional job, not just a feature.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0-2s | Engagement party, close-up: SIL flicks bride-to-be's necklace | SIL: "Cute. Did it come with the cake?" (laughter) |
| 2-5s | Bride's face, humiliated; fast push-in | Music sting |
| 5-9s | Flash: SIL at the pool, her 'designer' bracelet turning her wrist green | Text: "3 weeks later" |
| 9-14s | Bride swims laps wearing her LC necklace; surfaces, still bright gold | — |
| 14-20s | SIL at the bachelorette, hiding her wrist; bride: "Oh, mine? I shower in it." | — |
| 20-25s | Product beat: hands-only LC box, '14K PVD · waterproof' | "Any 7 for $85" |
| 25-28s | SIL quietly searching "louise carter" on her phone | Payoff laugh |

### Hooks

- "She laughed at my necklace at my engagement party."
- "My mother-in-law said real women wear real gold."
- "He bought her the expensive one. She got the one that lasted."
- "The bridesmaid who mocked my jewelry turned green first."

### Production recipe

1. **Story (Claude):** pick a humiliation moment tied to LC's real problem (green neck, tarnish, cheap-looking jewelry at an event). 6-8 beats, 25-30 s, 2-3 characters.
2. **Character lock:** generate each character once (GPT Image / Nano Banana), keep a reference sheet; same outfit per scene.
3. **Shots:** 12-16 clips of 1.5-2.5 s in Seedance 2.5 / Kling / Veo, 9:16; or Arcads' short-drama template.
4. **Dialogue + lip-sync:** max 8 words per line; ElevenLabs voices; Arcads/HeyGen lip-sync for close-ups.
5. **Product shots must be real** LC footage (no AI-rendered jewelry), cut in for the payoff.
6. **Edit:** cut every 1-2 s, music stings on reveals, burned-in captions; export 25-30 s and a 45-60 s version.

### Existing bot prompt

```
Write 5 short revenge-drama ad scripts (25-30 s, 12-16 shots) for Louise Carter. Structure: 0-2 s humiliation/betrayal tied to jewelry (green neck, 'cheap' comment, tarnish at a big event); 2-15 s escalation with fast cuts; twist where the LC piece survives water/sweat and the antagonist's doesn't; 20-25 s real product beat (any 7 for $85); 25-30 s payoff. Give each shot: duration, camera, action, dialogue (≤8 words), on-screen text, and a Seedance prompt. Mark AI disclosure. Never name a competitor.
```

### Variants to test

- Length 25 s vs 45 s vs 60 s
- AI vs acted
- Antagonist (SIL vs MIL vs ex)
- Product reveal time (15 s vs 20 s)

## Reference examples

See [examples/README.md](examples/README.md) (5 posts). Top 5:

- @frankyecom (282L/437BM/67kV): Women want shows: characters, drama, payoff; build entertainment first, slot product in. — https://x.com/frankyecom/status/2106833649970684195
- @0xROAS (104L/139BM/9kV): 100% AI Drama Ad with Seedance 2.5... module is live inside ai ads community here’s how to make sure your dramas hit: - start with a very aggressive hook - make — https://x.com/0xROAS/status/2107188290264740348
- @zedmadeit (27L/61BM/3kV): heres how to make ai drama ads for your brand ai dramas are the new trend and theyre great for engagement but you want the right kind the kind that actually con — https://x.com/zedmadeit/status/2102176819709673703
- @david_attisaas (4L/6BM/708V): I'm running short drama ads for a few apps right now, and every one of them started as a copy of something a dropshipper ran first. I went looking after the tal — https://x.com/david_attisaas/status/2108195582607081720
- @ViralOps_ (4L/5BM/579V): Koriderm is absolutely CRUSHING with these DRAMA ads rn. they're literally making mini movies just to sell skincare products 😭 and i think this could be one of  — https://x.com/ViralOps_/status/2108255353016406383
