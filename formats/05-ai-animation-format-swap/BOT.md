# BOT.md · generate a "AI animation format swap (Claymation, Pixar-3D, Zach-Films 2nd-person, Skeleton, Chalkboard, Brick, Tiny-characters)"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: Same length as the source winner (15-60s)), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@oliverxmedia](https://x.com/oliverxmedia/status/2099359156121825337) · An Arcads demo: one short scene re-rendered in several animation styles, shown side by side and sequenced (Pixar-3D kids in a room, then the same beat in other looks). It shows the core move of the format: keep the script, swap the visual style.
- Example: [@Diego_exits](https://x.com/Diego_exits/status/2101991919920243015) · PRIMALQUEEN $6M/mo, 1,019 active ads; normal cartoon ads.
- Example: [@CEO_Vlad](https://x.com/CEO_Vlad/status/2107328605995077699) · 7 AI UGC animation styles and what each is good for (article).
- Example: [@ArmandasPuckus](https://x.com/ArmandasPuckus/status/2107781382533472512) · 'Selling to menopausal women with AI animations IS the method'.
- Example: [@LordofAds](https://x.com/LordofAds/status/2102132251706429937) · 'Money glitch': remake best 30-day ad in 6 animation styles (Pixar, anime, paper cutout, whiteboard, skeleton...).
- Example: [@therahulissar](https://x.com/therahulissar/status/2099519666045776287) · Break Meta audience cap with format change (same message, new display: AI video, static, lo-fi) and new personas.
- Example: [@CEO_Vlad](https://x.com/CEO_Vlad/status/2087333716334924071) · Pixar-style AI ads helped $117k day.
- Example: [@aaliya_va](https://x.com/aaliya_va/status/2098420179403444486) · A product image can now become a 3D ad without starting from scratch. Arcads lets you add your website and product image, pick an animation style and 
- Example: [@ashen_one](https://x.com/ashen_one/status/2105715646273368159) · if you're using AI to cook ads and you've been doing the claymation meta, the singing meta seems to be next using arcads, you can cook an entire ad in

### Live paid ads in this format (3 in [adlibrary/](adlibrary/README.md), longest-running first)

- **Hemios: Talking-product CGI skit (Hemios, "I'm not an accessory, Karen")** (254 days live): A Pixar-style couple in bed talk to an animated hematite ring: "I have to apologize… I thought you were a scam… I'm not an accessory, Karen. I'm 2,000 years of natural hematite. I was fixing men before pills existed." 32 s.
- **Dr. Lisa Downing: Pixar-style organ-and-pills CGI (kidneys)** (217 days live): Pixar-style 3D characters around organs and a pill bottle, with captions like "That foam was protein leaking through stressed kidneys… By day 15…" 123 s.
- **Resilia · Arterial Health Review: “What happens if you don if you don't clean out your arteries once they…”** (1 days live): Opens: “What happens if you don if you don't clean out your arteries once they start to clog? Day one, you feel completely normal, exactly like you have for years, but inside it has already begun.”

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| Before you start | Pick ONE proven script (a winner with stable CPA) | Do not change a word of the script; only the visual style changes |
| 0-3s | Hook shot in the new style (claymation, Pixar-3D, 2nd-person "you" camera, stop-motion) | Same hook line, same timing as the winner |
| 3-end | Re-render each shot of the winner shot-for-shot in the chosen style | Same VO (re-use the original audio if it is yours) and captions |
| Product shots | Cut back to REAL product footage, or a faithful 3D model | Same CTA as the winner |

### Prompts

**Midjourney / Nano Banana (style frames)**

```
claymation stop-motion style, handmade plasticine woman in a tiny bathroom set, soft studio light, visible fingerprints in clay, Aardman-like, 9:16 -- [scene description from the winner shot list]
```

**Kling / Runway / Seedance**

```
image-to-video, 4-6s, keep the style frame exactly, gentle motion, no morphing, no text
```

**Arcads / Creatify (optional)**

```
Upload the winning script, choose the "animation" or "Pixar" template, export 9:16 and 4:5.
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
- [ ] Files named `F05-<concept>-<variant>`; tracking tag `utm_content=F05-<concept>-<variant>`.
- [ ] Avoid: Changing script and style at the same time means you will not know what worked.
- [ ] Avoid: Each style is a new creative to Meta (new Entity ID); launch 3 styles together so they compete.
- [ ] Avoid: Keep the product real: stylised characters are fine, stylised jewelry misleads.
- [ ] Avoid: Pixar is crowded; claymation and 2nd-person POV were less saturated in the research window.

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
5. Name every asset `F05-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F05
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

Same script/angle as a proven ad, re-rendered in an animated style. Styles and their jobs (from @CEO_Vlad's 7-styles chart and tier list):
| Style | Good for | Why |
|---|---|---|
| Claymation | everyday embarrassing problems | clay hides AI artifacts → highest usable rate |
| Pixar-style 3D | emotional benefits (confidence, family) | faces carry emotion; stages what a camera can't |
| "Zach Films" 2nd-person cinematic | problems that compound | "you" inside the story, each scene worse |
| Skeleton | blunt truths / calling out habits | says rude things a person can't; burns out fastest |
| Chalkboard explainer | mechanism / how it works | drawing motion holds attention; teaches before selling |
| Brick style | step-by-step / before-after | building is satisfying (IP risk if LEGO-like) |
| Tiny characters on the body | invisible-cause problems | villain/hero battle |

@LordofAds "money glitch": take best 30-day ad (even UGC), recreate it **6 times** in Pixar, anime, paper cut-out, whiteboard/stick-figure, skeleton, 16-bit — new Entity IDs for Meta's Andromeda (see [Peter_Quadrel](https://x.com/Peter_Quadrel/status/2107325758238777477): visually similar ads share one Entity ID).

Shot structure (30-45s): 0-2s character + problem visual hook · 2-12s escalation (2-3 scenes) · 12-25s product enters as solution, mechanism visual · 25-35s life after · end card with real product photo + offer.

### Why it works

Pattern-break in a feed of UGC; animation feels like content; characters stage impossible scenes (the necklace surviving the ocean, chlorine, sweat); new visual style = new Entity ID = fresh delivery.

### Hooks

"What happens if you [do X] every day?" then Day 1 / Day 7 / Day 30 (FedotOff90 example transcript); skeleton: "Stop doing this…"; chalkboard: "How it works:" with a hand drawing.

### Production recipe

Claude skill pipeline (as built by @AlessandroLavis / @eliasrrecom): competitor research → script + hooks → scene list → image gen per scene (Nano Banana/Midjourney with style reference) → image-to-video (Kling/Seedance/Veo) → ElevenLabs VO → CapCut assembly. Agent "ad DNA" step (@ladprofit): extract hook, mechanism, emotional arc, belief shift from the winner before re-styling. Cost $5-40/ad, 1-3h.

## Reference examples

See [examples/README.md](examples/README.md) (29 posts). Top 5:

- @spwfeijen (908L/2121BM/74kV): Chalkboard Explainer AI ad format: native look, step-by-step drawing retention, myths/listicles. — https://x.com/spwfeijen/status/2107023055532810720
- @CEO_Vlad (894L/1279BM/49kV): 7 AI UGC animation styles and what each is good for (article). — https://x.com/CEO_Vlad/status/2107328605995077699
- @ArmandasPuckus (917L/605BM/45kV): 'Selling to menopausal women with AI animations IS the method'. — https://x.com/ArmandasPuckus/status/2107781382533472512
- @FynCas (348L/705BM/21kV): Same Chalkboard Explainer post (copied by FynCas). — https://x.com/FynCas/status/2107818540522737913
- @AlessandroLavis (397L/579BM/27kV): Claude skill for cartoon ads from one prompt (research->script->scenes->VO->animation). — https://x.com/AlessandroLavis/status/2104186859689836822
