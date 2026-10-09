# BOT.md · generate a "Faceless niche slideshow (content-first, product as one tip)"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 5-6 slides, 1080x1920 (TikTok photo mode) or 1080x1350 (IG)), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@leonclipping](https://x.com/leonclipping/status/2104660939069170110) · A TikTok profile for a faceless relationship page (@notruthlove). Every post uses the same photo of a couple by the sea. Only the title text changes ("the strict agreements we made before signing a lease", "Rules we made after we almost broke up"), and each post gets about 100K to 775K views. The page never shows a face, and the product is pushed inside the slides.
- Example: [@PerezHatesAI](https://x.com/PerezHatesAI/status/2106779894785188006) · This is wild 😭 4.3M views. 250K saves. On a "weird habits" slideshow. No product demo. No feature dump. Just aesthetic slides of habits that "actually
- Example: [@rsalimx](https://x.com/rsalimx/status/2108259483902513153) · nah this is actually insane 😭 the account has posts sitting at 40m views and the app is doing ~$10k mrr off it recipes are the most natural slideshow 
- Example: [@rsalimx](https://x.com/rsalimx/status/2107517609960702306) · Running-girl ICP page; app shows on slide 4 of 5 right before last tip (can't get full list without seeing it).
- Example: [@ChadAppDev](https://x.com/ChadAppDev/status/2098786343836860487) · Before building: make niche TikTok page, find most viral slideshow formats, copy with own flavor, 1/day.
- Example: [@ChadAppDev](https://x.com/ChadAppDev/status/2107186633871114374) · Repost of ChadAppDev niche slideshow method.
- Example: [@leonclipping](https://x.com/leonclipping/status/2106833379823894702) · GLP-1 diary page: different selfie per post, 'what nobody tells you about first 8 weeks', tracker app as one tip.
- Example: [@Dkevs_](https://x.com/Dkevs_/status/2100425887636472312) · $200K MRR app via TikTok slideshows; don't overcomplicate with clippers.
- Example: [@mufvza](https://x.com/mufvza/status/2082847934841049519) · Analysis of 1,000 app slideshows: most-viewed != most installs; track saves/profile clicks per slideshow.

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| Slide 1 (cover) | The page's signature photo (same one every post: a faceless couple / hands / a view), slightly darkened so white text reads | Title in TikTok "Classic" font, white with black shadow, 6-10 words: "rules we made after we almost broke up" |
| Slide 2 | Same photo or a close variant | Tip 1, written like a diary line: "1. no phones at dinner. not even face down." |
| Slide 3 | Same photo | Tip 2, slightly vulnerable: "2. we say the annoying thing the same day" |
| Slide 4 (product slide) | Same photo; the product is NOT pictured big. Optional small inset of it worn | Tip 3 IS the product, framed as a habit: "3. matching necklaces we never take off. even in the shower (ours are from [brand])" |
| Slide 5 | Same photo | Tip 4, the most emotional one, so the product slide is sandwiched |
| Slide 6 | Same photo | Soft close: "save this for the next hard week". No CTA, no link. |

### Prompts

**Midjourney / Nano Banana (signature photo)**

```
candid film photo of a couple seen from behind sitting on a sea wall at golden hour, faces not visible, her hand on his knee, thin gold chain on her neck, soft grain, 35mm, muted warm tones, vertical 9:16 --style raw
```

**Claude / ChatGPT (captions)**

```
Write 10 slideshow scripts for a faceless relationship page. Each: a 6-10 word title in lowercase, 5 numbered tips in the voice of a woman writing in her notes app. In exactly one tip per script, mention [product] as a habit the couple has, never as a recommendation. No hashtags, no emojis.
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
- [ ] Files named `F01-<concept>-<variant>`; tracking tag `utm_content=F01-<concept>-<variant>`.
- [ ] Avoid: Changing the photo every post kills the page identity; the repeat image IS the brand.
- [ ] Avoid: The product slide must read like a tip, not an ad. If it says "shop now" the slideshow loses saves.
- [ ] Avoid: Post 1-3 times a day from a warmed account for 2+ weeks before judging; one slideshow is not a test.
- [ ] Avoid: Use AI or licensed photos only; never lift a real couple's photo.

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
5. Name every asset `F01-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F01
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

A 4-6 slide photo carousel that reads like genuinely useful niche content (tips, rules, lists, diary). The product appears **once**, framed as one of the tips — typically slide N-1 ("right before the last tip so you can't get the full list without seeing it", @rsalimx).

Slide-by-slide (proven skeleton):
1. **Hook slide** — candid, slightly imperfect photo (same persona/couple/selfie style every post for recognisability) + big white text hook: "rules we made after a fight", "what nobody tells you about the first 8 weeks", "5 ways to get [result]".
2-3. **Value slides** — one tip per slide, short, true, specific.
4. **Product slide disguised as a tip** — "#4: the one thing I stopped doing… I switched to X".
5. **Last tip / payoff** — closes the list (keeps saves high), soft CTA in caption.

Account pattern: one niche identity (relationship, GLP-1 diary, running girl, recipes), one visual constant (same couple photo / different selfie each post), same format every post, 1-2 posts/day. Batch: research 1h → write 2 months of slides in one 4-6h day (@sulfurscales, @brainextends, @enzoxmotion). Sequence: content, content, content, content, "ad warm-up", product push.

### Why it works

Photo-mode posts get saved and swiped (dwell + saves are strong ranking signals); the content is useful on its own so it isn't skipped as an ad; one recognisable visual constant builds a "page" people follow. @mufvza's 1,000-slideshow analysis: **most-viewed ≠ most installs** — track saves and profile clicks, not views. @g_buildz_apps: fewer slides (≤4) and CTA always last.

### Hooks

- "rules we made after a fight" / "things my boyfriend does that…" (relationship)
- "what nobody tells you about [first 8 weeks of X]" (diary)
- "5 ways to get [result]" / "[N] [things] for your lazy ass" (listicle)
- "POV: you finally [identity outcome]"
- "things I wish I knew before [milestone]"

### Production recipe

- Research account: fresh TikTok used only for research, follow nothing but the niche, like/save target content for a few days so the FYP becomes a format feed (@brainextends).
- Images: own UGC photos / product shots / licensed lifestyle photos, or AI images (Nano Banana, GPT Image) with a consistent persona prompt. @MaxHirsch13 agent prompt: *"Make me a 6-slide TikTok photo carousel for [brand]: slide 1 is a wide, candid, realistic photo with the hook '5 ways to get [result]' in white text, slides 2-6 …one tip each"*.
- Build: Canva bulk-create, Volume, or a Claude script writing slide JSON → Canva/Figma template. Schedule via native scheduler or Postiz/Buffer (official APIs).
- Cost: ~$0-3/post; time ~15 min/post batched.

## Reference examples

See [examples/README.md](examples/README.md) (32 posts). Top 5:

- @ErnestoSOFTWARE (941L/1533BM/95kV): 11.5M views one faceless account; pitches Arcads automating carousels; 3-4 accounts. — https://x.com/ErnestoSOFTWARE/status/2103534688048414959
- @sulfurscales (452L/1127BM/87kV): Batch 2 months of slideshows in one 4-6h day; sequence content x4 -> ad warm-up -> product push. — https://x.com/sulfurscales/status/2075642615316513195
- @leonclipping (449L/765BM/37kV): Faceless relationship page: same couple photo every post, 'rules we made after a fight' slides, app plug as bonus tip; 1.7M top post. — https://x.com/leonclipping/status/2104660939069170110
- @mufvza (277L/674BM/44kV): Analysis of 1,000 app slideshows: most-viewed != most installs; track saves/profile clicks per slideshow. — https://x.com/mufvza/status/2082847934841049519
- @rsalimx (267L/428BM/16kV): Fitness page pushing one workout app; 4.8M views slideshow; reads as tips, is an ad. — https://x.com/rsalimx/status/2107549240868422131
