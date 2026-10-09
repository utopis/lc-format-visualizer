# BOT.md · generate a "Elder-wisdom street interview + '3 things' countdown (the product is #3)"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 45-75s, 1080x1920), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@ZedNilm1](https://x.com/ZedNilm1/status/2101280447154036917) · An AI-generated street interview with a 90+ year-old man in a hat and long beard. The reporter asks him questions, he answers with captions ("MY GRANDFATHER LIVED"), then holds up the product ("MAKE A DIFFERENCE").
- Example: [@father_rmv](https://x.com/father_rmv/status/2100219781668356485) · Saint Thascius Caecilius Cyprianus, commonly known as Saint Cyprian of Carthage, stands as one of the most influential figures in early Christianity, 

### Live paid ads in this format (3 in [adlibrary/](adlibrary/README.md), longest-running first)

- **Prime Prometics: Older-man talking head (Prime Prometics persona ad)** (331 days live): A white-haired man in a black shirt talks and laughs to camera, holding the product tube, with captions ("…called PrimeLash", "but I'm going to try", "My wife would", "The girls."). 153 s. Prime Prometics has 2,702 active ads.
- **Resilia · Moshe Goldberg: “I'm 93 years old. I've never had high blood pressure. I've never had a…”** (1 days live): Opens: “I'm 93 years old. I've never had high blood pressure.”
- **Resilia · Active Longevity Review: A monk holding the pouch** (1 days live): A monk holding the pouch: "2 soft gels a day keeps clogged arteries away. BUY 3 GET 2 FREE."

**Do not copy (seen in these live ads):** The monks and elders appear AI-generated. Use real people.

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| 0-5s | Street interview: a lively 80-year-old woman in gold jewellery, reporter holds a mic | Reporter: "What's your secret?" She laughs: "Three things." |
| 5-20s | Thing #3 (save the product for #1) | "I walk every day, rain or not." |
| 20-35s | Thing #2 | "I never let anyone tell me I'm too old for anything." |
| 35-50s | Thing #1: she holds up her necklace | "And I wear what I love, every day. My granddaughter got me this. I swim in it." |
| End | Product + offer | "Any 7 for $85." |

### Prompts

**Veo 3**

```
street interview, an elegant 80-year-old woman with silver hair and a thin gold necklace laughing, handheld mic, sunny European street, shallow depth of field, 8s, 9:16
```

**Real version**

```
Interview a real older customer (with consent); film handheld with a lav mic.
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
- [ ] Files named `F93-<concept>-<variant>`; tracking tag `utm_content=F93-<concept>-<variant>`.
- [ ] Avoid: AI people must be labelled; never present an AI elder as a real customer.
- [ ] Avoid: No health or longevity promises; jewellery is a habit, not a cure.
- [ ] Avoid: Keep the elder dignified; she is the hero, not the punchline.

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
5. Name every asset `F93-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F93
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

A street-interview hook ("How old is your grandson?" "That's my grandson's grandson") reveals a startlingly old, healthy elder, who then counts down three habits. The first two are free, familiar tips (olive oil, onions); the third is the product. Age is the authority; the countdown hides the pitch until the end.

### Why it works

- Age surprise is a strong scroll-stopper and reads as organic street content.
- Two free tips build trust before the product appears as #3.
- "Save this video, you never know when you'll need it" drives saves and shares.
- Resilia produces it entirely with AI people; @ZedNilm1: "none of it is real… age-based authority without the actual talent". That is the compliance problem.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0:00-0:06 | Interviewer with mic stops a stylish 84-year-old woman with a gold chain | "How long have you been wearing that necklace?" "Every day since 1968." |
| 0:06-0:20 | #1 free tip | "Number one: buy fewer pieces and wear them every day." |
| 0:20-0:35 | #2 free tip | "Number two: never buy anything that turns your skin green." |
| 0:35-0:55 | #3 = product (only if she is a real LC customer) | "Number three: my granddaughter got me these. I swim in them." |
| 0:55-1:00 | CTA card | "Any 7 for $85." |

### Hooks

- "How long have you been wearing that necklace?" "Every day since 1968."
- "I'm 84 and I've never taken my jewelry off. Three rules."
- "Save this, my grandmother's three jewelry rules."

### Production recipe

1. Only real people: LC customers 65+ (or their grandchildren) with written consent.
2. Shoot vertical, handheld, lav mic; keep the countdown tips genuinely useful.
3. The product must be #3 only if she really wears LC.

### Existing bot prompt

```
Write a 60-second elder-interview countdown for LC with a REAL customer {{NAME_AGE}}: surprise-age opener, 2 genuine jewelry-care rules, #3 = her LC piece (only what she actually said), save-this line, CTA. No invented ages, quotes or people.
```

### Variants to test

- Interview vs to-camera
- Product #3 vs no product

## Reference examples

See [examples/README.md](examples/README.md) (6 posts). Top 5:

- @ladprofit (0L/0BM/0V): US Under Secretary flagged scam ads using "hidden knowledge" ethnic secrets + romantic-betrayal drama; quoted re Resilia. — https://x.com/ladprofit/status/2100156940483760583
- @ZedNilm1 (116L/185BM/17kV): Resilia AI street interviews with 90+ year olds - believable, near-zero ad feel. — https://x.com/ZedNilm1/status/2101280447154036917
- @orbit_media_ (0L/0BM/0V):  — https://x.com/orbit_media_/status/2066967439095771257
- @IMJustinBrooke (79L/127BM/6kV): Passing on my best wisdom, pt 8 21yrs of Hook Writing Advice in <600 Words As I thought about everything I could probably teach you, one thing stood out as the  — https://x.com/IMJustinBrooke/status/2095535789836824724
- @FedotOff90 (52L/67BM/9kV): Ryze Superfoods is doing multiple 9 figs with 1 product and crazy creative strategy. Massive ad library. Did the full analysis with Gethookd MCP and API. Here's — https://x.com/FedotOff90/status/2092303494250135860
