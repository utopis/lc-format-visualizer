# BOT.md · generate a "Faceless niche slideshow (content-first, product as one tip)"

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
