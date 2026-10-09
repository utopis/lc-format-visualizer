# BOT.md · generate a "AI melodrama mini-movie (2-10 min soap opera, humiliation → mentor → vindication, product after the midpoint)"

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

See [examples/README.md](examples/README.md) (27 posts). Top 5:

- @briannjho (138L/338BM/10kV): Ad picks: Smooche AI song ad, Ryze AI skit, UndrDog big-enemy, Everyday Dose skit, Serene Herbs AI identity, Nuora apology mash-up, Mama Bear "this is what happ — https://x.com/briannjho/status/2094662259746480410
- @TheIvanKreimer (1L/0BM/62V): Smooche AI melodrama: ID-photo clerk scene, product at 1:54; retention: 90-95% drop before product. Try only if short DR saturated. — https://x.com/TheIvanKreimer/status/2107808445508321597
- @0xROAS (0L/0BM/0V): 100% AI drama ad (Seedance): turn the winning ad into a 2-3 min story; Resilia hooks: cheating husband/wife, compared to another girl. — https://x.com/0xROAS/status/2104589798208065796
- @EcomSapo (0L/0BM/0V): Smooche top ad of 1,600+: "At 63 I ran into my ex at Walmart" + Seoul colleague, 5:37; Atria #1 of 721, 70d. "Resilia blueprint works for skincare." — https://x.com/EcomSapo/status/2103047669556166886
- @CSRIPPER (0L/0BM/0V): "10 minute movie ad with a Japanese/Swiss authority": Resilia, Lymphoria all run them. — https://x.com/CSRIPPER/status/2101315284753629664
