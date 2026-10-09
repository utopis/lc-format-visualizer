# BOT.md · generate a "AI animation format swap (Claymation, Pixar-3D, Zach-Films 2nd-person, Skeleton, Chalkboard, Brick, Tiny-characters)"

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

- @spwfeijen (908L/2121BM/73kV): Chalkboard Explainer AI ad format: native look, step-by-step drawing retention, myths/listicles. — https://x.com/spwfeijen/status/2107023055532810720
- @CEO_Vlad (894L/1279BM/49kV): 7 AI UGC animation styles and what each is good for (article). — https://x.com/CEO_Vlad/status/2107328605995077699
- @ArmandasPuckus (903L/602BM/44kV): 'Selling to menopausal women with AI animations IS the method'. — https://x.com/ArmandasPuckus/status/2107781382533472512
- @FynCas (348L/705BM/21kV): Same Chalkboard Explainer post (copied by FynCas). — https://x.com/FynCas/status/2107818540522737913
- @AlessandroLavis (397L/579BM/27kV): Claude skill for cartoon ads from one prompt (research->script->scenes->VO->animation). — https://x.com/AlessandroLavis/status/2104186859689836822
