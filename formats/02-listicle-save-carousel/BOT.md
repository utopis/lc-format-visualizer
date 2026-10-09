# BOT.md · generate a "Listicle save-carousel (one item per slide)"

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
5. Name every asset `F02-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F02
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

Cover slide with a big, warm "for you" headline over a hero image ("High protein dinner ideas FOR YOU", "5 weeknight dinners for your lazy ass", "dinners to make for your husband this week") then **one item per slide**, each a beautiful photo + 1-line label. Product/app line sits in bio ("Get our app with all 500+ recipes") or on the last slide ("all of this, in your pocket"). Example account: @success.fitness — 1.4M followers, 25.4M likes, posts at 16-42M views ([@rsalimx](https://x.com/rsalimx/status/2108259483902513153)).

### Why it works

People save lists on instinct (utility), share to partners/friends ("make this for me"), and return to it; saves + shares push distribution. Zero face, zero filming.

### Hooks

"[N] [things] for your [lazy ass / husband / 9-5 week]", "[season] [things] to [do]", "[Result] ideas FOR YOU (with [details])", "save this for [occasion]".

### Production recipe

Photos: LC product photography + customer UGC (with permission) + AI-styled on-body shots (see F20). Template in Canva: cover + 5-8 item slides. Agent prompt (adapted from @MaxHirsch13): *"Make a 7-slide carousel for Louise Carter: slide 1 wide candid photo of [persona] with hook '[N] waterproof stacks for [occasion]' in white serif text; slides 2-7 one stack per slide, label = piece names + price; last slide 'all pieces 14K PVD, shower-proof'."*

## Reference examples

See [examples/README.md](examples/README.md) (12 posts). Top 5:

- @MaxHirsch13 (75L/224BM/3kV): Exact agent prompt for 6-slide carousel: candid wide photo + '5 ways to get [result]' hook, slides 2-6 one tip each. — https://x.com/MaxHirsch13/status/2108340891601748034
- @rsalimx (120L/200BM/6kV): Running-girl ICP page; app shows on slide 4 of 5 right before last tip (can't get full list without seeing it). — https://x.com/rsalimx/status/2107517609960702306
- @rsalimx (103L/146BM/6kV): Recipe slideshows (one meal per slide) hit 40M views; app = 'all of this in your pocket'. Save-bait listicle. — https://x.com/rsalimx/status/2108259483902513153
- @_afterblossom_ (3932L/391BM/35kV): Throwing back this piece to see in the new carousel format https://t.co/rOPT5RDzKO — https://x.com/_afterblossom_/status/2095194062756413781
- @rustybrick (17L/13BM/5kV): ChatGPT Ads Product Updates including multi-product carousel format for product feed campaigns https://t.co/TWMRyCOCy2 — https://x.com/rustybrick/status/2085121962976661782
