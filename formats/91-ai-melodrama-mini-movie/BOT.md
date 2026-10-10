# BOT.md · generate a "AI melodrama mini-movie (2-10 min soap opera, humiliation → mentor → vindication, product after the midpoint)"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 3-8 min film (9:16), plus a 60s cut-down), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@TheIvanKreimer](https://x.com/TheIvanKreimer/status/2107808445508321597) · An AI live-action melodrama (Smooche): a woman at an ID-photo desk being told she looks old ("in this photo", "what did you do?"), office scenes with colleagues, and the product only appearing around 1:54.
- Example: [@LachezarVoynov](https://x.com/LachezarVoynov/status/2071623979371225598) · What’s that ad creative style called? I reckon a ‘mini-movie’? I bet it prints. This is the typical hero’s journey used to create 99% of the Western w
- Example: [@LachezarVoynov](https://x.com/LachezarVoynov/status/1976293825112150474) · This is undeniably the best ad we’ve created in 2025. It combines many different elements that we've seen work in 2025, after spending over $20M on Me
- Example: [@ViralOps_](https://x.com/ViralOps_/status/2108255353016406383) · Koriderm is absolutely CRUSHING with these DRAMA ads rn. they're literally making mini movies just to sell skincare products 😭 and i think this could 
- Example: [@zedmadeit](https://x.com/zedmadeit/status/2102176819709673703) · heres how to make ai drama ads for your brand ai dramas are the new trend and theyre great for engagement but you want the right kind the kind that ac
- Example: [@0xROAS](https://x.com/0xROAS/status/2104589798208065796) · 100% AI drama ad (Seedance): turn the winning ad into a 2-3 min story; Resilia hooks: cheating husband/wife, compared to another girl.
- Example: [@SGradon](https://x.com/SGradon/status/2101705439565979947) · In 2026 creative strategists should steal from screenwriters AI drama ads are becoming a trend, and everyone's about to copy the same 5 stories. Here'
- Example: [@tryatria_AI](https://x.com/tryatria_AI/status/2100612079891755286) · AI ANIMATED STORYTELLING ADS SHOULDN’T WORK THIS WELL. BUT THEY DO. 👀 Cartoon characters. Dramatic storylines. Pixar-style animation. Ridiculous plot 
- Example: [@whotanish](https://x.com/whotanish/status/2100587035786715295) · All the big brands have already catching up too the AI drama ads . users have organically have been watching the micro dramas for really long It has b

### Live paid ads in this format (7 in [adlibrary/](adlibrary/README.md), longest-running first)

- **PopDrama 02: Long-form short-drama episode ad (PopDrama, 19:41)** (406 days live): A full episode of a ReelShort-style drama (a boardroom, a betrayed heroine, a CEO), running 958-1,181 s, used as a Meta ad by the drama app.
- **Olivia Ramirez: English soap-style drama ad (Olivia Ramirez, 4:40)** (277 days live): An English live-action melodrama: a cheating confrontation, "I've been using my money and living under my roof… kick this woman out", and a bank-card reveal. 274-280 s.
- **Smooche · Cosmetic Times: “I had a sit next to my Miss it it was my daughter So I had to walk in…”** (44 days live): Opens: “I had a sit next to my Miss it it was my daughter So I had to walk in In front of everyone and be seen and the only reason I walked in with my head up was because of what my best friend Handed me…”
- **Smooche · Cosmetic Times: “I had to sit next to my ex husband So I had to walk in front of…”** (44 days live): Opens: “I had to sit next to my ex husband So I had to walk in front of everyone and be seen And the the only reason I walked in with my head up was because of what my best friend handed me three nights…”
- **Smooche · Cosmetic Times: “He's not leaving until you listen to her 8 months after the divorce was…”** (44 days live): Opens: “He's not leaving until you listen to her 8 months after the divorce was finalized 8 months of staring at myself in the mirror every morning When I started looking so old I spent the whole week…”
- **Smooche · Smooche: “My ex has been locked in A woman he left me for Young enough to be her…”** (21 days live): Opens: “My ex has been locked in A woman he left me for Young enough to be her daughter On the first date, I've been on in 22 years And the only reason I didn't fall apart On both of them So, the day before,…”

**Do not copy (seen in these live ads):** Most of these are fully AI-generated actors and are not labelled as such, and the health outcomes in the plots are dramatised. Disclose AI and keep any claim inside what you can substantiate.

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| 0:00-0:20 Humiliation | Office ID-photo counter; clerk looks at her photo then at her | Clerk: "Ma'am, that's not you in this photo." She touches her bare neck. |
| 0:20-1:30 Wound | Close-ups at home; old jewellery in a box, green-tinged | Her sister on the phone: "Just buy something new." "I did. Three times." |
| 1:30-2:30 Mentor | A friend at a café, unbothered, sea-swim hair | Friend: "I haven't taken mine off in a year." Slides a small box across the table. |
| 2:30-4:00 Climb | Montage: shower, beach, a work presentation; the necklace catches light | Little or no dialogue; music builds |
| 4:00-5:00 Vindication | Back at the same counter | Clerk: "...You look different." She smiles. |
| Last 30s | Brand card, offer, AI-generated label | "Any 7 for $85. This film uses AI-generated actors." |

### Prompts

**Veo 3 (scene)**

```
live-action melodrama, a 55-year-old woman at an office ID-photo counter, a clerk says "Ma'am, that's not you in this photo", soft fluorescent light, handheld, 8s, 9:16
```

**Character consistency**

```
Generate a reference sheet for each character first, then use it as image input for every shot (Kling Elements / Veo ingredients).
```

**Claude (script)**

```
Write a 5-minute melodrama: humiliation, failed fixes, mentor, gift, doubt, climb, vindication, pitch. Product appears only at the gift. Dialogue under 15 words per line.
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
- [ ] Files named `F91-<concept>-<variant>`; tracking tag `utm_content=F91-<concept>-<variant>`.
- [ ] Avoid: Label AI actors.
- [ ] Avoid: No fake credentials for the mentor.
- [ ] Avoid: Most viewers drop before the product appears; test 60s and 3-minute cuts.
- [ ] Avoid: Keep the humiliation light; cruelty reads badly for a gift brand.

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
5. Name every asset `F91-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F91
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

A single, self-contained short film (not a series) told like a daytime soap: the hero is publicly humiliated (ex shows up with a younger partner, an ID clerk says "that's not you", husband mistaken for the caterer), tries everything, then a close, credible mentor hands over the product; the climax replays the opening scene with the roles reversed. The pitch is the last ~30-60 s. Resilia and Smooche run it both spoken and sung (sung = F04).

### Why it works

- It does not look like an ad, so cold audiences watch; the people still watching at minute 2 are pre-qualified buyers.
- The pain is social (being seen, being compared), not product-level, which is far stronger than a benefit claim.
- The mentor (sister, best friend who is a dermatologist, Seoul colleague) delivers the mechanism as overheard dialogue, which reads as discovery rather than a pitch (@Inceptly).
- Caveat: @TheIvanKreimer measured 90-95% drop-off before the product appears. You pay for entertainment; it only wins where shorter DR has saturated.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0:00-0:08 | Cold open on the humiliation: ex-husband at the daughter's graduation with his new partner; she touches her bare neck | VO: "I had to sit next to my ex-husband and the woman he left me for…" |
| 0:08-0:40 | Rewind: years of putting herself last, stopped buying anything for herself, jewelry box of green-stained pieces | "Everything I wore turned my skin green, so I stopped wearing anything." |
| 0:40-1:10 | Mentor scene: best friend (real jeweller or long-time customer) hands her a small box | "Sit down. Don't argue. Wear this to the graduation and don't take it off." |
| 1:10-1:40 | Doubt → small wins: showers in it, swims in it, coworker compliments | "Day 4: still gold. Day 9: someone asked where it's from." |
| 1:40-2:10 | Vindication: same graduation photo line, the new partner asks where the necklace is from | "'Where is that from?' she asked. I just smiled." |
| 2:10-2:30 | Pitch card: any 7 for $85, waterproof 14K PVD | "Louise Carter. Any 7 for $85. Link below." |

### Hooks

- "I had to sit next to my ex-husband and the woman he left me for."
- "The clerk said I didn't look like my own ID photo."
- "At my 40th anniversary party, they thought my husband was the caterer's date."

### Production recipe

1. Pick one sub-avatar (e.g. 52, divorced, "stopped buying herself anything") and write her private fear in one line.
2. Write the 12 beats (Maxfusion): ordinary world, humiliation, wound deepens, frozen, sees it too, failed fixes, mentor, gift, doubt, climb, vindication, pitch.
3. Mentor = someone close AND credible (friend who is a jeweller, sister, mother). Never a salesperson.
4. Produce a 90 s and a 2:30 cut; product enters after 55-60% of runtime; captions burned in.
5. Real actors, or clearly fictional AI characters with a "dramatisation" label; never present it as a real customer story.

### Existing bot prompt

```
Write a 2:30 melodrama ad script for Louise Carter (waterproof 14K PVD jewelry, any 7 for $85). Sub-avatar: {{AVATAR}}. Use the 12-beat structure: humiliation in the first line, wound deepens, hero freezes, failed fixes (green-staining jewelry, taking it off, stopped wearing any), close credible mentor gifts the piece, doubt, week-by-week small wins noticed by others, vindication that reverses the opening scene, 25-second pitch. Mark it as a dramatisation. No health, income or "real customer" claims.
```

### Variants to test

- Spoken vs sung (F04)
- 90 s vs 2:30
- Product at 40% vs 60%
- Revenge vs reconciliation ending

## Reference examples

See [examples/README.md](examples/README.md) (30 posts). Top 5:

- @briannjho (138L/338BM/10kV): Ad picks: Smooche AI song ad, Ryze AI skit, UndrDog big-enemy, Everyday Dose skit, Serene Herbs AI identity, Nuora apology mash-up, Mama Bear "this is what happ — https://x.com/briannjho/status/2094662259746480410
- @TheIvanKreimer (1L/0BM/62V): Smooche AI melodrama: ID-photo clerk scene, product at 1:54; retention: 90-95% drop before product. Try only if short DR saturated. — https://x.com/TheIvanKreimer/status/2107808445508321597
- @0xROAS (0L/0BM/0V): 100% AI drama ad (Seedance): turn the winning ad into a 2-3 min story; Resilia hooks: cheating husband/wife, compared to another girl. — https://x.com/0xROAS/status/2104589798208065796
- @EcomSapo (0L/0BM/0V): Smooche top ad of 1,600+: "At 63 I ran into my ex at Walmart" + Seoul colleague, 5:37; Atria #1 of 721, 70d. "Resilia blueprint works for skincare." — https://x.com/EcomSapo/status/2103047669556166886
- @CSRIPPER (0L/0BM/0V): "10 minute movie ad with a Japanese/Swiss authority": Resilia, Lymphoria all run them. — https://x.com/CSRIPPER/status/2101315284753629664
