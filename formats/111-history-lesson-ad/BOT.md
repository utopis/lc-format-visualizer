# BOT.md · generate a "History-lesson ad (\"2,000 years ago people did X. Then the industry changed it for profit. Here's the version that goes back to the original\")"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 60-90s, 1080x1920 (and 4:5), documentary VO, era date stamps, big serif captions), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@LachezarVoynov](https://x.com/LachezarVoynov/status/2079594476352246083) · A 1:57 fully AI-generated vertical ad. A blonde presenter in a pink tank top time-travels through the history of hair-loss treatment, talking to camera like a travel vlogger. 0:07 an ancient Chinese apothecary (on-screen "3,000 years of hair loss treatment"), where an herbalist explains blood flow to the scalp; 0:36 a village in India grinding turmeric for the scalp; 0:51 "two completely separate 
- Example: [@LachezarVoynov](https://x.com/LachezarVoynov/status/2072708967147471270) · history lesson ads are money printers rn people on social media love conspiracy theories everyone knows that big household corporations optimise for p
- Example: [@LachezarVoynov](https://x.com/LachezarVoynov/status/2050577141197087015) · history-lesson ad creatives are the most untapped ad creative style in the eComm space right now perfect for saturated niches humans never get tired o
- Example: [@LachezarVoynov](https://x.com/LachezarVoynov/status/2062925236916420679) · History lesson ads. This uses storytelling to keep the viewers' attention. Give people a quick rundown on how your industry ended up in the terrible s
- Example: [@LachezarVoynov](https://x.com/LachezarVoynov/status/2027442187835695191) · Meta ad creatives at their finest. Don't sell your product. Give people a history lesson. Educate them on how the industry you are in ended up in the 
- Example: [@LachezarVoynov](https://x.com/LachezarVoynov/status/2041181235230232837) · I have a new favorite ad library to get inspired by. The Conscious Bar. Their content is so clean and so aesthetically pleasing that you just watch it

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| 0-4s hook | AI period still animated in Kling: a Roman woman stepping into steaming baths, a gold bracelet catching light. Serif text: "Why Roman women never took their gold off". Era stamp "27 BC" | VO: "Two thousand years ago, Roman women wore their gold into the baths. Every single day." |
| 4-15s past | Museum-style close-ups or AI renders: Egyptian collar, Byzantine ring, 1700s locket, all still shining | VO: "Real gold doesn't rust or tarnish. That's why these pieces still shine in museums." |
| 15-30s change | AI 1950s factory line dipping brass in colour; cut to a modern $5 earring counter. Stamp "1952" | VO: "Then jewelry got cheap: brass with a coat of colour thinner than a hair." |
| 30-42s status quo | Green-finger close-up, a tarnished chain in a drawer, rings taken off before a shower. Stamp "today" | VO: "By week three it's green and dull. We were taught that's normal. It isn't." |
| 42-60s return to the original | Qirra's hands at the workbench, PVD chamber B-roll, a necklace going into the ocean | VO: "Louise Carter went back to the original rule: jewelry you never take off. 14K gold bonded with PVD." |
| 60-75s offer | Stack on a wet wrist in the sea → product grid → "any 7 for $85" | VO: "Wear it like the Romans did." CTA: Shop the stack |

### Prompts

**Script (Claude / GPT)**

```
Write a 75 s history-lesson ad for Louise Carter: hook set in the past with a date; 2-3 real, checkable facts about historical gold jewelry (list a source for each); how plated costume jewelry changed the category (no named competitor); today's visible letdown (green fingers, taking rings off to shower); LC as the return to the original (PVD 14K, waterproof); offer any 7 for $85. 150-200 words.
```

**Period stills (Nano Banana / GPT Image)**

```
"Cinematic photoreal scene, ancient Roman bathhouse, steam, warm torchlight, a woman in a linen stola lowering herself into the water, a thick gold bracelet on her wrist catching the light, 35mm film grain, documentary lighting, 9:16"; one prompt per script line, same colour grade.
```

**Motion (Kling 3.0 image-to-video)**

```
Slow push-in, 5 s per still, subtle steam/water movement, no face morphing; keep the jewelry shape fixed.
```

**VO (ElevenLabs / human)**

```
Calm documentary narrator, 150 wpm, low strings or room-tone ASMR under it.
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
- [ ] Files named `F111-<concept>-<variant>`; tracking tag `utm_content=F111-<concept>-<variant>`.
- [ ] Avoid: Invented history kills trust: every fact needs a source in the doc before the edit.
- [ ] Avoid: AI renders must not be presented as real museum artefacts; label AI where required.
- [ ] Avoid: "Conspiracy" framing ("the industry is poisoning you") is a claim; keep the enemy to verifiable facts (plating wears off).
- [ ] Avoid: Too long before the product: test 45 s and 90 s cuts; Voynov's examples run 75-117 s.

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
5. Name every asset `F111-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F111
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

A 60-120 second video that **doesn't sell the product first. It tells the story of the category.** It opens in the past ("In ancient Rome…", "For 3,000 years monks…", "Before 1950 every chocolate bar was…"), shows how people used to solve the problem, then explains **how and why the industry changed** (cheaper materials, shortcuts, profit). It lands on today's status quo (what the viewer is buying now and why it disappoints them), and only then introduces the product as **the return to the original way**. The visuals are AI-generated period scenes (Nano Banana / Kling), archive art or museum B-roll, and a calm documentary narrator.

Lachezar Voynov's recipe ([post](https://x.com/LachezarVoynov/status/2072708967147471270)): *"tell them how everything started → explain how and why things changed → show them what the current status quo is → then introduce your product, which is the solution and the only alternative on the market."*

### Why it works

- **The brain files it as education, not advertising** ([post](https://x.com/LachezarVoynov/status/2050577141197087015)). "You get their attention for free because you're not asking for a sale."
- **Humans never get tired of a good story.** A time-travel open loop ("how did we get here?") holds attention past the 3-second mark.
- **It builds an enemy without naming a competitor.** "The industry optimised for profit" makes the viewer angry at the status quo ([post](https://x.com/LachezarVoynov/status/2079594476352246083): "it makes them angry, it evokes a response"), and the product becomes "not a solution but the only viable option."
- **Built for saturated markets** (supplements, skincare, SaaS, and jewelry) where every brand claims the same benefit. A history lesson gives you a new reason to believe.
- **Low frequency, unaware audience.** It reaches people who aren't shopping yet, which is where Adam Taylor says most accounts spend $0 (strategy 44).

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time | Visual | Audio / copy |
|---|---|---|
| 0-4 s | AI period still animated (Kling): a Roman woman stepping into steaming baths, a gold bracelet catching light. On-screen: "Why Roman women never took their gold off" | VO: "Two thousand years ago, Roman women wore their gold into the baths. Every single day." |
| 4-15 s | Museum close-ups / AI renders: Egyptian collar, Byzantine ring, a 1700s locket. Each one still shines. | "Real gold doesn't rust, doesn't tarnish and doesn't care about water. That's why you can still see these pieces in museums today." |
| 15-30 s | Shift to a 1950s factory (AI), then a modern fast-fashion counter with $5 earrings | "Then jewelry got cheap. Brass dipped in a coat of colour thinner than a hair. It looks like gold on day one…" |
| 30-42 s | Green-finger close-up, a tarnished chain in a drawer, taking rings off before the shower | "…and by week three it's green, it's dull and you're taking it off to wash your hands. We were taught that's normal. It isn't." |
| 42-60 s | LC founder hands (Qirra) at a workbench; PVD chamber B-roll; a necklace going into the ocean | "Louise Carter went back to the original rule: jewelry you never take off. 14K gold bonded with PVD, so you can swim, shower and sweat in it." |
| 60-75 s | Stack on wrist in the sea → product grid | "Any 7 pieces for $85. Wear it like the Romans did." CTA: Shop the stack |

### Hooks

- "Why Roman women never took their gold off"
- "In 1950 jewelry changed forever, and nobody told you"
- "Your grandmother's ring is 60 years old and still shines. Your new one went green in a month. Here's why."
- "The jewelry industry has a secret it doesn't want you to know about the 1980s"
- "How monks / sailors / pearl divers wore jewelry in the sea" (Voynov's "Monk history lesson" variant)

### Production recipe

1. **Research (1 h):** three real, checkable historical facts about the category (for LC: Roman and Egyptian gold jewelry, why gold doesn't corrode, when plated costume jewelry became mass-market). Write the source next to every fact.
2. **Script (VSL bones, F72):** past → change → status quo → enemy (the shortcut, never a named competitor) → product as the return to the original → offer. 150-200 words for 75 s.
3. **Visuals:** Nano Banana / GPT Image period stills (one per line), animated with Kling 3.0 image-to-video; museum B-roll only where the licence allows; real LC footage for the last third.
4. **VO:** calm documentary narrator (human or ElevenLabs), with low strings or ASMR room tone.
5. **Edit:** big serif captions, 1 cut every 2-3 s, a date stamp on each era ("27 BC", "1952", "today").
6. **Variants:** 3 hooks (era-first / mystery-first / grandmother's ring), 2 lengths (45 s and 90 s).

### Existing bot prompt

```
Write a 75-second history-lesson ad for <BRAND> (<PRODUCT>, <OFFER>). Structure: (1) hook set in the past, 1 line, with a date or place; (2) how people solved <PROBLEM> back then (2-3 real, checkable facts; list the source for each); (3) how and why the industry changed (cheaper materials, shortcuts, profit) without naming a competitor; (4) today's status quo and how it lets the viewer down (a specific, visible moment); (5) the product as the return to the original way (one mechanism line); (6) offer + CTA. Then a shot list: one AI period image prompt per line (Nano Banana style), Kling motion note, on-screen text, and an era stamp. No invented history, no health claims, no 'ancient secret' that isn't real.
```

### Variants to test

- AI period scenes versus museum/archive B-roll
- Narrator VO versus founder (Qirra) telling it to camera (founder-story wrapper, F27)
- ASMR room tone versus strings
- 45 s versus 90 s (Voynov's examples are 75-117 s)

## Reference examples

See [examples/README.md](examples/README.md) (7 posts). Top 5:

- @LachezarVoynov (396L/1453BM/88kV): 29 TOF video ad formats to test on Meta (transformation, Suno song, skit, beginner-intermediate-expert...). — https://x.com/LachezarVoynov/status/2086842038457098499
- @LachezarVoynov (0L/0BM/0V):  — https://x.com/LachezarVoynov/status/2041181235230232837
- @LachezarVoynov (0L/0BM/0V):  — https://x.com/LachezarVoynov/status/2072708967147471270
- @LachezarVoynov (0L/0BM/0V):  — https://x.com/LachezarVoynov/status/2027442187835695191
- @LachezarVoynov (0L/0BM/0V):  — https://x.com/LachezarVoynov/status/2079594476352246083
