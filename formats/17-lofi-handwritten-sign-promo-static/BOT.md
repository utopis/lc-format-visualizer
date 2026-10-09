# BOT.md · generate a "Lo-fi promo statics (handwritten sign + 24 BFCM variants)"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 1 static, 1080x1350), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@adamtaylorl](https://x.com/adamtaylorl/status/2106021392567198020) · A handwritten paper sign taped above a product on a Christmas tree: "WellnessBaby CYBER MONDAY 60% OFF TODAY!". It looks shot on a phone, lo-fi on purpose.
- Example: [@tryatria_AI](https://x.com/tryatria_AI/status/2098414761578811635) · HANDWRITTEN ADS SHOULDN’T WORK THIS WELL. BUT THEY DO. 👀 Handwritten notes. Whiteboards. Crude drawings. Marker scribbles. They look almost too simple
- Example: [@stnkvcs](https://x.com/stnkvcs/status/2077403948370067675) · I've been ranting a lot about native ads lately. I love 'em. But while they do tickle the algo (and my fancy) in just the right way, "native" is just 
- Example: [@Simon__Rob](https://x.com/Simon__Rob/status/2089448804676239424) · this is how your Meta ad account should be built if you're a brand: - ugly static ads and yapping videos stop cold traffic - testimonials and stats co

### Live paid ads in this format (1 in [adlibrary/](adlibrary/README.md), longest-running first)

- **Alicia Darling: Gym-clock POV with sticky caption ("Black leggings so I hope no one notices")** (319 days live): A POV of sneakers on a gym floor, a flip-clock "10:45" overlay, a white caption bubble: "Black leggings so I hope no one notices 😅". 4 variants ("At least no one else will smell me now"). Alicia Darling has 710 ads.

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| Frame | Phone photo of a real handwritten sign (marker on paper or cardboard) taped somewhere real: fridge, shop counter, Christmas tree | The offer in handwriting: "ANY 7 FOR $85. TODAY ONLY."  |
| Product | Product in the photo next to the sign, natural light | Nothing else; no logo overlay |
| Primary text | - | One line that sounds like a person: "we made a sign because people kept asking" |

### Prompts

**Shoot**

```
Write the sign with a thick Sharpie on printer paper, tape it, shoot on iPhone in daylight, slight angle, no edits except crop.
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
- [ ] Files named `F17-<concept>-<variant>`; tracking tag `utm_content=F17-<concept>-<variant>`.
- [ ] Avoid: The sign must be really handwritten; fonts that imitate handwriting look fake.
- [ ] Avoid: Only promote a real offer with a real end date.

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
5. Name every asset `F17-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F17
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

## Reference examples

See [examples/README.md](examples/README.md) (12 posts). Top 5:

- @adamtaylorl (57L/112BM/6kV): 25 BFCM static ads incl. The Handwritten Sign. — https://x.com/adamtaylorl/status/2106021392567198020
- @thekaipullai (373L/4BM/24kV): What's the point of all these record profits when it was the worst broadcasted sporting event anyone has ever seen. Never in my life I have seen a sporting chan — https://x.com/thekaipullai/status/2106771287096119428
- @Tonystakkz (132L/106BM/13kV): This is why Shaun for me is top 5 copywriter in 2026. He understands how copywriting in the modern world works. Abraham Lincoln said something very similar: "Gi — https://x.com/Tonystakkz/status/2099548690360721815
- @binghott (133L/57BM/20kV): We might be cooked Go to your best image ad in Ads Manager and check Meta's AI generated image options. I found a handwritten Post-It note ad in it. And it wasn — https://x.com/binghott/status/2077730930785980720
- @tryatria_AI (72L/93BM/3kV): HANDWRITTEN ADS SHOULDN’T WORK THIS WELL. BUT THEY DO. 👀 Handwritten notes. Whiteboards. Crude drawings. Marker scribbles. They look almost too simple compared  — https://x.com/tryatria_AI/status/2098414761578811635
