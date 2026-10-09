# BOT.md · generate a "Shock-headline typographic static (story headline + product block)"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 1 static, 1080x1350 (also 1080x1920)), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@tryatria_AI](https://x.com/tryatria_AI/status/2105745816828940336) · A plain white static from Resilia with a huge black headline: "MY SISTER SLEPT WITH MY HUSBAND." Below: "Eight months later, she's the one everyone calls beautiful at family dinners. Because she drains parasites. And I didn't even know I had them." Then the product pack and "SHOP NOW". All the work is done by the shock line.
- Example: [@iwo_cybulski](https://x.com/iwo_cybulski/status/1946251552919814347) · Long text static ad for Vitaboost 🔥 → Want high-converting static ads + media buying for your brand? DM me "ads" ⚡
- Example: [@Aidanb2b](https://x.com/Aidanb2b/status/1989120076415705137) · Which one of you was behind this ad creative masterclass. Big headline Great offer Urgent CTA 10/10

### Live paid ads in this format (9 in [adlibrary/](adlibrary/README.md), longest-running first)

- **BioRoot Labs: "We don't trick you into taking turmeric" retention-claim static** (481 days live): A beige static: "We don't trick you into taking turmeric. Your body convinces you to keep going. After one bottle, most people don't cancel. They stock up." Bottle and capsules, "Trusted by thousands" with Trustpilot stars.
- **Dr Ruth White: Persona-page "this woman found relief" static (Dr Ruth White)** (416 days live): An older woman with a red-glowing knee inset; black bar: "VIRAL: THIS WOMAN FOUND RELIEF FROM DAILY IBUPROFEN WITH JUST ONE TURMERIC SUPPLEMENT · CLICK TO LEARN". Run from the persona page "Dr Ruth White". DCO with 22 media.
- **Pure Rhythm: "Content may go offline" podcast clip (weight loss)** (326 days live): "If you want to go from size L to size S, you need to hear this… three essential ingredients that the industry does everything to hide from you… share this with your friend because this content may go offline at any moment." 117 s.
- **Pinch Magic Fiber: Product callout-label static ('This cleared my stuck poop')** (258 days live): Close-up of a scoop over the jar, black pill headline 'THIS CLEARED MY STUCK POOP' and 3 small callout labels pointing at the product (perfect poops / high-quality psyllium husk / tastes great).
- **Wellness Way UK: "Regain your confidence, without pills" device static (Wellness Way UK)** (252 days live): A hand holds a black device: "REGAIN YOUR CONFIDENCE, WITHOUT PILLS", "Harder, stronger erections in just 10 minutes", "50% OFF today" badge.
- **Shopmenvault: "BUY 2, GET 2 FREE – We won't do this again" offer static** (251 days live): A black static: "BUY 2, GET 2 FREE", "WE WON'T DO THIS AGAIN", 3 boxer briefs, "50% OFF deals", "Trusted by 10,000+ men after prostate surgery".

**Do not copy (seen in these live ads):** Fictional first-person stories presented as true.

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| Top 45% | White background, huge condensed black headline (Anton/Bebas/Druk), tight leading | Story line in quotes: "MY SISTER STOLE MY NECKLACE." |
| Middle | Regular weight body, 32-40px, 3 short lines | Twist that turns to the product: "Six months later she still won't give it back. Because she swims in it." |
| Bottom | Product pack shot right, brand + 2-line benefit left | "[Brand]. 14K PVD, waterproof." + "SHOP NOW →" |

### Prompts

**Figma spec**

```
Canvas 1080x1350, margins 64px, headline 120-150px condensed bold uppercase, line-height 0.95, body 36px regular, product PNG 380px with soft shadow, logo 48px.
```

**Headline bank (Claude)**

```
Give me 30 one-line story headlines (max 7 words) about a woman and a piece of jewelry that sound like the start of a juicy story: betrayal, envy, a lost heirloom, a stolen gift. No product claims.
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
- [ ] Files named `F10-<concept>-<variant>`; tracking tag `utm_content=F10-<concept>-<variant>`.
- [ ] Avoid: The headline must be a story, not a benefit; "Waterproof gold" never stops a scroll.
- [ ] Avoid: Keep the twist honest and tied to a real benefit.
- [ ] Avoid: Do not imply a real named person did something.

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
5. Name every asset `F10-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F10
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

White background, huge condensed black headline that is a story line, 3 short lines of body continuing the story with a twist, product pack-shot bottom right, brand + 2-line benefit + "SHOP NOW →". Example: "MY SISTER SLEPT WITH MY HUSBAND. / Eight months later, she's the one everyone calls beautiful at family dinners. / Because she drains parasites. / And I didn't even know I had them." ([@tryatria_AI](https://x.com/tryatria_AI/status/2105745816828940336)).

### Why it works

Typography-only reads in 1s, novelty of a tabloid line in a polished feed; cheap to produce → huge variant volume.

### Hooks

Family betrayal line, confession, overheard insult, "Nobody at the reunion recognised me".

### Production recipe

Figma/Canva template; Claude writes 50 headlines in LC voice; designer approves 10; resize 1:1/4:5/9:16.

## Reference examples

See [examples/README.md](examples/README.md) (2 posts). Top 5:

- @tryatria_AI (73L/98BM/4kV): Static hook 'My sister slept with my husband' vs generic benefit lines. — https://x.com/tryatria_AI/status/2105745816828940336
- @adamtaylorl (17L/9BM/3kV): Fully agree. Most brands have a winning ad they haven't made yet and the footage is already sitting on a hard drive. But there's a reason this works that most p — https://x.com/adamtaylorl/status/2103439375787003983
