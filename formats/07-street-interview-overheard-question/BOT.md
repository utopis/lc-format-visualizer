# BOT.md · generate a "Street / resort interview & "overheard question" ("what are you wearing?")"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 20-60s, 1080x1920), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@adamtaylorl](https://x.com/adamtaylorl/status/2094742062755422423) · Phone-in-hand at a hotel front desk: the creator films herself asking staff what mattress the hotel uses (captions "FRONT DESK THIS...", "NOTHING SPECIAL", "WE STARTED PUTTING"), then cuts to a man sleeping badly, a woman unboxing the brand and the answer reveal. It looks like an overheard real conversation, not an ad.
- Example: [@tryatria_AI](https://x.com/tryatria_AI/status/2095860430099058905) · AI resort 'random interview' ('Are you really 56?') hook format.
- Example: [@maxxmalist](https://x.com/maxxmalist/status/2080007884406960319) · the new animation ads are crushing on fb here's an example created by my whop member you can literally do any format with AI: - podcasts - street inte
- Example: [@0xROAS](https://x.com/0xROAS/status/2078901864498692155) · the new drama ADS are crushing on fb lol. you can literally do any format with AI: - podcasts - street interview - drama ads - doctor/authority figure
- Example: [@vicmediaco](https://x.com/vicmediaco/status/2092248121581486114) · Made this street interview ad for a beauty brand … what do you think ? Need Video ads? …send a DM 📩 https://t.co/Km4XvI6oNF
- Example: [@theisaacmed](https://x.com/theisaacmed/status/2087181812103831724) · The ad frequency on my meta account for street interview agencies is at 100x. Every day I login to ig and am blasted by ads. https://t.co/UdeTr0VJDw

### Live paid ads in this format (1 in [adlibrary/](adlibrary/README.md), longest-running first)

- **Penrose Skin: Nightlife street-reaction montage (Penrose)** (89 days live): Night-street clips of people reacting to a man ("Before you go, what do you think of this?", "OK, that's dangerous"), then a VO: "That reaction? It's real. And it happens every time. This is Penrose Skin, a pheromone-infused body butter…" 41 s.

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| 0-3s | Phone in hand, filming a stranger or staff member (hotel desk, beach, street). Handheld, vertical, a bit messy | The overheard question as hook caption: "asked the hotel front desk what mattress this is" |
| 3-15s | The interviewee answers on camera (or the interviewer reacts) | Natural answer, unscripted feel: "people ask every day, it's [brand]" |
| 15-30s | Cutaways to the product in that real setting | Captions carry the key facts |
| 30-end | Creator to camera or end card | "so I bought one" + offer |

### Prompts

**Interview brief (real shoot)**

```
Shoot at a resort pool/beach. Ask 20 women: "what is that necklace, it looks expensive?" Ask permission on camera, get a signed release, film 4K 30fps vertical, wireless lav on the interviewer.
```

**AI version (Veo 3 / Seedance)**

```
handheld vertical phone footage of a woman at a hotel front desk asking the receptionist a question, natural daylight, realistic skin, slight camera shake, ambient lobby noise; 8s; then the receptionist smiling and answering
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
- [ ] Files named `F07-<concept>-<variant>`; tracking tag `utm_content=F07-<concept>-<variant>`.
- [ ] Avoid: Staged "real people" interviews that are presented as real are deceptive; if actors or AI, label it.
- [ ] Avoid: Get a release from everyone identifiable.
- [ ] Avoid: The question must be one a real person would ask; scripted-sounding questions kill the overheard feel.

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
5. Name every asset `F07-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F07
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

**Variant 1 — Interview**: handheld mic, stranger on the street/resort: "Are you really 56?" → "I lost 18 pounds in one month… it was cortisol" ([@tryatria_AI](https://x.com/tryatria_AI/status/2095860430099058905)). Question does the hooking; answer is social proof.
**Variant 2 — Overheard question (stronger)**: the product is discovered by a third party asking. GroundingWell: hotel guests calling the front desk asking what mattress they use — "Quick question, what kind of mattress you guys use?… I think you just saved me three grand… half the calls I get now are about the sheets" (transcript; [@adamtaylorl](https://x.com/adamtaylorl/status/2094742062755422423)). They don't even sell mattresses.

Shot list (20-30s, V2): 0-2s stranger approaches / phone rings "Sorry—where is your necklace from?" · 2-10s owner answers casually, fiddles with it · 10-20s reveal detail ("I swim in it") + close-up · 20-25s asker: "okay I'm ordering one" · end card.

### Why it works

Curiosity + third-party validation; viewer becomes the person asking. Resolves "is it real gold?" doubt via an honest answer on camera.

### Production recipe

Real: hire 2 creators, film in a café/beach, scripted-but-natural (disclose as ad). AI: Seedance/Veo two-character scene — only for dramatized skits, not presented as real people.

## Reference examples

See [examples/README.md](examples/README.md) (16 posts). Top 5:

- @adamtaylorl (362L/466BM/26kV): GroundingWell 550+ ads: hotel guests asking what mattress they use (overheard-question angle). — https://x.com/adamtaylorl/status/2094742062755422423
- @adamtaylorl (139L/203BM/13kV): Tier list of ecom formats: F = AI UGC, street interviews, read scripts; B = founder, testimonial compilations, listicle statics... — https://x.com/adamtaylorl/status/2097641383355879452
- @lorenzo_pravata (150L/196BM/10kV): "Ads that don't look like ads": podcast clips, street interviews, skits with studio actors; pet brand $29K→$150K/mo spend in 60 days, CPA $188→$124. — https://x.com/lorenzo_pravata/status/2104536224488738839
- @ZedNilm1 (116L/185BM/17kV): Resilia AI street interviews with 90+ year olds - believable, near-zero ad feel. — https://x.com/ZedNilm1/status/2101280447154036917
- @tryatria_AI (83L/150BM/9kV): AI resort 'random interview' ('Are you really 56?') hook format. — https://x.com/tryatria_AI/status/2095860430099058905
